---
layout: post
title:  "Finding records with Ember Data"
date:   2015-11-06 06:30:00
categories: ember
---

One of the concepts I didn't completely understand when initially learning Ember
were the different methods that can be called on models to retrieve records from
the Ember Data store.

My initial apps only used the `find` method, which provides records of a single type, but there are others that can be used as well including `findAll` and `findQuery`. These initial apps weren't backed by a database either so everything was loaded from fixtures and new records were destroyed upon a page refresh.

```javascript
export default Ember.Route.extend({
  model: function (params) {
    return this.store.find('recipe', params.recipe_id);
  }
});
```

In a recent app, it was connected to a Rails API and was using the `findQuery` method to retrieve records from the Ember Data store. I didn't write the initial code, I was only adding features to the app, so I wasn't familiar with `findQuery`. In adding features to the app, I created a form to add new records and a function in my controller that would grab the data from the form and save the new record. I ran into one problem though. Although my Ember app was making a POST request to the Rails backend to save the record to the database, the DOM was not automatically updating with the new record.

```javascript
// In my model:
model: function(params) {
  return this.store.findQuery('memory', params);
}

// In my controller:
addNewMoment: function () {
      let moment = this.getProperties('caption', 'content', 'location', 'happenedAt');
      this.store.createRecord('moment', moment).save();
    }
```

I felt like I had tried everything and couldn't figure out why the record was saving to the database, but wasn't updating on the front-end in my Ember app. It turns out the reason why my record wasn't saving was because of the `findQuery` method in my model.

If you use the `findQuery` method, it puts the job of filtering on the server's back. Ember Data assumes that the results that were returned initially are the only results that are associated with that collection, so it will only make the call to the database once. In this case, you can manually push a new record into a collection of records using `pushObject`."

```javascript
  // If using findQuery, something like this
  // will push the new record into the collection:
  var model = this.get('model');
  model.pushObject(moment);
```

This is when I realized that I needed to pay closer attention to the methods that I was calling in my models and started to learn what all the different ones will do for you.

Basically, `findAll` will return all the records of a specific type and will trigger a request to the server, `all` is essentially the same, but uses the cache, so if you have records in your store, no request will be made, `findById` returns a single object and as we discussed earlier, `findQuery` will return a subset from your server.

Here's [a bit more information](https://github.com/emberjs/data/blob/master/packages/ember-data/lib/system/store.js#L431) in the Ember source code.

I hope this was helpful for other Ember beginners learning the framework.

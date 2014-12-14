jlslides
========

JavaScript Presentation Framework using AngularJS

[Demo](http://joshualat.com/slides/angularjs-restangular/)

~~~ html
<slide title="Introduction" link="intro" page="1">
  <blue>Backbone.js</blue> has models and collections. <br />
  <blue>Ember.js</blue> has Ember Data and ember-model. <br />
  What about <red>AngularJS</red>?
</slide>

<slide title="Introduction" link="intro" page="2">
  <red>$resource</red> for data models?
  <prism class="language-javascript">
    angular.module('login').provider('User', function() {
      this.$get = ['$resource', function($resource) {
        var User = $resource('http://localhost:8080/user/:_id', {}, {
          update: {
            method: 'PUT'
          }
        })

        return User;
      }];
    });
  </prism>
</slide>
~~~
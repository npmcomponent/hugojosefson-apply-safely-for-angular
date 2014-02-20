*This repository is a mirror of the [component](http://component.io) module [hugojosefson/apply-safely-for-angular](http://github.com/hugojosefson/apply-safely-for-angular). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/hugojosefson-apply-safely-for-angular`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# apply-safely-for-angular

  Calls `fn` with or without `scope.$apply()`, depending on if current thread is already inside `$apply()`. For AngularJS.

## Installation

### As a [component](https://github.com/component/component)

    $ component install hugojosefson/apply-safely-for-angular

### With [Bower](http://bower.io/)

    $ bower install hugojosefson-apply-safely-for-angular

## API

    require("applySafely");

    // Example use
    angular.module("yourModule", []).controller("yourController", function($scope, applySafely) {

      someNonAngularCodeWhichCallsBack("params", function callback(result) {
        applySafely($scope, function() {
          $scope.result = result;
        });
      });

    }); 

## License

  MIT

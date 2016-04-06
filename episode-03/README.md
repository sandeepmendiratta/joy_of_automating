### Episode 3 - Working with Legacy Code (Redis)

Air Date: April 1, 2016 10AM PDT

In this episode we focused on understanding, testing, and refactoring an existing cookbook.

* [Recording](https://www.youtube.com/watch?v=Td1MMyvwaF8)

## Resources

### Activity

In this episode we focus on testing and refactoring and existing cookbook found here: https://github.com/chef-training/redis.

### Further Activities

Now that the default recipe is under test there are so many places that you can take your practice.

* Clarity in Resource Names

The execute resources within the recipe have their commands specified in their names. This creates for very brittle tests if you were to change version numbers or the flags of the command. It would be better if the command were stored in their appropriate attribute.

A resource named `make && make install` could be named `redis_build_and_install`.

First update the specifications to more clearly state the intention of the command. Run the tests to see the failure. Update the recipe and see the tests pass.

* Continue to refactor the tests

The tests within the cookbook are code you maintain as well. As we refactored the version number into a node attribute it would also be good to extract that version number into a `let` helper method. This will reduce the number of times we repeat the version number in the specification.

Another important step after defining the version number in a `let` helper method would be look at specifying the version value in as a node attribute for the chef-client run. ChefSpec provides the ability to set attributes.

* Continue to extract more values into attributes

Providing more values as attributes allows for a more flexible cookbook. The source location that we request Redis from

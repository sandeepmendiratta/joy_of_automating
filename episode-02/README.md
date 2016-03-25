# Episode 2 - Scripts to Recipes (Installing Django)

Air Date: March 25, 2016 10AM PDT

In this episode we focused on converting the installation of Django into tested recipes. We explored installing Django from multiple sources: packages; pip; and through virtualenv. Which lead us into writing integration tests and unit tests for the various recipes, defining multiple test kitchen suites, and git branch workflow. Near the end we started to define a custom resource within the cookbook to handle our requests to install packages through pip.


* Recording - https://www.youtube.com/user/getchef/live

## Resources

### Activity

In this episode we focus on taking the manual installation instructions found in [this tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-the-django-web-framework-on-ubuntu-14-04) and create a recipe that does the work for us.

* [How to Install The Django Web Framework](https://www.digitalocean.com/community/tutorials/how-to-install-the-django-web-framework-on-ubuntu-14-04)

This is the code that was completed during the exercise: https://github.com/chef-training/django

### Further Activities

After completing the initial activity we encourage you to challenge yourselves with the following activities.

* Another Installation

We walked through several installations. As an exercise walk through another manner of installation. In this case installing Django from source.

* Custom Resource

We defined a pip custom resource and by default we set it up to support for installation by name. In the last installation method we are installing from source.

To support that approach the custom resource needs to be updated to support a source attribute.

The next problem is to specify the right value with the correct flag when it comes time to install from source. This means if the source attribute has been specified we want to ignore the resource name and ensure we include the flag.

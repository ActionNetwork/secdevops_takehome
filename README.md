# Action Network Developer Operations and Security Engineer Take Home Assignment

This take home assignment is designed to allow you to demonstrate DevOps and security skills. 

## Expectations and Deliverables

Our expectations are:

* There is no time limit or due date, though we expect this may take at least a couple days to accomplish and test. An honorarium will be provided as compesation for this work.
* This is a skills test, so we do not expect the finished product to be production ready.
* That said, we do expect to be able to run your work ourselves to see what you've done and how it functions.

Your deliverables are:

* A repository on GitHub (public or private) with your work, accomplishing the goals set out in the instructions below. (Feel free to fork this repository if you'd like.)
* A writeup (including diagrams if desired) of your infrastructure and setup. (Can be a readme type file in the repository if you want.)
* Instructions for how to run your code ourselves and demonstrate the features, including any necessary services we need to sign up for, etc... (Can be a readme type file in the repository if you want.)

When you are finished, email a link to your repository, writeup, and instructions to your hiring contact. If you need our GitHub usernames to add to a private repository, we can provide those.

## Instructions and Goals

Your goal with this assignment is to write infrastructure as code that provisions a set of web servers in an auto scaling group behind a load balancer. (No need to set up a databse or a full web application stack, though you can if you want.)

The auto scaling group should have 3 servers in it by default, with a max of 5 total, and scale and descale based on simulated load (so your work should have a way to manually simulate load or send some kind of scaling signal to cause scaling and descaling to happen). The servers should serve a basic html page that says “Hello world” with the current date and time, at some kind of publicly available endpoint (does not have to be a full website, can be a load balanceer URL of a cloud service for instance). Bonus points for zero manual config on boot. (This could all be accomplished with Terraform, Chef, Elasticbeanstalk, etc...)

In addition, write a method to automatically update or replace servers whenever a new security update for the operating system or installed packages is available (or perhaps on some kind of schedule, like nightly), making sure to test servers running the new configuration are alive and serving before putting them in to the load balancer.

Your setup should also take into account industry-standard security practices, including encryption in flight and at rest (feel free to use a self-signed certificates), no secrets checked into GitHub, etc...

We use Ruby on Rails, Linux (Ubuntu primarily), Chef or Elasticbeanstalk, Cloudformation, and AWS for our main stack, but feel free to implement on whatever stack you're most comfortable with.

If you have any questions as you go, please don't hestitate to reach out to your hiring contact.

Good luck! We're looking forward to seeing your work!

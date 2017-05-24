# RFC-1 The Idea

### Introduction

The serverless computing[1] paradigm offers significant advantages over more conventional cloud computing models[2]. 
But as serverless computing platforms such as Amazon Lambda becomes more popular,
it also locks in the clients into its own closed technology platform. This naturally is harmful to the clients 
freedom of choice as well as the competition. It also might hinder the advancement of the technology. 
To prevent this an open and transparent effort from the open source community is needed to advance this next generation technology. 
Open Lambda is an open source project inspired by this idea. 
 
 ### Vision
 
 Core vision of the Open Lambda project is `Pure Functions Everywhere`. 
 Therefore the goal is to enable running functions written in any language on any platform to accomplish 
 any task without the overhead of managing the platform by your self. Functional layer of any app can and should be 
 separated from the concerns about managing the underlying platform from the perspective of 
 the program as well as the programmer. 
 
 ```
 +------------------+
 |                  |
 |  User functions  |
 |                  |
 +------------------+
 |                  |
 | Isolation layer  |
 |                  |
 +------------------+
 |                  |
 | Platform eg:     |
 | devices, cloud   |
 +------------------+

 ```
 
 Open Lambda while accomplishing this goal, will go further in helping users to 
 structure their programs better with `pure functions` as the basic building block. 
 
 ```
                   +------------------------------------------------------+
                   |           External services required by functions    |
                   |                                                      |
                   +------+----------------------------------+------------+
                          ^                                  ^
                          |                                  |
                          |                                  |
                          |                                  |
                        +-+--+                             +-+--+
                        |    |                             |    |
  +-----------------+   |    |      +-------------------+  |    |      +-------------------+
  |                 |   |    |      |                   |  |    |      |                   |
  | function 1      |   |    |      |    function 2     |  |    |      |     function 3    |
  |                 |   |    |      |                   |  |    |      |                   |
  +-----------------+   |    |      +-------------------+  |    |      +-------------------+
 +----------------------+    +-----------------------------+    +-----------------------------+
 |                                                                                            |
 |           Open Lambda isolates running user functions services and execution platform      |
 |                                                                                            |
 +--------------------------------------------------------------------------------------------+
 |                                                                                            |
 |                        Runtime eg: the cloud, hardware                                     |
 |                                                                                            |
 +--------------------------------------------------------------------------------------------+


 ```
 
 One could argue its like an operating system for running functions anywhere.
 
 
 
 ### references
 
 1. [Serverless computing](https://en.wikipedia.org/wiki/Serverless_computing)
 2. [Serverless Advantages](https://www.infoq.com/articles/serverless-takes-devops-next-level)
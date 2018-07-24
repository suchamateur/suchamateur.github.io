---
layout: post
title:  "Run unit test with catkin build tool"
date:   2018-07-24 22:15:18 +0800
categories: ROS catkin
---
# Run all tests
{% highlight terminal %}
catkin run_tests
{% endhighlight %}

# Run tests for specific package
{% highlight terminal %}
roscd <pkg_name>
catkin run_tests --no-deps --this
{% endhighlight %}
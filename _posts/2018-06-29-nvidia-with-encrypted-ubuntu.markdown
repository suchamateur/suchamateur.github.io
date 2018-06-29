---
layout: post
title:  "Nvidia graphics in encrypted Ubuntu 16.04"
date:   2018-06-29 09:59:18 +0800
categories: Ubuntu
---



[Original Post][original-post]

# 1 Update GRUB
In `/etc/default/grub`, change `GRUB_CMDLINE_LINUX_DEFAULT="quiet-splash"` to `GRUB_CMDLINE_LINUX_DEFAULT=""`

{% highlight terminal %}
sudo update-grub
{% endhighlight %}

# 2 Disable default graphics driver
Create a file `/etc/modprobe.d/blacklist-nouveau.conf`

with content:
{% highlight terminal %}
blacklist nouveau
options nouveau modeset=0
{% endhighlight %}

# 3 Stop X-server
{% highlight terminal %}
sudo service lightdm stop
{% endhighlight %}

# 4 Update kernel
{% highlight terminal %}
sudo update-initramfs -u
sudo reboot
{% endhighlight %}

# 5 Stop X-server
{% highlight terminal %}
sudo service lightdm stop
{% endhighlight %}

# 6 Install Nvidia driver
sudo <xxxx>/xxxx.run
reboot

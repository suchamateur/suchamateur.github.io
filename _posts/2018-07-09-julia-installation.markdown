---
layout: post
title:  "Install latest Julia with Ubuntu 16.04"
date:   2018-07-09 14:15:18 +0800
categories: Ubuntu Julia
---
# 1 Download latest Julia
[Julia Download][julia-download]
`Generic Linux Binaries for X86`

# 2 Extract and make soft link for julia executable
{% highlight terminal %}
sudo ln -s %EXTRACTED JULIA DIRECTORY%/bin/julia /usr/local/bin/julia
{% endhighlight %}

# 3 Update Julia packages
{% highlight Julia %}
Pkg.add("PyPlot")
{% endhighlight %}

[julia-download]: https://julialang.org/downloads/
---
layout: post
title:  "Shadowsocks with chacha20-ietf-poly1305 encryption"
date:   2018-06-26 01:45:18 +0800
categories: Ubuntu
---
[Original Post][original-post]

# 1 Install libsodium
{% highlight terminal %}
sudo apt-get install libsodium-dev
{% endhighlight %}

# 2 Install libbotan-2.x from source
{% highlight terminal %}
wget https://botan.randombit.net/releases/Botan-2.3.0.tgz
tar xvf Botan-2.3.0.tgz
cd Botan-2.3.0
./configure.py
make
sudo make install
sudo ldconfig
{% endhighlight %}

# 3 Install libQtShadowsocks
{% highlight terminal %}
git clone https://github.com/shadowsocks/libQtShadowsocks.git
cd libQtShadowsocks
mkdir build
cd build
cmake ..
make
sudo make install
{% endhighlight %}

# 4 Install dependencies for shadowsocks-qt5
[Shadowsocks-qt5 dependencies][ss-qt5-deps]

# 5 Install shadowsocks-qt5
{% highlight terminal %}
git clone https://github.com/shadowsocks/shadowsocks-qt5
cd shadowsocks-qt5
mkdir build
cd build
cmake ..
make
sudo make install
{% endhighlight %}

[ss-qt5-deps]: https://github.com/shadowsocks/shadowsocks-qt5/wiki/Compiling
[original-post]: https://github.com/shadowsocks/shadowsocks-qt5/issues/595
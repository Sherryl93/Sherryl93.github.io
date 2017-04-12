---
layout: post
title:  "Training CNN with ImageNet and Caffe"
description: understanding deep learning
date: 2017-04-12 10:00:25 
img: collage_s.png
categories: Caffe, CNN, ImageNet
author: PSS
---
This post is a tutorial to introduce how [`Convolutional Neural Network (CNN)`](http://cs231n.github.io/convolutional-networks/) works using `ImageNet` datasets and `Caffe` framework.

[`ImageNet`](http://www.image-net.org/) is a large-scale hierarchical image database that mainly used by vision related research.

[`Caffe`](http://caffe.berkeleyvision.org/) is one of the widely used deep learning framework. The performance is quite fast and this framework focuses on Computer Vision area. 

now lets get started!

## Install Caffe to your system:
*Assumed you already done the prequisite step for your system, if you haven't go [here](http://caffe.berkeleyvision.org/installation.html).*

**Steps:**
{% highlight markdown %}
> git clone https://github.com/BVLC/caffe.git
> cd caffe
> mkdir build
> cd build
> cmake ..
> make -j13 or make all
> make install
> make runtest
{% endhighlight %}

## Data Preparation:
### 1. Download ImageNet 2012 data
First, you need to download the ImageNet 2012 Training data from [here](http://image-net.org/challenges/LSVRC/2012/browse-synsets) and put it under *'caffe/data/ilsvrc12/'* root folder.
Then, download auxilaries, to do this you can use `get_ilsvrc_aux.sh` under *'caffe/data/ilsvrc12/'*  and run:
{% highlight markdown %}
> sh get_ilsvrc_aux.sh
{% endhighlight %}
Now you have downloaded all data.
### 2. Convert data to lmdb


Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

## Headings

Headings by default:

## Heading first level
### Heading second level
#### Heading third level

{% highlight markdown %}
## Heading first level
### Heading second level
#### Heading third level
{% endhighlight %}

## Lists

Unordered list example:
* Unordered list item 1
* Unordered list item 2
* Unordered list item 3
* Unordered list item 4

Ordered list example:
1. Ordered list item 1
2. Ordered list item 1
3. Ordered list item 1
4. Ordered list item 1

{% highlight markdown %}
* Unordered list item 1
* Unordered list item 2

1. Order list item 1
2. Order list item 1
{% endhighlight %}


## Quotes

A quote looks like this:

> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna.

{% highlight markdown %}
> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

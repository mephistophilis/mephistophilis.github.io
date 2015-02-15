---
layout: post
title: 安装Jekyll
---

作为一个上进的码农，除了应该懒惰之外，还应该保持对新事物的敏锐嗅觉，如果鼻子不好使，不求走在前沿，但最起码应该对已经看到的新事物有好奇心。虽然到我看到jekyll的时候，这东西都已经出现了好几年了，但是看到不少开源项目的大神都在用这东西写博客，所以还是义无反顾跟上大神的的脚步。

下面纪录一下之前的安装过程。

 1. github里开一个repository。  
	 [pages.github.com](https://pages.github.com/)有详细步骤。

 2. 安装Jekyll  
	 osx的系统里自带ruby。虽然自带ruby，但是Jekyll依赖一大堆Ruby Gem，我很担心这玩意装上以后把系统搞的乱七八糟。所以打算使用rbenv和ruby-build。

	osx里已经安装了homebrew，所以安装rbenv 和 ruby-build很方便。  
    `brew install rbenv ruby-build`

	bash.rc里加入：  
	   `if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi`
	    
	打开新的terminal：  
	   `rbenv install 1.9.3`  
	   `rbenv global 1.9.3`  
	   
	   `gem install bundle`  
	   `rbenv rehash`  
	   
	   创建一个 Gemfile文件里面写入：  
	   `source 'https://rubygems.org'`  
	   `gem 'github-pages’`  
	
	然后运行  
		`bundle install`  
		`rbenv rehash`  
	 
	 如果所有步骤都成功了，jekyll就安装成功了。
	
	mkdir 创建一个新的目录 test。  
	进入目录执行，  
	`jekyll new .`  
	然后再执行   
	`jekyll server`  
	
	用浏览器打开127.0.0.1:4000可以看到jekyll已经正常工作。



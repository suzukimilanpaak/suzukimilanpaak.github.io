---
layout: post
title: 'Note: How to show SQL in Rails Console'
date: '2012-04-22T11:51:00.000+01:00'
author: Suzuki MilanPaak
tags:
- Ruby/ Ruby on Rails
modified_time: '2012-05-23T15:00:51.944+01:00'
blogger_id: tag:blogger.com,1999:blog-6758697817819098194.post-7101700334507754620
blogger_orig_url: http://engineerflies.blogspot.com/2012/04/note-how-to-show-sql-in-rails-console.html
---

Just add the following lines into&nbsp;&nbsp;config/environment.rb. This switches default logger to STDOUT.

    # Render SQL in Rails Consoleif "irb" == $0  require 'logger'  if ENV.include?('RAILS_ENV')&&  !Object.const_defined?('RAILS_DEFAULT_LOGGER')     Object.const_set('RAILS_DEFAULT_LOGGER', Logger.new(STDOUT))  else     ActiveRecord::Base.logger = Logger.new(STDOUT)  endend


---
layout: post
title: Accessing ActionView::Base in a ActionController in Rails 2.3
date: '2012-04-27T05:42:00.003+01:00'
author: Suzuki MilanPaak
tags:
- Ruby/ Ruby on Rails
modified_time: '2012-04-27T05:42:39.782+01:00'
blogger_id: tag:blogger.com,1999:blog-6758697817819098194.post-740139147285339400
blogger_orig_url: http://engineerflies.blogspot.com/2012/04/accessing-actionviewbase-in.html
---

just came accross an instance variable of an ActionView::Base in ActionController, which is @template;

    class AnyController def index logger.debug @template.inspect #=> # endend


---
# Leave the homepage title empty to use the site title
title:
date: 2025-12-14
type: landing

sections:
  - block: hero
    content:
      title: FoMaSE Project
      image:
        filename: welcome.png
      text: |
        
        **FoMaSE (Foundations for Macroprogramming-based Software Engineering)** is a basic research project 
        led by principal investigator **Roberto Casadei**  
        that was awarded the Italian *FIS3 Starting Grant for ~€1.1M*.  
        It aims to investigate ways for addressing the **micro-macro link** and 
        **artificial collective intelligence** by a computer science and software engineering perspective,
        enabling predictable design of intelligent services and applications (for smart cities and beyond) backed by autonomous artificial collectives.
  - block: collection
    content:
      title: Latest News
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: '1'
  
  # - block: markdown
  #   content:
  #     title:
  #     subtitle: ''
  #     text:
  #   design:
  #     columns: '1'
  #     background:
  #       image: 
  #         filename: coders.jpg
  #         filters:
  #           brightness: 1
  #         parallax: false
  #         position: center
  #         size: cover
  #         text_color_light: true
  #     spacing:
  #       padding: ['20px', '0', '20px', '0']
  #     css_class: fullscreen

  - block: collection
    content:
      title: Latest Publications
      text: ""
      count: 5
      filters:
        folders:
          - publication
        #publication_type: 'article'
        author: Roberto Casadei
    design:
      view: citation
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
---

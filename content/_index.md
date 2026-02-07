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
      # cta: # Call To Action (CTA)
      #   label: Get Started
      #   url: https://wowchemy.com/templates/
      text: |
        
        **FoMaSE (Foundations for Macroprogramming-based Software Engineering)** is a basic research project 
        led by principal investigator **Roberto Casadei** that was awarded the Italian *FIS3 Starting Grant for ~€1.1M*.  
        It aims to investigate ways for addressing the **micro-macro link** and 
        **artificial collective intelligence** by a computer science and software engineering perspective,
        enabling predictable design of intelligent services and applications (for smart cities and beyond) backed by autonomous artificial collectives.
    design: # https://bootstrap.hugoblox.com/blocks/hero/
      css_class: hero-wide-text
      #background:
      #gradient_start: '#ddd'
      #gradient_end: '#fff'
      #text_color_light: 
  - block: features # https://bootstrap.hugoblox.com/blocks/features/
    design:
      background: 
        #gradient_start: "#448"
        #gradient_end: "#448"
        #color: 'navy'
        #text_color_light: true
      spacing:
        padding: ['1rem', '1rem', '1rem', '1rem']
      css_class: 'my-custom-class'
      view: showcase # card, compact, showcase, masonry
    content:
      title: "Key Project Information at a Glance"
      css_class: boh        
      items:
        - name: "2026-2031"
          description: "5-years Project Duration"
          icon: "clock"
          icon_pack: fas
        - name: "University of Bologna"
          description: "Host Institution"
          icon: "university"
          icon_pack: "fas" 
        - name: "~€1.1M"
          description: "Total Funding"
          icon: "euro-sign"
          icon_pack: "fas"
        - name: "Basic Research Project"
          description: "Project Type"
          icon: "mortar-board" # "search-plus" # "search"
          icon_pack: "fas"
        - name: "Roberto Casadei"
          description: "Principal Investigator"
          icon: "user-secret"
          icon_pack: fas 
          # https://bootstrap.hugoblox.com/getting-started/page-builder/#icons
        - name: "Computer Science & Eng."
          description: "Topic Area"
          icon: "microchip" #"computer-desktop"
          icon_pack: "fas"
          #icon: ":computer:"
          #icon_pack: "emoji" 
        # last line
        - name: "&lt;X&gt; Post-Docs, &lt;Y&gt; PhDs"
          description: "Number of Team Members"
          icon: "users"
          icon_pack: "fas"
        - name: "&lt;N&gt; Publications"
          description: "Current Project Output"
          icon: "line-chart" #"arrow-circle-up" # "plane"
          icon_pack: "fas" 
        - name: "&lt;K&gt; Collaborations"
          description: "Inter/national Networking"
          icon: "globe" 
          icon_pack: "fas"
        # last line of icons
        - name: 
          description: | 
            {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
        - name: 
          description: | 
            {{% cta cta_link="./details/" cta_text="Project Details →" %}}
        - name: 
          description: | 
            {{% cta cta_link="./contact/" cta_text="Collaborate →" %}}

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
      spacing:
        padding: [45px,0,0,0]
  
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
        tag: "fomase"
        #publication_type: 'article'
        #author: Roberto Casadei
    design:
      view: citation
      columns: '1'
      spacing:
        padding: [45px,0,0,0]

  # - block: markdown
  #   content:
  #     title:
  #     subtitle:
  #     text: |
  #       {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
  #   design:
  #     columns: '1'
---

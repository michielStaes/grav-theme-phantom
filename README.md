
# Phantom Theme

The **Phantom** [Grav CMS](http://github.com/getgrav/grav) Theme.  
Based on the responsive [Phantom template ](https://html5up.net/phantom)  

![Antimatter](screenshot.jpg)



### Supported Page Templates
* Default view template (home/landing page) `default.md`
* Error view template `error.md`
* generic view template `generic.md`

### Instructions default.md   
default.md is intended to be used as a landing/home page.

#### How to setup a default page using the admin-panel:

 1. Add a new page, select folowing options: ![default-create](https://user-images.githubusercontent.com/26135526/38764368-bb5ec562-3fad-11e8-9dee-c50d22249db2.JPG)
 
 2.![formatter](https://user-images.githubusercontent.com/26135526/38764445-66559918-3faf-11e8-8c79-ed04f896c9f0.JPG)
 Open the expert tab and paste following headers into the Frontmatter: <details><summary>default.md headers</summary>



```python
title: Home
content:
    items: '@self.children'
form:
    name: contact
    fields:
        -
            name: name
            label: Name
            placeholder: 'Enter your name'
            autocomplete: 'on'
            type: text
            validate:
                required: true
        -
            name: email
            label: Email
            placeholder: 'Enter your email address'
            type: email
            validate:
                required: true
        -
            name: message
            label: Message
            placeholder: 'Enter your message'
            type: textarea
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Submit
        -
            type: reset
            value: Reset
    process:
        -
            email:
                subject: '[Site Contact Form] {{ form.value.name|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Thank you for getting in touch!'


```
</details>



  

 3. after saving, you can open the 'normal tab' and navigate to the 'home page settings tab'. To enable/disable extra features of the page. ![home-page-settings](https://user-images.githubusercontent.com/26135526/38764414-d7602804-3fae-11e8-8f35-99c153275b5e.JPG)



## Instructions generic.md 

generic.md is intended to be used as a information/blog page. Clicking a tile on the default page will open the generic page.  
generic.md  YAML header cheatcheat:

| YAML 			 |REQUIRED		| INFO
|----------------|--------------|--------------|
|title			 |required      | Page title. Also represented in the menu.
|image			 |required      | The name of the image. This image will be used in the homepage as a tile.
|style|required  |The style should either be a number between 0 and 6, or the 'random' string. Depending on the number a different colour of tile will be generated in the default page. Random will generate a random colour.  

<details><summary>generic.md example</summary>



```python
---
title: blogpost1
image: pic.jpg 
style: 1


---

# This is Phantom, a free, fully responsive site </br> template designed by <a href="http://html5up.net">HTML5 UP</a>.


Etiam quis viverra lorem, in semper lorem. Sed nisl arcu euismod sit amet nisi euismod sed cursus arcu elementum ipsum arcu vivamus quis venenatis orci lorem ipsum et magna feugiat veroeros aliquam. Lorem ipsum dolor sit amet nullam dolore.



```
</details>


.

### Folder structure  

> intended pages structure

    .
    ├── pages                   
          ├── 01.home                    
                ├── default.md
                ├── 01.blog    
                        ├── generic.md    
                        ├── pic.jpg    


                
    



  

# Phantom Theme

The **Phantom** [Grav CMS](http://github.com/getgrav/grav) Theme.  
Based on the responsive [Phantom template ](https://html5up.net/phantom)  

![Antimatter](screenshot.jpg)



### Supported Page Templates
* Default view template `default.md`
* Error view template `error.md`
* generic view template `generic.md`

### Default.md instructions  
Default.md is intended to be your landing page.

Default.md YAML header cheatcheat:

| YAML 			 |REQUIRED|
|----------------|--------------------------|
|title			 |required    
|content		 |required  
|links			 |not required           
|body_classes	 |not required
|form			 |not required








<details><summary>example</summary>
<p>


```python
---
title: Home
links:
        -
            name: twitter
            url: twitter.com
           
        -
            name: github
            url: https://github.com/youraccount
          
        -
            name: facebook
            url: facebook.com
            
        -
            name: instagram
            url: instagram.com
            
        -
            name: dribbble
            url: dribble.com

        -
            name: 500px
            url: url.com

        -
            name: phone
            url: url.com
        


            
body_classes: title-center title-h1h2
content:
    items: '@self.children'
    

form:
    action: /your-modular-page
    name: my-nice-form
    fields:
        -
            name: name
            label: Name
            placeholder: 'Enter your name'
            autofocus: 'on'
            autocomplete: 'on'
            type: text
            default: 
               
        -
            name: email
            label: Email
            placeholder: Enter your email address
            type: email
            validate:
            required: true

    buttons:
        -
            type: submit
            value: Submit
    
---



# This is Phantom, a free, fully responsive site </br> template designed by <a href="http://html5up.net">HTML5 UP</a>.


Etiam quis viverra lorem, in semper lorem. Sed nisl arcu euismod sit amet nisi euismod sed cursus arcu elementum ipsum arcu vivamus quis venenatis orci lorem ipsum et magna feugiat veroeros aliquam. Lorem ipsum dolor sit amet nullam dolore.

```

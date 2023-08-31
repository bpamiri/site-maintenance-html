# site-maintenance-html

This project allows you to show a nice looking Site Maintenance page by just hosting the HTML. The images and stylesheets are hosted and served directly from this GitHub acount.

Several years ago I was looking for a Site Maintenance page and came accross this project that had five different version on the same theme. Unfortunately I don't remember the site I originally found these to give proper credit. If you know the original source please let me know. I'd love to give them proper credit. 

Anyway, I found five version of the same moving gears all in different colors. I liked them so much, I thought it would be fun to use all five and just randomize which stylesheet got used on load. I achieved this with some simple CFML on the backend and that was that. 

Fastforward a few years and I switched to a new loadbalancer technology that only allowed me to specify a single HTML content for the maintenance page. I would have to figure out how to host the images and stylesheets online. I then figured that you can server these through cdn.statically.io thanks to this [blog post](https://blog.mergify.com/how-to-serve-static-files-from-github/#:~:text=To%20use%20Statically%2C%20simply%20replace,gh%20and%20you%27re%20done.&text=Serving%20the%20same%20file%20through,loaded%20by%20a%20Web%20browser) by Julien Danjou. Then I had to figure out how to change the random number generated which I was using CFML to generate to JavaScript that could be hosted within the HTML. 

With all the pieces put together I now have some simple static HTML that can be paseted or posted anywhere that will use cloud hosted assets and display a maintenance page that cycles through 5 themes randomly.

## To Use

### Hosting the HTML file

If your environment lets you host the HTML file, simply copy the index.html file from this repository and place it in the appropriate directory on your environmet. Rename the file accordingly to match your environment's needs.

### Using just the HTML content

If your environment only gives you access to a field where you can paste the HTML you wish to use for a maintenance page, then just copy the content of the index.html file and paste it into your system. 

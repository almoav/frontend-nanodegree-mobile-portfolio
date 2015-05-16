## Website Performance Optimization portfolio project

####To run:

You can load the website on your local machine by opening
index.html in a web browser.

Alternatively, you can serve it using the steps below:

1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/downloaded-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/downloaded-project-folder
  $> ngrok http 8080
  ```

1. In a web browser navigate to the public URL that ngrok spits out.

###Optimizations to views/main.js

*changePizzaSizes() : removed multiple calls to over-complicated functions, determine container widths
within this function.  Parse all pizza containers once outside of the for-loop.
*updatePositions() : move the body.scrollTop parse to outside of the for loop, preventing FSL.

###Optimization to views/css/style.css

*place .mover on own layers with will-change : transform

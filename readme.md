#sheetCMS


###Step 1: Create a google spreadsheet and enter some data. Select "File / Publish to the web" and copy the url in the pop-up.
![spreadsheet.png](https://image.ibb.co/fy7swF/spreadsheet.png)


###Step 2: Include cmsish.min.js in your project (found in dist/cmsish.min.js).
```
<script src="cmsish.min.js" type="text/javascript"></script>
```


###Step 3: Initiate cmsish and pass it the url to your google spreadsheet:
```
<script type="text/javascript">
var myCms = new cmsish.init('GOOGLE_SPREADSHEET_URL');
</script>
```


###Step 4: In your HTML, wrap your content in a handlebars script tag by entering 
```
<body>
  <script id="entry-template" type="text/x-handlebars-template">
    <!-- All your HTML goes between these script tags -->

    <!-- Stop your HTML now -->
  </script>
</body>
```


###Step 5: Add handlebars template tags to your markup, using the column names from the spreadsheet as the template tags
```
<body>
  <script id="entry-template" type="text/x-handlebars-template">
    <!-- All your HTML goes between these script tags -->

    <h1>{{Title}}</h1>
    
    <p>{{Introtext}}</p>
    
    <p>{{Phone}}</p>
    
    <p>{{Testimonial}}</p>

    <!-- Stop your HTML now -->
  </script>
</body>
```

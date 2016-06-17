Partial JS
----------

 1. A ng-include replacement 
 2. Simple declarative syntax.
 3. Support Inline JS Inside template
 4. Support Script Tags with Src Attribute
 5. Zero dependencies 
  

```
    <partial src="templates/header.html"></partial>`
```
or

```
    <partial src="templates/footer.html" onload="Footerloaded"></partial>
```


More complex 

```
HTML

    <div id="menu" class="list-group">
    <a href="pages/index.html" class="list-group-item active">
        Home
    </a>
    <a href="pages/page1.html" class="list-group-item">About</a>
    <a href="pages/page2.html" class="list-group-item">Contact</a>
    <a href="pages/page3.html" class="list-group-item">Other Links</a>
    
    </div>

```

```
JAVASCRIPT

    $('#menu a').click(function (e) {
        e.preventDefault();
        var path = $(this).prop('href');
        var container = document.getElementById('view');
        partial.getPage(path, container, function (elem) {
            Prism.highlightAll();
        });
        $('.active').removeClass('active');
        $(this).addClass('active');

    });
    

```

 - Simple to use 
 - can do what ng-include dose but without angular
 - 3kb normal side 
 - 2kb minified


 How to use ?

 npm install 

 run.bat 
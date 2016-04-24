# Materialize Pagination

![Pagination screenshot1](/../screenshots/screenshot2.png?raw=true)

Materialize Pagination is a jQuery plugin that provides behaviour and  rendering of the [Materialize Pagination component][1].

### Getting stated

To get the Materialize Paginaton plugin working you first need to include [jQuery][2], [Materlize.css][3] and [Materlize icons][4]. 
  
```html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
<link href="css/materialize.min.css" type="text/css" rel="stylesheet">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.2/jquery.min.js"></script>
<script src="materialize-paginaiton.min.js"></script>
```

Next invoke the function on your pagination container

```javascript
$('#pagination').materializePagination({ 
    align: 'left',
    lastPage:  10,
    firstPage:  1,
    urlParameter: 'page',
    useUrlParameter: true,
    onClickCallback: function(requestedPage){
        console.log('Requested page is '+ requestedPage);
    }
}); 
```

### Available options
| Attribute       | Type     | Default | Description |
| :-------------: | :------: | :-----: | ----------- |
| align           | string   | 'center'| Pagination alignment within its parent container. Possible options: `center`, `left` and  `right`         |
| lastPage        | int      | 1       | Int value of last page |
| firstPage       | int      | 1       | Int value of first page |
| urlParameter    | string   | 'page'  | The url parameter that indicates which page is currently open e.g. `/?page=2`|
| useUrlParameter | boolean  | true    | If option is set to false, page navigation will not change the url and the  correspondigly the `urlParameter` is ignored |
| onClickCallback | function | {}      | Optional user defined function that is invoked every time a new page is requested i.e clicked. It recives the  `requestedParameter` containing the requested page number   |

[1]: http://materializecss.com/pagination.html
[2]: https://jquery.com/
[3]: http://materializecss.com/getting-started.html
[4]: http://materializecss.com/icons.html

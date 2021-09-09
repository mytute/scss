# SCSS

### content

1. same styles in multiple classes.   
2. BEM naming methodology.    
3. Loop as forEach.   
4. Combinator Selectors.    
5. Themes colors.     

### same styles in multiple classes
```scss
//css
body.shop, body.contact {background-color:#fff;}

//scss
body{
   &.shop, &.contact {
        background-color:#fff;
    }
}
```

### BEM naming methodology.
```scss
//css
.btn {
  &-primary {}
  &-secondary {}
}

//scss
.btn {
  &-primary {}
  &-secondary {}
}
```

### Loop as forEach.
```scss
//css
@charset "UTF-8";
.icon-eye:before {
  display: inline-block;
  font-family: "Icon Font";
  content: "";
  font-size: 12px;
}

.icon-start:before {
  display: inline-block;
  font-family: "Icon Font";
  content: "";
  font-size: 16px;
}

.icon-stop:before {
  display: inline-block;
  font-family: "Icon Font";
  content: "";
  font-size: 10px;
}

//scss
$icons:
  "eye" "\f112" 12px,
  "start" "\f12e" 16px,
  "stop" "\f12f" 10px;

@each $name, $glyph, $size in $icons {
  .icon-#{$name}:before {
    display: inline-block;
    font-family: "Icon Font";
    content: $glyph;
    font-size: $size;
  }
}
```

### Combinator Selectors

```scss
/*
element element 	  div p   	Selects all <p> elements inside <div> elements
element>element   	div > p 	Selects all <p> elements where the parent is a <div> element
element+element   	div + p 	Selects the first <p> element that are placed immediately after <div> elements
element1~element2 	p ~ ul 	  Selects every <ul> element that are preceded by a <p> element
*/

// css
.button > span { }
.button + span { }
.button ~ span { }

//scss (both are ok)
button {
  & > span { }
  & + span { }
  & ~ span { }
}
.button {
  > span { }
  + span { }
  ~ span { }
}
```


### Themes colors.
```scss
.theme-color{
  color: #f44336; // red 	
  color: #e91e63; // pink 	
  color: #9c27b0; // purple 	
  color: #673ab7; // deep-purple 	
  color: #3f51b5; // indigo 	
  color: #2196F3; // blue 	
  color: #87CEEB; // light-blue 	
  color: #00bcd4; // cyan 	
  color: #009688; // teal 	
  color: #4CAF50; // green 	
  color: #8bc34a; // light-green 	
  color: #cddc39; // lime 	
  color: #f0e68; // khaki 	
  color: #ffeb3b; // yellow 	
  color: #ffc107; // amber 	
  color: #ff9800; // orange 	
  color: #ff5722; // deep-orange 	
  color: #607d8b; // blue-grey 	
  color: #795548; // brown 	
  color: #9e9e9; // grey 	
  color: #616161; // dark-grey 	
  color: #000; // black 	
  color: #4CAF50; // mutx
}
```

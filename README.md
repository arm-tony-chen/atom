## Arm Global Web Components - TopNav / SubNav

<br />

### How To Use ###
```
<arm-top-navigation> </arm-top-navigation>
```
<br>
<br>

### Component Attribute ###

**observeId** - Scroll page, observe id and show solid background
```
<arm-top-navigation observeId="#id"> </arm-top-navigation>
```
**subnav** - load top-sub navigation css
```
<arm-top-navigation subnav> </arm-top-navigation>
```
**disabled-subnav** - remove top sub navigation
```
<arm-top-navigation disabled-subnav> </arm-top-navigation>
```
**disabled-subnav-animation** - disable sub nav animation
```
<arm-top-navigation disabled-subnav-animation> </arm-top-navigation>
```
**hide-top-navigation** - hide top navigation
```
<arm-top-navigation observeId="#ancher" subnav hide-top-navigation>
```
**custom-subnav** - Use custom desgin sub nav
```
<arm-top-navigation subnav custom-subnav>
    <span slot="c-subnav">
    <style>
        .custom-subnav-element { color: green; cursor: pointer; padding: 0 12px; }
    </style>
    <div class="custom-subnav-element"> green </div>
    <script>
        var div = document.querySelector('.custom-subnav-element');
        div.addEventListener('click', function(){ console.log('custom-subnav-element')})
    </script>
    </div>
</arm-top-navigation>
```


### Component arguments ###

```
<arm-top-navigation arguments>


|arguments type                         |Description                    |
|---------------------------------------|-------------------------------|
|subnav                                 |Show subnav                    |
|hide-top-navigation                    |hide top navigation            |
|ui-route-disabled                      |disable UI route eventlistender|
```

### Component API ###

```
var element = document.querySelector('arm-top-navigation');


|API Name                               |Description                    |
|---------------------------------------|-------------------------------|
|element.showTopNavigation();           |Show top navigation            |
|element.showTopMainNav();              |Show top main nav              |
|element.showTopSubNav();               |Show top sub nav               |
|element.showTopSubNavWithAnimation();  |Show top sub nav with animation|
|element.hideTopNavigation();           |hide top navigation            |    
|element.hideTopMainNav();              |hide top main nav              |
|element.hideTopSubNav();               |hide top sub nav               |
|element.enableAnimation();             |enable animation               |
|element.disabledAnimation();           |disable animation              |
|element.setSubNavActiveState(index)    |setSubNavActiveState           |
|element.cleanSubNavActiveState()       |cleanSubNavActiveState         |
```

### EventListener ###

```
    document.addEventListener("arm-top-sub-nav-search", function (e) {
        console.log(e.detail);
        var url = "https://www.arm.com/search#q=";
        var url2 = "https://developer.arm.com/search#q=";
        var url3 = "https://www.google.com/search?q=";
        // location.href = url3 + e.detail;
    });

    document.addEventListener("arm-top-sub-link", function(e) {
        console.log(e);
    });

|EventListener Name                     |Description                    |
|---------------------------------------|-------------------------------|
|arm-top-sub-nav-search                 |top sub nav search callback    |
|arm-top-sub-link                       |sub nav link callback          |

```
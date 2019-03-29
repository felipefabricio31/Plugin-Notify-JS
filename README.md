# Check out [notifit 2!](https://github.com/naoxink/notifit-2) :D

notifIt!
=

Notificações simples com o JQuery.

Agora você pode enviar notificações de tudo o que quiser e quando quiser, de maneira simples e rápida.
Fácil de aprender e usar. Personalize com suas cores favoritas, defina o tamanho desejado, defina a opacidade, faça um adesivo e muito mais!

#### De uma chance! [Demo](http://naoxink.ga/notifIt)

#### Intalar via npm
```
npm install notifit-js
```

#### Structure
```
 notifIt
 ├── css
 │   └── notifIt.css
 │   └── notifIt.min.css
 ├── demo.html
 ├── dev
 │   └── notifIt.js
 └── js
     ├── notifIt.js
     └── notifIt.min.js
```

#### Plug
```html
<head>
	<script type='text/javascript' src='js/notifIt.js'></script>
	<link rel='stylesheet' type='text/css' href='css/notifIt.css'>
</head>
```

#### & Play
```javascript
notif({
	msg: "<b>Oops!</b> A wild error appeared!",
	type: "error",
	position: "center"
});
```

## `notif()`

#### Configuration

Variable name|Type|Posible values|Default
---|---|---|---
type|`String`|success, error, warning, info|default
msg|`String`|Message|
position|`String`|left, center, right, bottom|right
width|`Integer`-`String`|Number > 0, 'all'|400
height|`Integer`|Number between 0 and 100|60
autohide|`Boolean`|true, false|true
opacity|`Float`|From 0 to 1|1
multiline|`Boolean`|true, false|false
fade|`Boolean`|true, false|false
bgcolor|`String`|HEX color|#444
color|`String`|HEX color|#EEE
timeout|`Integer`|Miliseconds|5000
zindex|`Integer`|The z-index of the notification|null (ignored)
offset|`Integer`|The offset in pixels from the edge of the screen|0
callback|`Function`|Function|null (ignored),
clickable|`Boolean`|true, false|false
append (dev)|`Boolean`|true, false|false


## `notif_confirm()`
### Description
Now you can ask 'yes' or 'no' easy as --
```javascript
var myCallback = function(choice){
    if(choice){
        notif({
            'type': 'success',
            'msg': 'Yeah!',
            'position': 'center'
        })
    }else{
        notif({
            'type': 'error',
            'msg': ':(',
            'position': 'center'
        })
    }
}

notif_confirm({
	'textaccept': 'Let\'s go!',
	'textcancel': 'I\'ll think about it',
	'message': 'Shall we?',
	'callback': myCallback
})
```

#### Configuração

Variable name|Type|Default|Optional
---|---|---|---
textaccept|`String`|Accept|Yes
textcancel|`String`|Cancel|Yes
message|`String`|Is that what you want to do?|Yes
callback|`Function`|null|Yes
fulllscreen|`Boolean`|false|Yes

#### Response
Funções retornam `true` or `false`
Se o retorno de chamada for passado, ele recebe um parâmetro `true` ou` false`


## `notif_prompt()`
### Description
Ask whatever you want quick and easy
```javascript
var myCallback = function(input_value){
    if(input_value){
        notif({
            'type': 'success',
            'msg': input_value,
            'position': 'center'
        })
    }else{
        notif({
            'type': 'error',
            'msg': 'Empty or cancelled',
            'position': 'center'
        })
    }
}

notif_confirm({
	'textaccept': 'That\'s it!',
	'textcancel': 'I don\'t have a pet :(',
	'message': 'What\'s your pet\'s name?',
	'callback': myCallback
})
```

#### Configuration

Variable name|Type|Default|Optional
---|---|---|---
textaccept|`String`|Accept|Yes
textcancel|`String`|Cancel|Yes
default_value|`String`||Yes
message|`String`|Tell me something|Yes
callback|`Function`|null|Yes
fulllscreen|`Boolean`|false|Yes

#### Response
Se o retorno de chamada for passado, ele recebe um parâmetro com o valor de entrada (se aceito) ou 'falso' (se cancelado)


# More things :)
- [bgfader](https://github.com/naoxink/bgfader)
- [Sublime text color scheme](https://github.com/naoxink/nxk-sublime-color-scheme)
- [asdText](https://github.com/naoxink/asdText)
- [View more](https://github.com/naoxink?tab=repositories)

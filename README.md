# leaflet-control-display
>


## Description
Object to hide or show groups of leaflet controls and to add or remove class-names to the controls container

## Installation
### bower
`bower install https://github.com/FCOO/leaflet-control-display.git --save`

## Demo
http://FCOO.github.io/leaflet-control-display/demo/ 

## Usage
```var myControlDisplay = new L.ControlDisplay( options );```


### options
| Id | Type | Default |
| :--: | :--: | :--- | --- |
| `controlSelector` | string | `".leaflet-control-container .leaflet-control"` | 
| `groups` | array of `controlDisplay` | 	`[`<br>`{id:'zoom', classNames:'leaflet-control-zoom'},`<br>`{id:'attribution', classNames:'leaflet-control-attribution'},`<br>`{id:'scale', classNames:'leaflet-control-scale'},`<br>`{id:'layers', classNames:'leaflet-control-layers'}`<br>`]` |

#### `controlSelector`
The jQuery selector to get all controls

#### `controlDisplay`

    { id, classNames }
	//id = id of the group
	//classNames = class-names to use to select the controls = string of name(s) or array of strings 



### Methods

    .add( id, classNames ): Add the class-names in classNames (string or array) to the group id 
    .hide( id ) //id = string of ids or array of string
	.show( id )	//id = string of ids or array of string:  

	//Special case
	.hide('ALL') / .show('ALL') //Hide/show all controls
	.hide('REST') / .show('REST') //Hide/show all controls not defined in options.groups or added with .add()

	//Alter class-names for container - also for 'ALL' and 'REST'
	.containerAddClass( id, classNames ) //Add classNames to the containers of all controls in group id
	.containerRemoveClass( id, classNames ) //Remove classNames to the containers of all controls in group id

## Copyright and License
This plugin is licensed under the [MIT license](https://github.com/FCOO/leaflet-control-display/LICENSE).

Copyright (c) 2016 [FCOO](https://github.com/FCOO)

## Contact information

Niels Holt nho@fcoo.dk


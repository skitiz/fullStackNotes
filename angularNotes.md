#### Initializing with HTML.
```
<html ng-app>		// directive to start the angular application.
	<body>
		<p>Nothing here {{'yet' + '!'}}</p>		

		/**

		binding denoted by {{ }}, and a simple expression by ' '. The {{ }} is called interpolation.
		AngularJS expressions are evaluated in the context of the current model scope.

		**/

	</body>
</html>
```


#### app.js
```
	// define the angular module.
	var angularModule = angular.module('angularModule', []);

	// define the controller.
	angularModule.controller('sameModuleAsTheOneDefinedInHTML', function sameModuleAsTheOneDefinedInHTML($scope) {
		$scope.variable = [
			{

		},
		{

		},

		];
	});
```

#### angular4 Features
	* ngIf = Support angular if available.
		<span *ngIf = "isavailable; else condition1">Condition</span>
		<ng-template #condition>Condition</ng-template>
	* _as_ keyword in for loops.
	* animation package.
	* ng-template
		depreciates the <template> tag because of naming conflicts with html <template> tag.
	Typescript 2.2
	AngularCLI

You can change the port number AngularJS server number runs on by running : `ng serve --host 0.0.0.0 –port 4205`.

The folder structure is as follows :
	e2e (end to end test folder), node_modules, src.

Karma is used for unit-testing with protractor.

`<app-root>` is the selector in in the `index.html` which is referenced in the `app.component.ts` and will display details on `app.component.html`.


```
import { Component } from '@angular/core';

@Component ({
	selector: 'app-root';
	templateUrl: './app.component.html';
	styleUrls: ['./app.component.css'];
	})

export class AppComponent {
	title = 'Angular 4 Project!';
	days = ['Monday', 'Tuesday', 'Wednesday'];
	isAvailable = true;
	myClickFunction(event){
		alert("Button is clicked.");
		console.log(event);
	}
	changemonths(event) {
		console.log("Changed month from the Dropdown.");
	}
}
```

```
<div>
	<h1>
		Welcome to {{title}}.
	</h1>
</div>

<div>
	<select (change) = "changemonths($event)">
		<option *ngFor="let i of days">{{i}}</option>
		<span *ngIf = "isAvailable">Yes.</span>
	</select>
</div>
<button (click)-"myClickFunction($event)">
	Click me.
</button>
```

Directives in _Angular_ is a __js__ class, which is declared as __@directive__.
	* Component Directives.
		* How components are processed, instantiated and used at runtime.
	* Structural Directives.
		* *ngIf and *ngFor.
	* Attribute Directives.
		* Deals with changing the look and behavior of dom element.

__PIPES__
```
import ( Component ) from '@angular/core';
@Component ({
	selector: `app-root`,
	templateUrl: './app.component.html',
	styleUrls: ['app.component.css']
	})

export class AppComponent {
	title = 'Angular 4 Project!';
}
```

```
<b> {{ title | uppercase }} </b>
```

__Services__ are used to provide functionality all through the page.

__Angular HTTP__ is used to get URL's and show them as JSON's.

__Angular 4 Materials.__

#### Initializing with HTML.
```
<html ng-app>		// directive to start the angular application.
	<body>
		<p>Nothing here {{'yet' + '!'}}</p>		

		/** 

		binding denoted by {{ }}, and a simple expression by ' '
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

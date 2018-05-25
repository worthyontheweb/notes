#Ionic Demo - Worthybob Tab

##tab-worthybob.html
<ion-view view-title="Worthybob">
  <ion-content class="padding">
    <h2>WHAT'S A WORTHYBOB?</h2>
<p class ="wotw">Worthybob {{worthybobchoice}}</p>
<ion-list>
 <!-- <ion-item ng-repeat="w in worthybob">{{w}}</ion-item>-->
</ion-list>
<div ng-click="refreshInfo()">try again</div>
  </ion-content>
</ion-view>

##worthybob code from controllers.js
//Claire's Worthybob Tab
.controller('WorthybobCtrl', function($scope) {

  var worthybob = ["wears hoodies","builds websites","talks a lot","is learning app development", "is writing a quiz"];
  $scope.worthybob = worthybob;
  $scope.refreshInfo = function refreshInfo() {
    console.log("refreshing info");
    $scope.worthybobchoice=$scope.worthybob[Math.floor(Math.random()*$scope.worthybob.length)];
  }
  $scope.refreshInfo();

})


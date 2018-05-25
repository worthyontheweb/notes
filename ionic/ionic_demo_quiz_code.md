#Claire's Demo Quiz

##tab-quiz.html
<ion-view view-title="Quiz">
  <ion-content class="padding">
    <h2>Claire's 1st Demo Quiz?</h2>
<!--<p>Worthybob {{worthybobchoice}}</p>
<ion-list>
  <ion-item ng-repeat="w in worthybob">{{w}}</ion-item>
</ion-list>
<div ng-click="refreshInfo()">try again</div>-->
<p>General text describing the quiz and giving people information and instructions. </p>
        <ion-list>
            <ion-item ng-repeat="question in questions" ng-show="$index===questionNumber">{{question.question}}
                <ion-item ng-repeat="(label,answer) in question.answers" ng-click="setAnswerChoice(label)" ng-class="{'selected': answerChoice === label}">
                    <button class="button full large" style="clear:both;display:inline-block;" >
                     
                        <span style="padding:10px; border:1px solid black;">{{label}}</span>{{answer}}
                    </button>
                </ion-item>
                
            </ion-item>
        </ion-list>
        <div class="button" ng-click="nextQuestion()" ng-show="questionNumber<questions.length">Next</div>
        <div ng-show="questionNumber===questions.length">You scored {{quizScore}} out of {{questions.length}}</div>
        
     </ion-content>
</ion-view>


##controllers.js quiz code
//Claire's Quiz 2018-05-24 13:55:45


.controller('QuizCtrl', function($scope) {
  $scope.quizScore = 0;
 var quizStuff = [
   {
     "question": "This is the first question?",
     "answers": {
       "a":" no it's not",
       "b":" nah, it isn't",
       "c":" yes it is"
     },
     "correctAnswer": "c"
   },
   {
    "question": "This is the first second question?",
    "answers": {
      "a":" yes it is ",
      "b":" nah, it isn't",
      "c":" nope"
    },
    "correctAnswer": "a"
  },
  {
    "question": "This is the third question?",
    "answers": {
      "a":" no it's not",
      "b":" yep",
      "c":" nah it isn't"
    },
    "correctAnswer": "b"
  }
 ];

  $scope.questions = quizStuff;
  
  var questionNumber = 0;

  $scope.userChoice = "";
  $scope.questionNumber = 0;

  //$scope.currentQuestion = quizStuff[ questionNumber ];

 $scope.setAnswerChoice=function setAnswerChoice(answerChoice) {
   console.log("setAnswerChoice called with ",answerChoice);
   $scope.answerChoice = answerChoice;
 }

 $scope.nextQuestion = function() {
   console.log("next!");

   // score the answer
   console.log("guess,correct =",$scope.answerChoice,$scope.questions[$scope.questionNumber].correctAnswer);
   if( $scope.answerChoice === $scope.questions[$scope.questionNumber].correctAnswer){
     $scope.quizScore++;
   }
   $scope.questionNumber++;   
   console.log("updating score ", $scope.quizScore);

   $scope.answerChoice = "";
 }


 $scope.checkAnswer = function() {

 }


})
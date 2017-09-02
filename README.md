# Knop in angular2 ionic3

## 1st- solution [ng-knob2](https://github.com/RadMie/ng-knob/issues/9#issuecomment-245337327)
      
  * lates update of *ng-knob2* not support angular 4 and ionic3 also not support D3 version 4, the functions they are using in the D3 not exist any more .
  * to make it run correctly with Angular4 and D3 version 4 check these commits [1st ng-knob2 fix](https://github.com/almgwary/knob-angular-2-ionic-3/commit/5e94659f3c45d1eb7459982cb1340bd680015cd0) -  [2nd fix run the component](https://github.com/almgwary/knob-angular-2-ionic-3/commit/aec2bda98662fa08b8eca6409f451a4beca7e778)
  * after fix it show small compoent in the page but still it have issues .
  * [example screen shot from home page](https://raw.githubusercontent.com/almgwary/knob-angular-2-ionic-3/master/s1.PNG)



## 2dn- solution [jQuery-Knob](https://github.com/aterrien/jQuery-Knob)

  * it works check  [ this screen shot from list page ](https://raw.githubusercontent.com/almgwary/knob-angular-2-ionic-3/master/s2.PNG) ;
  * we can use jquery with anuglar2 but we have to handel data binidg manullay 
  * any change in the JQ will affect the angular modle by this function 
           
                    $(element).knob({
                      'change' :  ()=> {
                        // this is JQ call back to update angular model
                        this.value = element.value
                      }
                    });
                    
  * any change in angular value should trigger change on JQ element 
  
  
                    
                    var newValue = this.value ;
                    $(element)
                      .val(newValue)
                      .trigger('change');
             
             
             
# Screen shots

<img src="https://raw.githubusercontent.com/almgwary/knob-angular-2-ionic-3/master/s2.PNG" width=30%>
<img src="https://raw.githubusercontent.com/almgwary/knob-angular-2-ionic-3/master/s1.PNG" width=30%>

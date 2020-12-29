# clickOnButtonWithJavaScriptADF
oracle adf, how to click on a button with javascript

1-- the button in the region must have the property clientComponent="true"
2-- on the javascript on the main page.  AdfPage.PAGE.findComponentByAbsoluteId('r1:btn') , the id of the component must be in the form of id of region "r1" and ":" and then 
    the id of the button "btn"
3-- the below code is the code that trigger the action on the button 
        var actionEvent = new AdfActionEvent(searchBtn);
         
          actionEvent.forceFullSubmit();
          actionEvent.noResponseExpected();
          actionEvent.queue(false);
          
if you add forceFullSubmit then it would submit the page if you dont add it, then it is a partial submit ( not refresh the whole page)

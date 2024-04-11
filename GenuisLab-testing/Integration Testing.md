**Integration Testing** :
> Literally taking the unit tested module one by one and test the behavior ad a combined unit 

>main focus is to test the interfaces btw units/modules  + checking the combination of  behaviors and validate whether the requirements have been implemented correctly or Nah Uh 

>normally done after unit testing 

>we start integrating them one by one until all modules are integrated 

## Why Integration Testing ? :
* In real world based application , due to good practices the app is broken down into several smaller modules and each developer is assigned one module to work on for instance  , humans are different from one another -> it's important to check that the logic given by each developer matches the expectations and rendering the correct value in accordance with the prescribed standards 
* To check that everything is in harmony together 
* there's third parties  that modules interact with --> necessity of checking that the data accepted by them is correct and that the response generated is also as expected 
* frequent requirement change : sometimes a developer deploys something without unit testing here integration testing becomes important
### In our app : 
let say a parent will see the different offers that a whole functionality and paying for a class is a total different thing these two modules shall be connected by the end , that where come our role to make it happen seamlessly
## When to begin : 
*Once the module is Done .*

## Types :
#### Big Bang Approach :
* good for small systems / bad for salable ones 
#### Bottom-up Approach  :
from lowest modules to ----> upper modules 
* easy to detect small problems before they get tricky 
* the main program does not exist till all modules are integrated and tested all together -> the higher lvl design flaws will be detected only at the end
#### Top-Down Approach :
the opposite
* at first only top modules is unit tested in isolation then we integrate the lower modules one by one 
### Things to be aware of : 
* this test is not done by the end of the cycle , it's conducted simultaneously with the development 

### Collapsing with Github Actions :
* finding ways to do these automatically on repeated parts etc ...
## Planning :
1. Prepare integration test plan 
2. prepare integration test scenarios , test cases
3. prepare test automation scripts
4. execute text cases
5. Report the defects
6. track and re-test the defects
7. re-resting testing goes on until integration testing is complete 
PS: this needs more research these two are hella important from beginning


#### *Gray box testing : testers have partial knowledge of the internal structure or code of an application*

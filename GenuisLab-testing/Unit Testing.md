**Unit testing :**
unit testing is the process of testing small portions of software application called units without relying on third party systems
any component that interacts with external database , file etc.. cannot be checked as a  part of unit testing as that unit tests are testing on isolated components during the primarily stages of development phase


Let say achraf and aymane made a new functionality 

* the moment they do it a test is integrated to check if it's working or not 
* it's crucial since the start 
* write tests during development not after it 
### Unit Testing Techniques :
it's carried out with the help of three testing techniques :
#### Structural technique :
* examine the structure of a program also known as **White Box** (litteraly seeing the code and trying to see if there;s some issues )
* developers typically do it 
* necessite a thorough understanding of the code 
* more about how it is accomplished rather than how it's functionning 
#### Functional Testing Techniques :
* checking functionality of features 
* compared to what we aim to have and suggest things if needed 
* tests are carried out by supplying sample inputs 
#### Error Based Techniques :
* by checking previous test data and checking what failed
* changing statements to check eventually what failed 
* fault seeding techniques L introduce problems into the code and test them untill all of them are identified 
### Good practices while writing unit tests 
* using ***parametarized tests*** help on writing and managing unit tests faster by using the same test on different places , -> ->->less redundency and code duplication 
* Unitphp dependency , Nodejs Mocha - jest - jasmine 
* in test don't use reasoning : 
  using logical conditition and manual string concatenation in unit tests increases  the likelihood of defect in your test suite 
  instead of focusing on the implementation specifics , test should focus on the intended results 
* avoid test interdependencies :
  each test case should have its own setup and takedown procedure without depending on another test 

### Questions :
* how to automate these tests :
*like if we have some sort of functions that is repeated how can we detect it and pass the exact test on it ?*


### Collapsing with Devops :
one of the good practices in devops philosophy is TDD which is test driven developement 


here we don't write the code first and then we test , instead test cases are written to outline and evaluate how the code will perfom (specially when we have an already existing code base and even if we don't) before making changes we test first to check what is the internded output and what does the test give us as an output and then how can we change the test to allign with the intended output that the test shall give


## things to question : 
Gorrila testing 
php and unit testing 
(mainly questionning them to be understood this week inshallah )


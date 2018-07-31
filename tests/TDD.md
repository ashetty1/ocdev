## Test Driven Development (TDD) for ODO

What’s TDD?  In simple terms, WRITE TESTS FIRST

#### TDD Workflow

Under TDD workflow, we write tests before writing feature code
The tests written will serve as a blueprint for writing feature code

1. Add a test
1. Run all tests and see if the new test fails
1. Write the code
1. Run tests
1. Rewrite code incorporating any changes, and add new tests

#### Purpose

1. Writing tests before implementing the functionality will enable us to write tests covering more scenarios
1. A feature with a good set of cases is also the most robust, thereby helping us improve the quality of the product
1. Would help us address the test coverage backlog we have


#### What kind of tests?

1. Phase 1: Unit tests will be our primary focus. 
1. Phase 2: Once we get comfortable with the process, we will work on incorporating e2e tests into this workflow.


#### TDD process for ODO

1. Write tests for every feature/bug fix before implementing the code. 

	* Developer will split the assigned task into small achievable subtasks
	* Each subtask will require unit tests to be written before feature implementation
	* Open work-in-progress [WIP] PR with the tests written
	
1. The tests should cover both positive and negative scenarios:
	* It would be good to have all permutations and combinations covered *as much as possible* helping us cover the boundary cases
	* There is always scope to add  more tests could be added once the feature has been fully implemented
	
1. Write feature code and run tests:
	* Feature code should be pushed to the same WIP test PR
	* Feature code should pushed only after pushing the unit tests
	* After the feature code is pushed, the test should pass
	
1. Review process
	* Ensure that PR with code change is accompanied by unit tests
	* Travis checks to be our point of determination

#### What does following TDD process involve

1. Reversing the process which we currently follow, i.e writing tests after writing the feature
1. We should treat tests as something that will help us gauge end-user interaction and product behaviour



#### FAQs
1. ##### Won't TDD slow down our development process?
 
   Initially we might feel that way, but over time, we will realise the advantage this would bring to our development process by reducing the bugs, improving test coverage and the development time spent in fixing regression bugs.  TDD will help us treat test development as an independent process and an essential prerequisite in our development process.

1. ##### What if we don’t know what a feature would finally look like

    Nothing prevents a developer from running the tests against his proof of concept code on his local setup before pushing the PR with tests.

1. ##### Writing tests based on a feature is easier.

    Writing tests beforehand (under TDD) would help us identify the design limitations and corner cases in advance. Writing tests post development often limits us to cover positive cases. TDD will help us move away from that mindset.

1. ##### Can we follow the same process for big features too?

    Tasks involving big features should be split into numerous simple and achievable subtasks, and each of those subtasks should have test coverage. 

1. ##### Are unit tests mandatory under TDD?
  
    Unit tests are key to TDD process. We will have unit tests (using fake client) as a mandatory requirement to PR review/acceptance.

1. ##### Should tests always be written first? 

    That’s the point. In order to follow TDD process, we need to look at feature development from a testing perspective. It will help us cover wider scenarios beyond the positive scenarios. Tests will also serve as good validator during the coding process.

 







**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#2 – Requirements-Based Test Generation**

| Group \#:      | 16  |
| -------------- | --- |
| Student Names: | Ethan Winters    |
|                | Carter Marcelo   |
|                | Karim Mansour    |
|                | Jason Pang       |

# 1 Introduction

With large software applications being complex and heavy with various methods, testing such an application must be done with efficiency and proper planning in mind. The use of various testing tools and methods is very important to avoid wasting time on irrelevant or repetitive testing. This lab demonstrates the work that can be done to ensure these faults are avoided and that the software application under test can be tested faster and more effectively. 

# 2 Detailed description of unit test strategy

The strategy our group adopted for testing involved various instances of equivalence testing, such as the tests performed on Row and Column total calculations. These tests included cases such as normal operations and the boundary cases where things may or are expected to go wrong. An example of this is the use of the two tests testCalculateColumnTotalThreeRows() and TestCalculateColumnTotalZeroForInvalidColumns(). Here, the first test works with normal, expected values for the number of columns while the second works with an invalid case that should throw an error. This ensures proper operation and handling of incorrect values. 

Of the test cases we’ve designed, there are several main classes we’ve worked with. The first being Rows, where the tests are partitioned into 2 major partitions, being expected and unexpected values. These partitions are tested with one test each, being the calculation of a row total with 3 rows and a total with an invalid number of rows. The parameter exception for Rows is also tested to ensure proper error handling is operational. The same is repeated for the columns class, which tests the same partitions of itself. 

The next class that was tested was the Range class, where boundary value analysis is heavily utilized. This can be seen in the getUpperBoundTest() and getLowerBoundTest() tests, where the boundaries of the range are tested to ensure they are properly handled by the system. 

A number of these tests use mocking, with the mock objects created in the @Before areas of the test suite. This presented benefits for the testing since object-oriented tests can now be done on actual objects to show the results of the test. Using mock objects that are constructed outside the tests themselves allow for the simulation of real system operation, making the tests much more accurate. There can be challenges to using mock objects as well, and these include the use of one object for multiple tests. To avoid errors in the order of tests performed on the object, you must ensure that your tests occur in the correct order. The downside to this is that if one test fails, the rest after it may fail due to an error in the mock object’s data. This can be prevented by a different object for each test, though this makes sequential operations rather challenging to test. 

# 3 Test cases developed

DataUtilitiesTest.java:

testCalculateColunmTotalThreeRows() 
// This test covers the Columns-Expected Partition of the Columns Equivalence Class

testCalculateRowTotalCols()
// This test covers the Rows-Expected Partition of the Rows Equivalence Class

testCalcuateColumnTotalZeroForInvalidColumns()
// this test covers the Columns-Unexpected Partition of the Columns Equivalence Class

testCalculateRowTotalZeroForInvalidRows()
// this test covers the Rows-Invalid Partition of the Rows Equivalence Class

testCalculateRowTotalThrowsInvalidParameterException()
// this test covers the Rows-Invalid Partition of the Rows Equivalence Class

testCreateNumberArray()
// this test covers the single partition of the Array Equivalence Class

RangeTest.java:

getCentralValueTest()
// this test covers the span partition of the Range Equivalence Class

getLengthTest()
// this test covers the span partition of the Range Equivalence Class

getLowerBoundTest()
// this test covers the size partition of the Range Equivalence Class

getUpperBoundTest()
// this test covers the size partition of the Range Equivalence Class

equalsTest()
// this test is stand alone

toStringTest()
// this test is stand alone

# 4 How the team work/effort was divided and managed

The work division in this lab was based off all the required work rather than just the tests themselves. This involved distributing the individual tests and lab report among the four group members. While some of us worked more on the tests themselves, others focused more on the documentation and lab report. This lab highlighted the importance of proper documentation of who is required to complete which work items to avoid confusion and misunderstandings as well as preventing time wasted on duplicate or irrelevant work.

# 5 Difficulties encountered, challenges overcome, and lessons learned

Throughout this lab, communication proved somewhat challenging while doing the tests. Working over the discord to confirm who was doing / had done what became challenging when others were not available. To work around this, group members requested instead that you check the GitHub before doing any tests to see which were already done, since some were somewhat related to others. Overcoming collaboration challenges was done throughout this lab by holding regular meetings to ensure that everyone was balancing the work accordingly and that everything would be completed on time.

# 6 Comments/feedback on the lab itself

This lab document proved very effective at teaching the concepts of using Junit to analyze a system under test to ensure all operations work as intended. The use of various testing strategies and plans such as equivalence classes worked very well for ensuring efficient tests were constructed. Boundary value tests were also highly effective at testing a wide range of values. Overall, this lab document showcased new and effective ways to practise testing, enhancing our understandings of testing even more so. 
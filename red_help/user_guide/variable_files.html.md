## local Python variable files to deal with missing variables

In some test environments, Robot specific enviroments variables are used in
test cases or injected as arguments to Robot test runner.  
RED is not aware of such usage thus those variables will be marked as unknown,
error marker will be placed.  
In order to include variable name validation without changing test suites,
user can create local Python file with list of variable names inside.  
Such file can be included in RED.xml under Variable files section thus making
RED aware of previously unknown variables.  
Variables from such file will be visible as Global variables for all Robot
files inside Project.  
Below is a sample body of such python variable file (examples can be also
found in RobotFramework official manual and Python examples).  
`  
#!python  
  
#Sample variables and values  
Scalar = 'value'  
UserList = ['value1','value2']  
UserDict ={'key1':'value1', 'key2':'value2'}  
`


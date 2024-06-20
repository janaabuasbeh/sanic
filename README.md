# Report for Assignment 1

## Sanic


Name: Group 102

URL: https://github.com/janaabuasbeh/sanic102 

Number of lines of code and the tool used to count it: 

The tool that we used is Lizard which was obtained from the gitbook. The tool “pip install lizard” was used to download Lizard and then “python lizard.py” was executed. The number of lines of code is 50156 nLOC which can be represented as 50.156 KLOC.




Programming language: Python 









## Coverage measurement

### Existing tool

The existing tool that was used for the coverage measurement is Coverage.py which was provided in the gitbook. To execute the tool, we implemented “pip install coverage”. Based on that we either used the command “python -m coverage run -m pytest” for windows and “coverage run -m pytest” for mac which ran the coverage. We also added the modules required to run it such as “pip install sanic” and other required modules. Based on that, “python -m coverage report” was used to generate the report and it was exported as an html via “python -m coverage html”.











### Your own coverage tool
Group member name: Medon Abraham 

Function 1 name:  def _poll_monitor(self) -> Optional[MonitorCycle]:

Function Coverage Before Instrumentation: 



Overview of uncovered lines:






Function Instrumentation:




Tests:















































Coverage after tests:





## Coverage improvement: 39%





Function 2 name: def ack(self) -> None:

Function Coverage Before Instrumentation: 


Overview of uncovered lines:



Function Instrumentation:



Tests:



Coverage after tests:




## Coverage improvement: 50%






Group Member Name: Jana Salah Mohammad Ali Abuasbeh

Function 1 Name: def unregister_app(cls, app: Sanic) -> None:

Function Coverage Before Instrumentation: 


Overview of uncovered lines:




Function Instrumentation:



Tests: 


Coverage after tests:



## Coverage improvement: 33%

Reason: The test cases now account for situations where the app is not an instance of a Sanic app, and presents two test cases where the name of the app is in the registry and not in it.

Function 2 Name: async def validate_file(request_headers: Header, last_modified: Union[datetime, float, int]) -> Optional[HTTPResponse]:

Function Coverage before instrumentation:



Overview of Uncovered Lines:





















Function after Instrumentation:








### Individual tests

 




Coverage after Tests:



## Coverage improvement:
25% improvement, from 75% to 100%

Elaboration:
By adding tests that account for every alternative, as in the “last-modified” variable and the “if_modified_since” variable take turns having invalid, valid, and naive input, all the branches’ conditions are met by some test, and so the coverage is increased to 100%





Group Member Name: Ayush Khadka


Function 1 Name: def _extract_style(maybe_style: Optional[str], name: str) -> str:

Function Coverage Before Instrumentation: 



Overview of uncovered lines:


Function Instrumentation:




The coverage result outputted by the instrumentation is 

Tests 1:




<Provide a screenshot of the old coverage results >

<Provide a screenshot of the new coverage results>


<State the ## Coverage improvement with a number and elaborate on why the coverage is improved>

The improvement went from 40% to 100% which is an increase of 60%. The reason why the coverage has improved is because of 













Function 2 Name:  def __eq__(self, other):

Function Coverage Before Instrumentation: 


Overview of uncovered lines:



Function Instrumentation:


### Individual tests





<Provide a screenshot of the old coverage results >


<Provide a screenshot of the new coverage results>



<State the ## Coverage improvement with a number and elaborate on why the coverage is improved>

The improvement went from 69% to 100% which is an improvement of 31%. The reason why the coverage has improved is because 






Group member name :  Amirreza Darabi

Function 1 name :    def refresh(self,passthru: Optional[Dict[str, Any]] = None,) -> Sanic:


Function Coverage Before Instrumentation: 



Overview of uncovered lines:
















Function Instrumentation:





Function Coverage after instrumentation:



### Individual tests







coverage after tests:




## Coverage improvement:

The coverage increased  26%, from 71% to 97% after the instrumentation and enhancing the tests in the test file.


Elaboration:
In the overview of uncovered lines it can be seen that three if statements are not covered, the reason was that their condition was never true. In the improved test functions, these functions :
 “if self is not registered:”
“if not registered.state.server_info:” 
“if hasattr(self, "multiplexer"):” 
 are sets to be true, hence the coverage percentage is increased to 97%. 




Function 2 name :    def purge_tasks(self) -> None:

Function Coverage before instrumentation:



Overview of Uncovered Lines:



Function after Instrumentation:



Function Coverage after instrumentation:






### Individual tests



coverage after tests:




## Coverage improvement:

The coverage increased  21%, from 79% to 100% after the instrumentation and enhancing the tests in the test file.

Elaboration:
As it can be seen in the uncovered lines, the first if condition is never true and the second if condition is always true, the enhanced tests are designed in the way that all possible ways are covered and both of the following conditions are set to true and false:

“if task is None:”
“if task.done() or task.cancelled():” 






### Overall

<Provide a screenshot of the old coverage results by running an existing tool (the same as you already showed above)>


<Provide a screenshot of the new coverage results by running the existing tool using all test modifications made by the group>


## Statement of individual contributions

Amir: 

Ayush: I did smth

Jana:

Medon




how do you read envvars from your host OS in a springboot applicaiton (similar to is it possible to assign values to properties from the environment in your application.properties/yml file)?
>>
api.key=${API_KEY:not set}

how do u handle an error condition while invoking or accessing a Stored procedure from your java applicaiton?
>>Ideally stored proc shouldnt run into exception or error; It can at max return and err code + err description.
In worst case it does fail just catch SQLException and return some user friendly error msg.

During a Get operation on say a Hashmap - what happens behind the scenes?
>>When u store an object, the hashcode meth gets called to Calculate a bucket location. If there is already an object there it wud then add one more entry by creating a linked list. So when trying to get the object back the Map.entry is evaluated by using the equals() method to see if the key object is contained or not. If it does its easy on performance you get the object else there is collision.

How do u create a thread-safe Singleton in Java?
>>
public enum Singleton{
    INSTANCE;
 
    public void show(){
        System.out.println("Singleton using Enum in Java");
    }
}

//You can access this Singleton as Singleton.INSTANCE and call any method like below
Singleton.INSTANCE.show();


When do u go for composition (and when do u go for aggregation or association)?
>>car is composed of tyres,doors, steering where the whole may control the direct responsibility of its constituent parts lifecycle. For eg what use is door or steering independent of the car.

Different ways to communicate b/w modules of your NG applicaiton using core NG functionality
Mainly 3 ways:-
>>using services, events

>>Directly b/w Controllers using controllerAs or other forms of inheritance $parent,$child, $$nextSibling etc

>>By assigning models on $rootScope

what is the speciality of threadLocal variable?
>>The Java ThreadLocal class enables you to create variables that can only be read and written by the same thread.

how many ways to iterate a collection such as list
>> using normal for loop

>> using iterator

>>Enchanced For loop: for (String aName : listNames) {
    System.out.println(aName);
}

>>forEach Method with Lambda Expressions
listNames.forEach(name -> System.out.println(name));

How do u test your Angular app? 
>>By using Protractor and any other f/w such as Mocha, Chai & Karma etc..

How do u come up with Lines of Code for a file say app.ts?
>>using lcov code coverage tool

when doing a Join such that first table should include all rows whereas second table can have Null
>>Left join on condition AND "filter_criteria"

    SELECT c.Customer, c.State, e.Entry
    FROM Customer c
    LEFT JOIN Entry e
        ON c.Customer=e.Customer
        AND e.Category='D'

How do u check connection leak to your OraDB?
>>
                    "SELECT COUNT(*) " /
                    "FROM pg_stat_activity " /
                    "WHERE state ILIKE '%idle%'"
                    
 
Why String needs to be immutable in Java?
What is a lambda expression? 
File handling using try with resources specifically stream closure

 	You have an object array . Assume that each object has got properties like name and emailId. Sort the list of objects using comparators 
 	Remove all objects from the array which has an invalid email not in the format xyz@gmail.com using the .fiIter() function on streams 
 	Retrieve a list of unique names from the array — using .map() function
 	Transform the list of user object list to another type of objects both objects have the same properties but different attributes
 	Find unique objects in a list if objects say every object has username and date_of_birth.  How to ensure that the list does not contain any duplicates?

What is a functional interface? Can you explain with an example why it is used
Can you explain how you can pass list of objects to a method as method argument?

Thread Lifecycle, 
Diff b/w wait and sleep (or when is InterruptedException thrown)? .
 
In java can a dead thread be reinstated or brought back into new / running state?

How to consume a REST endpoint  i.e.  invoke/call from java or Spring-boot app (reactive way) - https://stackoverflow.com/questions/3913502/restful-call-in-java
Multiple RESTful calls parallelly: https://stackoverflow.com/questions/50345971/how-to-call-multiple-rest-api-parallel-in-java 
(Scenario based question : Need to pull 1000’s of msgs using a single Facebook rest endpoint and insert into DB. Note that order of the actuals msgs is not important at the time of insertion. 
How to invoke a REST api base on Executor service & perform bulk insert into DB using Batch queries

                    

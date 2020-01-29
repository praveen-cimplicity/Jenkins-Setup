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
                    
                    
                    

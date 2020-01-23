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
                    
                    
                    

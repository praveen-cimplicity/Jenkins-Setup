Different ways to communicate b/w modules of your NG applicaiton using core NG functionality
Mainly 3 ways:-
>>using services, events

>>Directly b/w Controllers using controllerAs or other forms of inheritance $parent,$child, $$nextSibling etc

>>By assigning models on $rootScope

what is the speciality of threadLocal variable?
>>The Java ThreadLocal class enables you to create variables that can only be read and written by the same thread.

How do u test your Angular app? 
>>By using Protractor and any other f/w such as Mocha, Chai & Karma etc..

How do u come up with Lines of Code for a file say app.ts?
>>using lcov code coverage tool

How do u check connection leak to your OraDB?
>>
                    "SELECT COUNT(*) " /
                    "FROM pg_stat_activity " /
                    "WHERE state ILIKE '%idle%'"
                    
                    
                    

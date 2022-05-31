# employeeManage

### An employee management application made by spring boot, angular and mySQL

1. Built basic MVC model by spring boot 2.6.7 with maven dependencies.
2. Tested Restful API GET, POST with postman and httpie.
3. Developed frontend by Angular 13.3.9 and typescript.


### Prerequisites

1. Java version 11
2. Node 16.13.2 / npm 8.10.0
3. Spring boot 2.6.7
4. Angular CLI 13.3.6 / Angular 13.3.9
5. mySQL v8.0.28
6. Postman Version 9.15.10
7. IntelliJ IDEA

### Spring boot project by IntelliJ IDEA

```
|- src
  |- main
    |- java
      |- com.company.employeemanager
        |- exception
          |- UserNotFoundException
        |- model
          |- Employee
        |- repo
          |- EmployeeRepo
        |- service
          |- EmployeeService
        |- EmployeemanagerApplication
        |- EmployeeResource
```

### If mySQL access denied for user 'root'@'localhost' mac
1. Change directory location: ```cd /usr/local/mysql/bin```
2. ```./mysql -u root -p```

### Test API GET, POST request
1. postman

<img width="853" alt="image" src="https://user-images.githubusercontent.com/39740066/170165628-15571f87-aab1-4216-8d2b-a5f2b9908980.png">

2. [httpie](https://httpie.io/cli)

<img width="777" alt="image" src="https://user-images.githubusercontent.com/39740066/170165702-34d1ee73-9aef-45ca-9cb5-057acafabfec.png">


### Angular cli
1. Install angular cli : ```npm install -g @angular/cli```
2. Create and build angular project : ```ng new employeemanagerapp```
3. Run project server : ```ng serve``` 

### Angular generate service
```
ng generate service employee --skipTests=true
```
[CLI Command Reference](https://angular.io/cli/generate#service-command)

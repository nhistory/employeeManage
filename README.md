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

### CORS(Cross-Origin Resource Sharing) configuration

Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources. CORS also relies on a mechanism by which browsers make a "preflight" request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.

<img width="536" alt="image" src="https://user-images.githubusercontent.com/39740066/171336103-e0103a87-d2b6-46c4-a6df-db15227ac2eb.png">


```Java
@Bean
	public CorsFilter corsFilter() {
		CorsConfiguration corsConfiguration = new CorsConfiguration();
		corsConfiguration.setAllowCredentials(true);
		corsConfiguration.setAllowedOrigins(Arrays.asList("http://localhost:4200"));
		corsConfiguration.setAllowedHeaders(Arrays.asList("Origin", "Access-Control-Allow-Origin", "Content-Type",
				"Accept", "Authorization", "Origin, Accept", "X-Requested-With",
				"Access-Control-Request-Method", "Access-Control-Request-Headers"));
		corsConfiguration.setExposedHeaders(Arrays.asList("Origin", "Content-Type", "Accept", "Authorization",
				"Access-Control-Allow-Origin", "Access-Control-Allow-Origin", "Access-Control-Allow-Credentials"));
		corsConfiguration.setAllowedMethods(Arrays.asList("GET", "POST", "PUT", "DELETE", "OPTIONS"));
		UrlBasedCorsConfigurationSource urlBasedCorsConfigurationSource = new UrlBasedCorsConfigurationSource();
		urlBasedCorsConfigurationSource.registerCorsConfiguration("/**", corsConfiguration);
		return new CorsFilter(urlBasedCorsConfigurationSource);
	}
```




## Reference
- https://www.youtube.com/watch?v=Gx4iBLKLVHk&t=437s
- https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

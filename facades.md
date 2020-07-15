# Facade Pattern
Es un tipo de objeto que se le puede pasar a una vista. Básicamente implementa el patrón `facade`, en donde se ofrece una interfaz limitada y simplificada a un conjunto de dependencias.

Se pueden implementar usando `Struct`s.

Se pueden construir directamente desde el controlador si es sencillo o bien puede ser el resultado de un action/service/interactor

### Naming
Idealmente deben llamarse como la vista o parcial en la cual se va a usar, o bien si no es para una vista con un nombre ad hoc.

`BookingsController::IndexFacade`

### Recursos
- [https://blog.appsignal.com/2020/03/18/facade-pattern-in-rails-for-performance-and-maintainability.html](https://blog.appsignal.com/2020/03/18/facade-pattern-in-rails-for-performance-and-maintainability.html)
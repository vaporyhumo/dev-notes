# Factory Pattern
Es un patrón que crea una instancia o un conjunto de instancias de objetos para un contexto dado.

Usualmente se usa para crear objetos de `ActiveRecord`, y pueden persistirse o no.

Si implementa un método `.build` o métodos `.build_*` devolverá uno o varios objetos no persistidos.
Si implementa un método `.create` o métodos `.create_*` devolverá uno o varios objetos persistidos.

### Naming
Por ejemplo si creamos un `TicketCancellation` a partir de un `Ticket` cuando lo cancelamos, podemos tener una fáctory como `TicketCancellation::BuildTicket` o `...::CreateTicket` o `...::TicketFactory`.

### Implementación
Se pueden implementar como servicios en el caso de que usen solo build o solo create. [[services]].
Se puede implementar como módulo para la clase de objetos que crea o construye.

Todos sus métodos tienen que devolver instancias o colecciones de objetos nuevamente creados; pudiendo o no estar persistidos.

Si no se implementa como servicio, sus métodos deben exclusivamente ser:
- `.build`
- `.create`
- de la forma `.build_*`
- de la forma `.create_*`
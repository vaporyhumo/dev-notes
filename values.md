# Value Objects
Son pequeños objetos que principalmente almacenan data; si tienen métodos, suelen ser de presentación.
La igualdad de estos objetos viene dada  por el valor de sus atributos y no por la identidad del objetos; esta es una diferencia que tienen con los entity objects.
Se considera una buena práctica hacerlos inmutables.

Se suele implementar `Comparable` y/o `Enumerable` en los value objects. Esto se hace implementando `#<=>(other)` e `#each` respectivamente.

Un `Struct` viene muy bien para implementarlos.

### Examples
```ruby
DateRange   = Struct.new(:start_date, :end_date)
Address     = Struct.new(:city, :street)
Temperature = Struct.new(:value, :unit)
Money       = Struct.new(:fractional, :currency)
```
# Decorators
Los decorators son objetos que extienden a otro objeto. Se usan para acomodar un objeto a un contexto específico mediante extensiones ad hoc.

Un ejemplo sencillo sería este:
```ruby
class IntegerDecorator
  def initialize(integer)
    @integer = integer
  end

  def sum_1
    @integer + 1
  end
end

2.sum_1
=> NoMethodError

a = IntegerDecorator.new(2)
a.sum_1
=> 3
```

También se pueden implementar usando `SimpleDelegator` o bien la gema `draper`.
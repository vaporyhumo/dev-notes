# Rails Routes
Para poder separar las rutas en varios archivos, se puede agregar esta configuración en `application.rb`:
```ruby
config.paths['config/routes.rb']  =  Dir[Rails.root.join('config/routes/*.rb')]
```	
Entonces en vez de usar `config/routes.rb` usamos `config/routes/*.rb`para serparar las rutas en namespaces o recursos.

### Recursos
- [Keep your routes clean](https://medium.com/rubycademy/how-to-keep-your-routes-clean-in-ruby-on-rails-f7cf348ec13b).
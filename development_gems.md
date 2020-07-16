# Development gems
Gemas para mejorar la productividad y calidad del desarrollo en ruby.

## Performance
Gemas que te ayudan a mejorar la performance de la aplicación.

#### [bullet](https://github.com/flyerhzm/bullet)
Whatch rails queries for N+1 and the likes. 

## Code Quality
Gemas que ayudan a mejorar la calidad del código en general.

### rubocop
General linting.

##### Using `--auto-gen-config`
Para empezar a trabajar con rubocop en un proyecto legacy o para cambios de configuración, usamos la opcion `--auto-gen-config` para generar un archivo TODO: `.rubocop_todo.yml`, que desactiva los cops ya existentes, generando una lista de cops que se deben arreglar para ajustarse a las nuevas configuraciones.

```sh
bin/rubocop --auto-gen-config --auto-gen-only-exclude --exclude-limit $(bin/rubocop -L | wc -l) -c .rubocop.yml
```

##### Using `--auto-correct`
La opción de `--auto-correct` nos permite usar rubocop para corregir automáticamente cierto tipo de ofensas. 
```sh
bin/rubocop --auto-correct path/to/file(s)
```

##### [rubocop-sorbet](https://github.com/Shopify/rubocop-sorbet)
[docs](https://github.com/Shopify/rubocop-sorbet/blob/master/manual/cops_sorbet.md)
##### Using `--auto-correct` to add method signatures
```sh
bin/rubocop -fs --only Sorbet/EnforceSignatures -a path/to/file(s)
```

##### Using autocorrect to add typecheck sigils
```sh
bin/rubocop -fs --only ????
```

# Query Pattern
Son objetos o módulos que se encargan de hacer queries a las distintas storages. Puede bien ser una query a la base de datos mediante `ActiveRecord` o bien puede ser una llamada a elastic search o a redis.

Tienen que devolver un objeto o una colección de objetos recolectada de alguna de estas fuentes externas. Usualmente esto significa un objeto o una colección de objetos de `ActiveRecord`.

### Naming
Se pueden nombrar como `User::FindByEmail`, `Books::WhereAuthor`, `User::Queries`.

### Implementació
Se pueden implementar como servicios o como módulo.

Sus métodos siempre retornan una instancia de un objeto, o una colección de objetos de una clase.

#### Diferencia con [[factories]]
Se diferencian de los factories en que estos últimos construyen (`#build`) o crean (`#create`) objetos **nuevos**; en cambio las queries obtienen la data de algún lugar en donde existe previamente.
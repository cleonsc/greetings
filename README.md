# Saludos en GO

Este paquete proporciona una forma simple de obtener saludos personalizados

## Instalación
Ejecuta el siguiente comando para instalar el paquete:
```bash
go get -u github.com/cleonsc/greetings
```

## Uso
Aquí tienes un ejemplo de como utilizar el paquete en tu código:

```go
package main

import (
	"fmt"
	"log"
	"github.com/cleonsc/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	message, err := greetings.Hello("Juan")
	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(message)

	names := []string{"César", "Edwin", "Juan"}
	messages, err := greetings.Hellos(names)
	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(messages)
}
```
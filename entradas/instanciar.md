Instanciar en Python significa crear una instancia de una clase, es decir, crear un objeto con base en dicha clase para definir qué atributos y métodos debe tener. 

En palabras más sencillas, una clase es como una plantilla, y cuando la instanciamos, lo que estamos haciendo es un objeto que se ajusta a nuestra plantilla.

Para tenerlo más claro, vayamos con un ejemplo sencillo. Definamos una clase que se llame "Autos" (es importante recordar que las clases siempre inician con letra mayúscula) cuyos atributos sean "marca", "modelo" y "year":

```python
class Autos:
    def __init__(self, marca, modelo, year):
        self.marca = marca
        self.modelo = modelo
        self.year = year
```

Ahora supongamos que queremos enviar un mensaje que diga "Mi auto es un Suzuki Ignis año 2023". Para ello, primero tendríamos que definir nuestra función (método) "mensaje" dentro de la clase Auto, es decir, tabulada a la altura del def anterior:

```python
    def mensaje(self):
        print(f'Mi auto es un {self.marca} {self.modelo} año {self.year}')
```

Y después crear una instancia de esta clase. En nuestro ejemplo, dicha instancia (objeto) será "auto1":

```python

auto1 = Autos('Suzuki', 'Ignis', 2023)
```

Nuestra instancia "auto1" está basada en la clase Autos y tiene sus propios valores para los atributos "marca", "modelo" y "year". 

Para imprimir el mensaje, llamamos a nuestro método "mensaje":

```python
auto1.mensaje()
```

Si estás iniciando en la programación orientada a objetos en python, seguramente tienes algunas dudas sobre qué significan "init" y "self". No te preocupes. En otra entrada, ahondaremos en ello. Por ahora, te comento que "self" es un parámetro que se usa para referirse al objeto actual (en nuestro ejemplo, el objeto es la instancia "auto1") y que "init" es un método especial llamado constructor que se usa para inicializar los atributos de una clase. 

¡Ahora puedes probar y divertirte! 

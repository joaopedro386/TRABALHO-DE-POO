POLIMORFISMO :

class Animal:
    def falar(self):
        pass

class Cachorro(Animal):
    def falar(self):
        return "Au au!"

class Gato(Animal):
    def falar(self):
        return "Miau!"

class Vaca(Animal):
    def falar(self):
        return "Muu!"

# Criando instâncias das classes derivadas
cachorro = Cachorro()
gato = Gato()
vaca = Vaca()

# Chamando o método falar em cada objeto
print(cachorro.falar())  # Saída: "Au au!"
print(gato.falar())      # Saída: "Miau!"
print(vaca.falar())      # Saída: "Muu!"



#Explicação DO CODIGO ACIMA 

# Neste exemplo, temos uma classe base Animal e três classes derivadas Cachorro, Gato e Vaca. A classe base Animal define 
um método falar() vazio, enquanto as classes derivadas Cachorro, Gato e Vaca implementam esse método com comportamentos 
diferentes.

# Ao criar instâncias das classes derivadas e chamar o método falar(), o Python realiza a vinculação dinâmica e executa a
implementação correta do método com base no tipo real do objeto. Assim, o polimorfismo é alcançado, permitindo que 
objetos de diferentes classes se comportem de maneira diferente, mas sejam tratados de forma uniforme.


HERANAÇA:


class Animal:
    def __init__(self, nome):
        self.nome = nome

    def emitir_som(self):
        print("O animal está emitindo um som.")

class Cachorro(Animal):
    def emitir_som(self):
        print("O cachorro está latindo.")

class Gato(Animal):
    def emitir_som(self):
        print("O gato está miando.")

# Criando instâncias das classes derivadas
cachorro = Cachorro("Rex")
gato = Gato("Felix")

# Chamando o método emitir_som em cada objeto
cachorro.emitir_som()  # Saída: "O cachorro está latindo."
gato.emitir_som()      # Saída: "O gato está miando."



# Neste exemplo, temos uma classe base Animal que possui um método emitir_som(). Em seguida, temos duas classes derivadas Cachorro e Gato, que herdam da classe Animal.

# A classe Animal tem um construtor que recebe um parâmetro nome e define um atributo nome para o animal. O método emitir_som() simplesmente imprime uma mensagem genérica.

# As classes derivadas Cachorro e Gato substituem o método emitir_som() da classe base com suas próprias implementações específicas. Ao criar instâncias dessas classes e chamar o método emitir_som(), a implementação correta é executada com base no tipo real do objeto.



ENCAPSULAMENTO:


class Carro:
    def __init__(self, marca, modelo):
        self.marca = marca        # Atributo público
        self.__modelo = modelo    # Atributo privado

    def get_modelo(self):
        return self.__modelo      # Método público para obter o modelo

    def set_modelo(self, novo_modelo):
        self.__modelo = novo_modelo  # Método público para definir o modelo


meu_carro = Carro("Ford", "Mustang")
print(meu_carro.marca)          # Saída: "Ford"
print(meu_carro.get_modelo())   # Saída: "Mustang"

meu_carro.__modelo = "Fiesta"   # Tentativa de atribuição direta a um atributo privado
print(meu_carro.get_modelo())   # Saída: "Mustang"

meu_carro.set_modelo("Fiesta")  # Usando o método público para definir o modelo
print(meu_carro.get_modelo())   # Saída: "Fiesta"



#Neste exemplo, a classe Carro possui dois atributos: marca (público) e __modelo 
(privado). Além disso, a classe define os métodos get_modelo() e set_modelo() para acessar e modificar 
o atributo privado __modelo.


#Ao criar uma instância da classe Carro, podemos acessar o atributo público marca diretamente. No entanto,
o atributo privado __modelo não é acessível diretamente. Em vez disso, usamos o método público get_modelo() para obter 
o valor do atributo privado e o método público set_modelo() para definir um novo valor para ele.

Isso ilustra como o encapsulamento protege os dados internos de uma classe, permitindo que sejam acessados e modificados apenas
através de métodos controlados. D



# 🏛️ Pilares da Programação Orientada a Objetos (POO)

A Programação Orientada a Objetos (POO) é um paradigma fundamental para estruturar e organizar código de maneira modular e reutilizável. Aqui estão os quatro principais pilares que sustentam a POO:

## ✨ 1. Abstração
A **abstração** é o processo de simplificação da complexidade, focando nos aspectos essenciais de um objeto ou sistema e ocultando detalhes não relevantes. Com a abstração, criamos classes que representam conceitos de forma clara, mantendo a complexidade interna encapsulada.

## 🔒 2. Encapsulamento
O **encapsulamento** envolve restringir o acesso direto a componentes internos de um objeto para proteger a integridade dos dados. Isso é alcançado controlando a visibilidade através de modificadores como `private`, `protected`, ou `public`. O encapsulamento promove segurança e modularidade.

## 🧬 3. Herança
A **herança** permite que uma classe (subclasse) herde propriedades e comportamentos de outra classe (superclasse). Isso facilita a reutilização de código e permite a criação de relações entre classes. A herança possibilita a criação de hierarquias e a utilização de código existente para novas funcionalidades.

## 🎭 4. Polimorfismo
O **polimorfismo** permite que um objeto tome diferentes formas, ou seja, o mesmo método ou operação pode ter comportamentos diferentes dependendo do contexto. Isso é útil para promover a flexibilidade e a extensibilidade do código. O polimorfismo é implementado através de métodos sobrecarregados ou por substituição de métodos em subclasses.

---

Estes quatro pilares trabalham juntos para criar sistemas robustos, flexíveis e reutilizáveis. Eles são parte essencial do design de software na Programação Orientada a Objetos.



# 🏛️ Exemplos de POO em C# no Unity

Este guia mostra exemplos dos quatro pilares da Programação Orientada a Objetos (POO) em C# no Unity. Cada seção demonstra um dos pilares: abstração, encapsulamento, herança e polimorfismo.

## ✨ Abstração
A abstração é o processo de simplificar a complexidade ao focar nos aspectos essenciais de uma classe, enquanto detalhes internos são ocultados.

```csharp
// Classe abstrata
public abstract class Animal
{
    public abstract void MakeSound(); // Método abstrato
}

````
O encapsulamento protege a integridade de dados, controlando o acesso através de modificadores como private, protected, e public.
O campo health é privado, permitindo acesso apenas através de métodos da classe Player. Isso evita modificações inesperadas ou não intencionadas.

``` csharp
public class Player
{
    // Encapsulando a vida do jogador
    private int health = 100;

    public void TakeDamage(int damage)
    {
        health -= damage;
        if (health < 0)
        {
            health = 0;
        }
    }

    public int GetHealth()
    {
        return health;
    }
}

```

A herança permite que uma classe (subclasse) herde propriedades e comportamentos de outra classe (superclasse), facilitando a reutilização e a criação de hierarquias.
Aqui, Dog e Cat são subclasses de Animal e implementam o método MakeSound(), mostrando como a herança é usada para reutilizar e especializar comportamentos.

``` csharp
public class Dog : Animal
{
    public override void MakeSound()
    {
        Debug.Log("Woof");
    }
}

public class Cat : Animal
{
    public override void MakeSound()
    {
        Debug.Log("Meow");
    }
}


```

O polimorfismo permite que uma interface comum tenha múltiplas implementações. Isso é visto na capacidade de uma classe usar diferentes versões de um método.
O método PlaySound aceita um objeto do tipo Animal, mas o comportamento muda conforme a subclasse usada. O mesmo método exibe resultados diferentes, dependendo do tipo específico de objeto passado.

``` csharp
public class Zoo
{
    public void PlaySound(Animal animal)
    {
        animal.MakeSound(); // Polimorfismo
    }
}

public class Game : MonoBehaviour
{
    private void Start()
    {
        Zoo zoo = new Zoo();
        Animal dog = new Dog();
        Animal cat = new Cat();

        zoo.PlaySound(dog); // Output: Woof
        zoo.PlaySound(cat); // Output: Meow
    }
}


```




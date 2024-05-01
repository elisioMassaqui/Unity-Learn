# Persistência de Dados entre Cenas no Unity

No Unity, a persistência de dados entre cenas é crucial para manter informações do jogo, como pontuações, progresso, configurações, ou o estado do jogador. Existem várias abordagens para alcançar isso. Vamos explorar três das mais comuns: PlayerPrefs, Objetos Singleton e Dados Estáticos.

## 📦 PlayerPrefs
O PlayerPrefs é uma funcionalidade do Unity para armazenar e recuperar valores simples (como inteiros, strings, e floats). Esses dados persistem entre sessões do jogo. Apesar de ser conveniente para informações pequenas e persistentes, ele tem limitações quanto à complexidade e tamanho.

```csharp
// Para salvar um valor inteiro
PlayerPrefs.SetInt("HighScore", 100);

// Para carregar um valor inteiro
int highScore = PlayerPrefs.GetInt("HighScore", 0); // Se não houver valor salvo, retorna 0

// Para salvar e carregar strings
PlayerPrefs.SetString("PlayerName", "John");
string playerName = PlayerPrefs.GetString("PlayerName", "DefaultName");

// Não esqueça de salvar após definir PlayerPrefs
PlayerPrefs.Save();
```

 Objetos Singleton
Um objeto Singleton garante que uma classe tenha apenas uma instância, persistindo entre cenas. É uma abordagem comum para manter dados que precisam ser acessados por várias partes do jogo. Aqui está um exemplo básico:

``` csharp
public class GameManager : MonoBehaviour
{
    private static GameManager instance;

    public static GameManager Instance
    {
        get
        {
            if (instance == null)
            {
                instance = FindObjectOfType<GameManager>();

                if (instance == null)
                {
                    GameObject singleton = new GameObject(typeof(GameManager).Name);
                    instance = singleton.AddComponent<GameManager>();
                    DontDestroyOnLoad(singleton); // Persiste entre cenas
                }
            }

            return instance;
        }
    }

    public int Score { get; set; } // Exemplo de dado persistente
}
```

Dados Estáticos
Dados estáticos permanecem em memória enquanto o jogo está em execução. Isso pode ser útil para armazenar informações acessíveis em várias cenas sem a necessidade de objetos persistentes.

``` csharp
public static class GameData
{
    public static int PlayerScore = 0;
    public static string PlayerName = "DefaultPlayer";
}


```

Você pode acessar e modificar dados estáticos de qualquer parte do código, mas eles não persistem entre sessões do jogo. Use dados estáticos para informações temporárias ou durante a execução do jogo.

Essas abordagens oferecem diferentes maneiras de persistir dados entre cenas no Unity. Dependendo do seu caso de uso, escolha o método que melhor se adapta às suas necessidades. Para dados simples e persistentes entre sessões, use PlayerPrefs. Para dados que precisam persistir apenas durante o tempo de execução, considere objetos Singleton ou dados estáticos.

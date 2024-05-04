# Missão: Primeiro Passo no Caminho do Núcleo Criativo

Bem-vindo à sua jornada no Núcleo Criativo! Esta missão é o ponto de partida para o seu aprendizado e desenvolvimento de habilidades essenciais no uso do Unity. Aqui, você descobrirá os tópicos fundamentais, atividades práticas e habilidades que farão parte do seu caminho.

## Objetivos da Missão
Durante esta missão, você irá:
- **Explorar os Tópicos do Creative Core**: Ganhe uma compreensão geral do que será coberto ao longo do curso.
- **Escolher um Projeto Guiado**: Selecione um projeto para aplicar as habilidades que você está aprendendo.
- **Criar um Novo Projeto no Unity**: Inicie seu próprio projeto, tomando algumas decisões técnicas no processo.
- **Utilizar Recursos de Terceiros com Responsabilidade**: Aprenda como incorporar o trabalho de outras pessoas nos seus projetos de maneira ética.
- **Conhecer a Documentação Técnica do Unity**: Saiba onde buscar informações detalhadas e suporte para seu aprendizado.
- **Praticar Avaliação Crítica**: Desenvolva habilidades de tomada de decisões para projetos criativos.

## Atividades
Para atingir esses objetivos, você deve:
1. **Familiarizar-se com o Conteúdo do Núcleo Criativo**: Faça uma revisão dos tópicos principais do curso.
2. **Selecionar um Projeto Guiado**: Escolha um projeto do Unity que seja relevante para seus interesses e habilidades.
3. **Iniciar um Novo Projeto no Unity**: Crie um projeto do zero e tome decisões sobre configuração, layout e outras escolhas técnicas.
4. **Incorporar Recursos de Terceiros**: Aprenda sobre licenças, direitos autorais e uso ético de ativos em seus projetos.
5. **Explorar a Documentação do Unity**: Visite a documentação oficial para obter informações detalhadas e dicas úteis.
6. **Praticar Avaliação Crítica**: Refletir sobre suas decisões durante o processo criativo, considerando alternativas e justificando suas escolhas.

## Habilidades que Você Adquirirá
- Compreensão dos conceitos básicos do Unity
- Capacidade de iniciar e gerenciar um projeto criativo
- Conhecimento sobre uso responsável de recursos de terceiros
- Habilidade para encontrar e usar documentação técnica
- Aptidão para avaliação crítica e tomada de decisões em projetos criativos

## Próximos Passos
Depois de concluir esta missão, você estará pronto para avançar para missões mais avançadas no caminho do Núcleo Criativo. Boa sorte e divirta-se aprendendo!

Ao longo deste caminho, você combinará as habilidades que aprenderá em cada um dos domínios criativos em um projeto guiado maior.

Um documento de design é um plano detalhado para um produto. Ele descreve como um produto deve funcionar e sua aparência.

# Pipelines de Renderização no Unity

## Introdução
Ao criar um projeto 3D no Unity, uma das decisões importantes a ser tomada é qual pipeline de renderização usar. O Unity oferece três principais pipelines de renderização: 
- **Pipeline de Renderização Integrado** (modelo 3D)
- **Pipeline de Renderização de Alta Definição (HDRP)** (Cena de amostra 3D (HDRP))
- **Universal Render Pipeline (URP)** (Cena de amostra 3D (URP))

Antes de entender a diferença entre esses pipelines, vamos primeiro explorar o que significa "renderizar".

## O Que é Renderização?
Renderização é o processo de gerar uma imagem a partir de uma cena 3D. Isso envolve a conversão de dados 3D (como malhas, texturas, luzes e câmeras) em uma imagem 2D para ser exibida na tela. O processo inclui cálculos complexos para determinar como a luz interage com objetos, como sombras são formadas, e como as cores e texturas são aplicadas a superfícies.

Quando você "renderiza" uma cena no Unity, está criando a imagem final a partir dos elementos que compõem a cena. Este processo pode variar em complexidade, dependendo do tipo de pipeline de renderização que você usa.

## Pipelines de Renderização
### Pipeline de Renderização Integrado
O pipeline de renderização integrado é o sistema mais antigo do Unity. Ele usa um conjunto fixo de regras e é o padrão para projetos mais simples ou com menos requisitos gráficos. É ideal para projetos menores e jogos que não precisam de efeitos visuais avançados.

### Pipeline de Renderização de Alta Definição (HDRP)
O HDRP é projetado para alto desempenho gráfico e realismo. Ele oferece suporte para recursos como iluminação física, sombreamento avançado, reflexão, refração, volume atmosférico e mais. É ideal para projetos que requerem qualidade gráfica de ponta, como jogos AAA e simulações realistas.

### Universal Render Pipeline (URP)
O URP é uma versão modernizada e mais flexível do pipeline integrado. Ele é otimizado para dispositivos móveis e plataformas de baixa capacidade, mas ainda oferece recursos visuais mais avançados do que o pipeline integrado. URP é uma escolha popular para desenvolvedores que desejam boa qualidade visual com desempenho otimizado.

## Como Escolher o Pipeline Certo?
A escolha do pipeline de renderização certo depende das necessidades do seu projeto:

- **Pipeline Integrado**: Ideal para projetos simples, jogos 2D ou pequenos jogos 3D sem necessidade de recursos gráficos avançados.
- **HDRP**: Para projetos que requerem alto realismo, como jogos AAA ou simulações de alta fidelidade. Tenha em mente que exige mais poder computacional.
- **URP**: Uma escolha equilibrada, adequada para uma ampla gama de projetos, especialmente se precisar de bom desempenho em plataformas diversas.

Considere as necessidades do seu projeto, incluindo requisitos gráficos, desempenho esperado, e as plataformas alvo, antes de escolher o pipeline de renderização mais adequado.

## O que é renderização?

Renderização é o processo de pegar dados tridimensionais (3D) e usá-los para gerar uma imagem bidimensional (2D) para uma tela.

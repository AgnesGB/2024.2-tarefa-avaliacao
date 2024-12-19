# 2024.2 Avaliação do 1o período de Sistemas Operacionais

## Informações gerais
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- Disciplina: **SO** Sistemas Operacionais
- Professor: [Leonardo A. Minora](https://github.com/leonardo-minora)
- Aluno: [Agnes Gonçalves Barbosa](https://github.com/AgnesGB)

## Avaliação
- **Lembre de fazer o fork deste repositório**
- As questões foram construídas com o auxílio do [copilot](https://copilot.microsoft.com/)

# Questão 1. Introdução a sistemas operacionais

Considere as funções e objetivos principais de um sistema operacional conforme discutido no texto. Explique como um sistema operacional gerencia os recursos de hardware e software de um computador para garantir eficiência e segurança. Em sua resposta, aborde os seguintes pontos:

- Gerenciamento de processos
- Gerenciamento de memória
- Gerenciamento de dispositivos de entrada e saída
- Gerenciamento de arquivos

**Dica**: Pense em exemplos práticos de como o sistema operacional realiza essas tarefas no dia a dia de um usuário.

**Copilot informa**: Essa questão incentiva os alunos a explorarem os conceitos fundamentais e a aplicarem o conhecimento teórico em situações práticas. Se precisar de mais alguma coisa, estou aqui para ajudar!

### Resposta:
Um SO é um software que atua como intermediário entre o hardware de um computador e os programas em execução., e tem como objetivo gerenciar os recursos de hardware e software de forma eficiente e segura, proporcionando uma experiência estável e funcional para o usuário.

- Gerenciamento de processos: envolve a criação, execução e terminação de processos, além da alocação de recursos como tempo de CPU, além de utilizar um escalonador para determinar quais processos terão acesso ao processador e por quanto tempo. Ele também isola os processos para evitar interferência mútua e monitora seu estado (pronto, em execução, suspenso). EX: Ouvir musica e navegar na internet, o SO garante que ambos os processos atuem sem prejudicar o desempenho geral.
- Gerenciamento de memória: assegura que a memória RAM seja utilizada de forma eficiente e que cada processo tenha acesso seguro à sua área de memória, divide a memória em partes e aloca espaços para os processos conforme necessário. EX: abrir várias abas no navegador, o SO aloca memória para cada aba, isolando-as para evitar que uma falha em uma aba afete as outras.
- Gerenciamento de dispositivos de entrada e saída: gerencia o acesso aos dispositivos de hardware, como teclado, mouse, impressoras e discos rígidos, garantindo comunicação eficiente e evitando conflitos. Ele utiliza drivers específicos para cada dispositivo e uma fila de solicitações para gerenciar múltiplos acessos. EX: copiar um arquivo para um pendrive, o SO controla a transferência dos dados, evitando que outro programa interfira no processo.
- Gerenciamento de arquivos: organiza e controla o acesso aos dados armazenados no disco rígido ou outros meios de armazenamento. Usa sistemas de arquivos, como NTFS ou EXT4, para estruturar os dados em diretórios e arquivos, além de gerenciar permissões de acesso para garantir segurança. EX: ao salvar um documento em uma pasta específica, o SO registra a localização e mantém as permissões para que somente usuários autorizados possam acessá-lo.

# Questão 2. Estrutura de sistemas operacionais

## Texto informativo
### Estrutura de Sistemas Operacionais: Custo de Desenvolvimento e Segurança da Informação

A estrutura de um sistema operacional (SO) é fundamental para determinar tanto o custo de desenvolvimento e manutenção quanto a segurança da informação. Existem várias arquiteturas de SO, como monolítica, microkernel e em camadas, cada uma com suas próprias implicações em termos de custo e segurança.

#### Custo de Desenvolvimento e Manutenção

1. **Arquitetura Monolítica**:
   - **Desenvolvimento**: Geralmente, mais rápida de desenvolver inicialmente, pois todos os componentes do SO são integrados em um único bloco de código.
   - **Manutenção**: Pode ser mais complexa e cara, pois qualquer alteração em um componente pode afetar todo o sistema, exigindo testes extensivos e cuidadosos.

2. **Arquitetura Microkernel**:
   - **Desenvolvimento**: Pode ser mais demorada e cara inicialmente, pois envolve a criação de um núcleo mínimo e a implementação de serviços adicionais como processos separados.
   - **Manutenção**: Mais fácil e menos custosa, já que os componentes são isolados. Atualizações e correções podem ser feitas em módulos específicos sem impactar o núcleo do sistema.

3. **Arquitetura em Camadas**:
   - **Desenvolvimento**: Moderadamente complexa, pois cada camada deve ser bem definida e interagir corretamente com as outras.
   - **Manutenção**: Relativamente fácil, pois problemas podem ser isolados e corrigidos em camadas específicas sem afetar o restante do sistema.

#### Segurança da Informação

1. **Arquitetura Monolítica**:
   - **Segurança**: Pode ser mais vulnerável, pois uma falha em qualquer parte do sistema pode comprometer todo o SO. A integração de todos os componentes em um único bloco de código pode dificultar a implementação de medidas de segurança robustas.

2. **Arquitetura Microkernel**:
   - **Segurança**: Geralmente mais segura, pois isola os serviços em processos separados. Isso limita o impacto de uma falha ou ataque a um único componente, protegendo o núcleo do sistema e outros serviços.

3. **Arquitetura em Camadas**:
   - **Segurança**: Oferece um bom equilíbrio, pois cada camada pode implementar suas próprias medidas de segurança. No entanto, a comunicação entre camadas deve ser cuidadosamente gerenciada para evitar vulnerabilidades.

### Conclusão

A escolha da arquitetura de um sistema operacional tem um impacto significativo tanto no custo de desenvolvimento e manutenção quanto na segurança da informação. Arquiteturas monolíticas podem ser mais rápidas e baratas de desenvolver inicialmente, mas podem acarretar custos de manutenção mais altos e maiores riscos de segurança. Por outro lado, arquiteturas microkernel e em camadas podem exigir um investimento inicial maior, mas oferecem vantagens em termos de manutenção e segurança.

## Questão
Com base no texto sobre a estrutura de sistemas operacionais, analise como as diferentes arquiteturas (monolítica, microkernel e camadas) impactam o custo com a equipe de desenvolvimento e a segurança do sistema operacional. Em sua resposta, considere os seguintes pontos:
- Complexidade de implementação e manutenção
- Necessidade de especialização da equipe
- Potenciais vulnerabilidades de segurança
- Facilidade de atualização e correção de falhas

**Dica:** Utilize exemplos de sistemas operacionais reais que adotam essas arquiteturas para ilustrar sua análise.

**Copilot informa**: Essa questão incentiva os alunos a considerarem tanto os aspectos econômicos quanto os de segurança ao avaliar diferentes arquiteturas de sistemas operacionais.

### Resposta:
Enquanto arquiteturas monolíticas são rápidas e baratas de desenvolver, elas apresentam desafios em segurança e manutenção. Arquiteturas microkernel e em camadas oferecem maior modularidade e segurança, mas exigem maior especialização e investimento inicial. A escolha ideal dependerá do contexto de uso e das prioridades, como custo, segurança ou facilidade de manutenção. Enquanto a Monolítica se mostra a mais "simples" inicialmente, ela requer um custo de manutenção alto, principalmente devido à sua vulnerabilidade em questões de segurança. Já a Microkernel, por precisar de um núcleo e da separação de processos, tem um custo inicial alto, mas, devido à alta segurança, sua manutenção acaba sendo menos custosa. Já a em Camadas, parece ter um equilíbrio maior, tendo uma segurança por camada, que pode acabar por apresentar algum problema na comunicação entre as camadas, mas também requer um bom investimento inicial, com manutenção mais simples, já que é feita camada a camada.
EXEMPLOS:
- Monolítica: Linux.
- Microkernel: Minix.
- Camadas: Windows.

# Questão 3. Introdução à Segurança de Sistemas Operacionais

## Texto informativo

A segurança de um sistema operacional é um aspecto crucial que visa proteger os recursos do sistema contra acessos não autorizados, ataques maliciosos e falhas. Um sistema operacional seguro deve garantir a integridade, confidencialidade e disponibilidade dos dados e serviços. Para alcançar esses objetivos, várias técnicas e mecanismos são implementados, incluindo:

1. **Controle de Acesso**: Define quem pode acessar o sistema e quais recursos podem ser utilizados. Isso é feito através de autenticação (verificação de identidade) e autorização (permissão de acesso).

2. **Criptografia**: Utilizada para proteger dados em trânsito e em repouso, garantindo que apenas usuários autorizados possam acessar informações sensíveis.

3. **Auditoria e Monitoramento**: Registra atividades do sistema para detectar e responder a comportamentos suspeitos ou anômalos.

4. **Isolamento de Processos**: Garante que os processos sejam executados em ambientes isolados, evitando que um processo comprometa a segurança de outro.

5. **Atualizações e Patches**: Manter o sistema operacional atualizado é essencial para corrigir vulnerabilidades conhecidas e proteger contra novas ameaças.


## Questão

Considerando os mecanismos de segurança discutidos, analise como a implementação de controles de acesso e criptografia pode impactar a performance e a usabilidade de um sistema operacional. Em sua resposta, aborde os seguintes pontos:
- Benefícios e desafios de cada mecanismo
- Impacto na experiência do usuário
- Exemplos de situações onde esses mecanismos são críticos

**Dica:** Pense em como esses mecanismos são aplicados em sistemas operacionais que você utiliza no dia a dia, como Windows, Linux ou macOS.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre o equilíbrio entre segurança, performance e usabilidade, aplicando conceitos teóricos a contextos práticos.

### Resposta
O controle de acesso e a criptografia são essenciais para a segurança de sistemas operacionais, mas podem impactar a performance e a usabilidade.  

- **Controle de Acesso:**  
  Beneficia a segurança ao limitar acessos não autorizados, mas pode frustrar usuários com autenticações frequentes ou rígidas. Bem implementado (como biometria), é quase imperceptível, mas, se mal otimizada, pode causar atrasos, especialmente em sistemas com grande volume de dados ou dispositivos com hardware antigo.
- **Criptografia:**  
  Protege dados, mas pode consumir muitos recursos em tempo real, especialmente em dispositivos menos potentes. Configurações bem ajustadas tornam seu impacto na usabilidade mínimo.  

Em situações críticas:
- Ambientes corporativos:
Controle de acesso e criptografia são indispensáveis para proteger informações confidenciais e atender a regulamentações (como GDPR).
- Serviços online:
Controle de acesso e criptografia (ex.: HTTPS e senhas protegidas) são essenciais para proteger dados de usuários em plataformas como redes sociais ou bancos.

# Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

## Texto informativo

O escalonamento de processos é uma função crítica de um sistema operacional, responsável por determinar a ordem em que os processos são executados pelo processador. O objetivo é maximizar a eficiência do sistema, garantindo que os recursos sejam utilizados de maneira justa e eficaz. No entanto, encontrar o algoritmo de escalonamento ótimo envolve um equilíbrio delicado entre o custo de processamento e a eficiência do escalonamento.

### Custo de Processamento

O custo de processamento refere-se ao tempo e aos recursos necessários para executar um algoritmo de escalonamento. Algoritmos mais complexos podem oferecer melhores resultados em termos de tempo de resposta e utilização do processador, mas também podem exigir mais recursos computacionais para tomar decisões de escalonamento. Isso pode incluir tempo de CPU, memória e outras operações de sistema.

### Algoritmo Ótimo de Escalonamento

Um algoritmo ótimo de escalonamento é aquele que maximiza a eficiência do sistema operacional, minimizando o tempo de espera dos processos, o tempo de resposta e o tempo de retorno. Alguns dos algoritmos de escalonamento mais comuns incluem:

- **First-Come, First-Served (FCFS)**: Simples e fácil de implementar, mas pode levar a longos tempos de espera para processos curtos.
- **Shortest Job Next (SJN)**: Minimiza o tempo médio de espera, mas pode ser difícil de implementar devido à necessidade de prever o tempo de execução dos processos.
- **Round Robin (RR)**: Oferece uma abordagem justa, atribuindo fatias de tempo iguais a todos os processos, mas pode resultar em maior sobrecarga de contexto.
- **Priority Scheduling**: Processos com maior prioridade são executados primeiro, mas pode levar à inanição de processos de baixa prioridade.

## Questão

Considerando os conceitos de custo de processamento e algoritmo ótimo de escalonamento, analise como diferentes algoritmos de escalonamento podem impactar a performance de um sistema operacional em termos de tempo de resposta, tempo de espera e utilização do processador. Em sua resposta, aborde os seguintes pontos:
- Vantagens e desvantagens de pelo menos dois algoritmos de escalonamento
- Impacto do custo de processamento na escolha do algoritmo
- Exemplos de situações onde um algoritmo pode ser preferível a outro

**Dica:** Pense em como esses algoritmos são aplicados em diferentes cenários, como sistemas de tempo real, servidores web e sistemas operacionais de uso geral.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre a complexidade e os trade-offs envolvidos na escolha de um algoritmo de escalonamento, aplicando conceitos teóricos a contextos práticos.

### Resposta

**First-Come, First-Served (FCFS)**

Vantagens:
- Fácil de implementar e com baixo custo de processamento. Funciona bem em sistemas onde a ordem de chegada é importante, como filas de impressão.

Desvantagens:
- Pode levar ao convoy effect, onde processos pequenos ficam esperando processos maiores terminarem. Resulta em tempos de espera altos para processos curtos.

Uso: Fila de impressão ou sistemas de processamento simples.


**Shortest Job Next (SJN)**

Vantagens:
- Minimiza o tempo médio de espera, pois prioriza processos mais curtos.
Maximiza a eficiência do processador em sistemas de processamento em lote.

Desvantagens:
- Requer conhecimento prévio do tempo de execução dos processos, o que pode não ser viável. Pode levar à inanição de processos longos, que ficam constantemente preteridos.

Uso: Servidores de processamento em lote.

# Questão 5. Aplicativo em python vs aplicativos em c

## Questão

Explique o caminho que as instruções seguem desde um aplicativo escrito em Python e um aplicativo escrito em linguagem C até serem executadas pelo hardware. Em sua resposta, considere os seguintes pontos:
- O papel do interpretador no caso do Python
- O processo de compilação no caso do C
- A interação entre o kernel do sistema operacional e os drivers de dispositivo
- A tradução final das instruções para o formato binário (0 e 1) executado pelo hardware

**Dica:** Compare e contraste os dois processos, destacando as principais diferenças e semelhanças na forma como as instruções são processadas e executadas.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre os diferentes caminhos que as instruções seguem em linguagens interpretadas e compiladas, aplicando conceitos teóricos a contextos práticos.

### Resposta:

**1. Aplicativo em Python**  
  O Python é uma linguagem interpretada. Isso significa que as instruções do código-fonte são lidas e executadas linha a linha por um interpretador, como o CPython.
- Caminho das Instruções: 
  1. O código Python é convertido em **bytecode** pelo interpretador, que é uma representação intermediária mais próxima do código de máquina.  
  2. Esse bytecode é executado por uma **máquina virtual** (Python Virtual Machine - PVM).  
  3. Durante a execução, o interpretador interage com o **kernel** do sistema operacional para solicitar recursos, como memória, processamento e entrada/saída.  
  4. As instruções finais são traduzidas em código binário pelo kernel e pelos drivers, sendo enviadas ao hardware.  
- Impacto:  
  O uso de um interpretador torna o Python mais lento em execução comparado ao C, pois as instruções são processadas em tempo real.

**2. Aplicativo em C**  
  O C é uma linguagem compilada, ou seja, o código-fonte é traduzido previamente em **código de máquina** por um compilador, como o **GCC**.
- Caminho das Instruções: 
  1. O código é transformado em código de máquina (binário executável) durante a compilação, antes da execução.  
  2. Quando executado, o binário interage diretamente com o **kernel** do sistema operacional, que gerencia os recursos do sistema.  
  3. O kernel solicita a ajuda dos **drivers de dispositivo** para traduzir as instruções de alto nível em comandos que o hardware pode entender.  
  4. Essas instruções chegam ao processador já no formato binário (0s e 1s).  
- Impacto: 
  Por já estar em código de máquina, aplicativos em C têm execução mais rápida e eficiente, mas requerem um passo extra de compilação.

**3. Interação com o Kernel e Drivers**
- Em ambos os casos, o kernel do sistema operacional é responsável por:
  - Gerenciar os recursos do sistema, como memória e CPU.
  - Solicitar aos drivers de dispositivo que traduzam as instruções para comandos de hardware específicos.
- A diferença está na forma como o código chega ao kernel:  
  - Em Python, via interpretador e máquina virtual.  
  - Em C, diretamente como código de máquina já compilado.

**4. Semelhanças e Diferenças**
- Semelhanças:  
  - Ambos interagem com o kernel e os drivers para acessar recursos de hardware.  
  - Ambos precisam traduzir suas instruções em binário para serem compreendidos pelo hardware.  
- Diferenças:
  - Python usa um interpretador, enquanto C usa um compilador.  
  - Python requer mais etapas em tempo de execução (interpretação, bytecode, execução pela PVM).  
  - C gera código de máquina direto, resultando em maior eficiência.


A principal diferença entre Python e C está no momento em que ocorre a tradução do código para binário. Python é interpretado em tempo de execução, o que o torna mais flexível, mas menos eficiente. Já o C é compilado previamente, o que resulta em maior velocidade e eficiência no uso de recursos, sendo ideal para sistemas de baixo nível ou aplicações críticas em desempenho.
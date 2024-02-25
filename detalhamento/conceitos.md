# EC2 e AMI

# EC2

## O que é?

- Serviço de computação em nuvem
- Capacidade de computação escalável na nuvem, permitindo que os desenvolvedores executem serviços em servidores virtuais configuráveis sob demanda.
- Implantar **servidores virtuais** (chamados de instâncias EC2)
- Desde pequenas instâncias para testes e desenvolvimento até instâncias poderosas para cargas de trabalho de produção de alto desempenho.
- Os usuários têm controle total sobre suas instâncias EC2, incluindo a capacidade de iniciar, parar, encerrar e dimensionar verticalmente (aumentar ou diminuir recursos como CPU, memória e armazenamento) conforme necessário.

# AMI

É uma imagem virtual usada para criar uma instância EC2.

É uma espécie de "modelo" de uma máquina virtual que inclui o sistema operacional, software pré-instalado, configurações e até mesmo dados.

As AMIs são fundamentais para o funcionamento do Amazon EC2, pois permitem aos usuários iniciar instâncias virtualizadas em questão de minutos, em vez de configurar manualmente cada máquina virtual do zero. As AMIs podem ser criadas por usuários da AWS ou disponibilizadas pela AWS e por terceiros.

# PUTTY e SSH

# PUTTY

## O que é

Putty é uma ferramenta de código aberto usada principalmente em sistemas Windows para acessar servidores remotos via SSH (Secure Shell), Telnet, Rlogin e outras conexões de rede. 

## Pra que é usado

No contexto de nuvem e AWS (Amazon Web Services), o Putty é frequentemente utilizado para acessar instâncias EC2 (Elastic Compute Cloud) e outros recursos hospedados na AWS.

## Como usa

Quando você provisiona uma instância EC2 na AWS, normalmente recebe uma chave SSH para autenticar e acessar essa instância. O Putty pode ser usado para estabelecer uma conexão SSH com essa instância, permitindo que você execute comandos no servidor remoto, transfira arquivos e realize outras operações administrativas.

# SSH

## O que é

SSH, ou Secure Shell, é um protocolo de rede utilizado para comunicação segura entre dispositivos em uma rede. 

## No que ele agrega

Ele é comumente utilizado para acessar servidores remotos de forma segura, permitindo a execução de comandos, transferência de arquivos e outras operações administrativas.

## Pra que serve

A principal característica do SSH é a sua capacidade de criptografar os dados transmitidos pela rede, o que garante que as informações sensíveis, como senhas e comandos, não sejam interceptadas por terceiros. 

## Como funciona

O SSH utiliza uma arquitetura cliente-servidor, onde o cliente (por exemplo, um computador local) se conecta a um servidor remoto usando o protocolo SSH. O cliente autentica-se no servidor usando credenciais (como uma senha ou uma chave pública) e, uma vez autenticado, pode interagir com o servidor de forma segura.

# RSA e ED25519

# RSA

## O que é

RSA (Rivest-Shamir-Adleman) é um dos primeiros e mais amplamente utilizados algoritmos de criptografia de chave pública. 

## Pra que é usado

Ele é amplamente empregado em sistemas de segurança de dados, como criptografia de dados, assinaturas digitais e autenticação.

## No contexto de EC2

 Quando você cria uma instância EC2, geralmente é necessário especificar uma chave SSH. Essa chave SSH é pode ser uma chave RSA que permite que você se conecte à instância de forma segura usando o protocolo SSH (Secure Shell).

 A chave pública é então colocada na instância EC2, enquanto a chave privada é baixada para o seu computador. Você pode usar essa chave privada para se autenticar e acessar a instância EC2 via SSH.

## Como funciona

O RSA baseia-se na ideia matemática de fatorização de números inteiros grandes, que é uma tarefa computacionalmente difícil. O algoritmo gera um par de chaves: uma chave pública e uma chave privada. A chave pública pode ser compartilhada livremente e é usada para criptografar dados ou verificar assinaturas digitais. A chave privada, por outro lado, é mantida em segredo pelo proprietário e é usada para descriptografar dados criptografados com a chave pública ou para assinar digitalmente mensagens.

## Por que funciona

A segurança do RSA é baseada na dificuldade de fatorizar grandes números primos. Até o momento, não existe nenhum método eficiente conhecido para fatorizar rapidamente produtos de dois números primos grandes em seus fatores primos. Portanto, a segurança do RSA depende da escolha de números primos suficientemente grandes para tornar a fatorização impraticável.

# ED25519

## O que é

ED25519 é um esquema de assinatura digital e sistema de chave pública derivado do algoritmo de curva elíptica Curve25519. Ele é projetado para ser mais seguro e eficiente do que os sistemas tradicionais baseados em RSA e DSA (Digital Signature Algorithm).

## Como funciona

A chave ED25519 é uma chave criptográfica assimétrica, o que significa que é composta por duas partes: uma chave pública e uma chave privada. A chave pública é usada para verificar assinaturas digitais, enquanto a chave privada é usada para gerar essas assinaturas.

## Vantagem

A principal vantagem do ED25519 sobre algoritmos mais antigos, como o RSA, é que ele oferece um nível de segurança comparável com chaves significativamente menores. Isso resulta em operações mais rápidas e menos recursos computacionais necessários para gerar e verificar assinaturas digitais.

## Da mesma maneira que RSA…

No contexto das instâncias EC2 da AWS, o ED25519 pode ser utilizado da mesma forma que o RSA para autenticação e segurança de acesso. Você pode usar chaves ED25519 para se conectar de forma segura às suas instâncias EC2 via SSH, da mesma maneira que faria com chaves RSA. A escolha entre RSA e ED25519 muitas vezes se resume a preferências pessoais e requisitos específicos de segurança e desempenho.

## Sobre Curva Elíptica

1. **Curva Elíptica**: Em matemática, uma curva elíptica é uma forma geométrica definida por uma equação do tipo \( y^2 = x^3 + ax + b \), onde \( a \) e \( b \) são constantes que determinam a forma específica da curva. Essas curvas têm propriedades matemáticas especiais que as tornam úteis em criptografia e outras áreas da matemática aplicada.

2. **Corpo dos Números Inteiros Módulo \( p \)**: Um corpo é um conceito matemático que representa um conjunto onde as operações de adição, subtração, multiplicação e divisão são definidas e possuem as propriedades usuais. "Números inteiros módulo \( p \)" refere-se a um conjunto de números inteiros onde as operações são realizadas considerando o resto da divisão inteira por \( p \), onde \( p \) é um número primo. Isso cria um conjunto finito de números inteiros, variando de 0 a \( p-1 \).

3. **\( 2^{255} - 19 \)**: Esta é uma expressão que define um número específico. \( 2^{255} \) significa 2 elevado à 255ª potência, e \( 19 \) é subtraído deste resultado. O número resultante é muito grande e é usado como o "módulo" para operações matemáticas na curva elíptica Curve25519.

# .pem e .ppk

# .pem

## O que é

O arquivo com extensão ".pem" geralmente é um tipo de arquivo usado em criptografia e segurança de rede. Ele pode conter diferentes tipos de dados, mas geralmente é associado com chaves criptográficas, certificados X.509 ou outros artefatos relacionados à infraestrutura de chave pública (PKI - Public Key Infrastructure).

## De onde veio

A extensão ".pem" significa "Privacy Enhanced Mail", embora hoje em dia seja usada para uma variedade de fins além do email, especialmente em sistemas Unix e Linux.

## [aprofundamento p/ ver dps]

Os arquivos PEM geralmente contêm texto codificado em Base64, que pode incluir cabeçalhos indicando o tipo de informação contida no arquivo. Por exemplo, você pode encontrar arquivos PEM contendo:

1. **Chaves Privadas e Públicas**: Como chaves RSA, DSA, ECDSA, ou ED25519, usadas em criptografia de chave pública.
2. **Certificados X.509**: Usados em SSL/TLS para autenticar a identidade de sites da web, serviços e outras entidades.
3. **Certificados de Autoridade de Certificação (CA)**: Certificados raiz e intermediários usados para validar a autenticidade de outros certificados em uma hierarquia de PKI.
4. **Cadeias de Certificados**: Conjuntos de certificados intermediários que formam uma cadeia de confiança entre um certificado de servidor e um certificado raiz.

## Resumo

Os arquivos PEM são frequentemente usados em ambientes Unix e Linux para armazenar e distribuir chaves criptográficas e certificados de forma conveniente e legível por humanos. Eles também podem ser usados em outras plataformas, embora possa haver variações na forma como são usados e interpretados.

# .ppk ~ putty

## O que é

A extensão de arquivo ".ppk" é comumente associada a arquivos de chave privada usados pelo programa PuTTY, uma ferramenta popular de acesso remoto para sistemas Windows. 

## PuTTY e .ppk

Quando você utiliza o PuTTY para se conectar a um servidor remoto via SSH, você geralmente precisa fornecer uma chave privada para autenticação. O PuTTY usa um formato específico para armazenar essas chaves privadas, e os arquivos com a extensão ".ppk" são esses arquivos.

As chaves privadas no formato ".ppk" são geralmente geradas usando o PuTTY Key Generator (PuTTYgen), uma ferramenta incluída no conjunto de programas PuTTY. O PuTTYgen permite gerar novas chaves, importar chaves existentes de outros formatos e exportar chaves no formato ".ppk".

Esses arquivos ".ppk" contêm informações criptografadas relacionadas à chave privada, como a própria chave, informações de criptografia e outras configurações. Eles são usados pelo PuTTY para autenticar com segurança a conexão com servidores remotos.


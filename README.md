# IPFS
Sistema de Arquivos Interplanetário (IPFS) 
Entenda o que é o IPFS:
https://www.youtube.com/watch?v=5Uj6uR3fp-U

Explica o que é função de hash:
https://en.wikipedia.org/wiki/Hash_function

Explica sobre o SHA256 e te da o hash criptográfico:
https://passwordsgenerator.net/sha256-hash-generator/

Este gerador de hash MD5 é útil para codificar senhas, números de cartões de crédito e outros dados confidenciais em MySQL, Postgress ou outros bancos de dados. Programadores PHP, programadores ASP e qualquer pessoa desenvolvendo em MySQL, SQL, Postgress ou similar devem achar esta ferramenta online um recurso especialmente útil.
O que é um hash MD5?
Um hash MD5 é criado pegando uma string de qualquer comprimento e codificando-a em uma impressão digital de 128 bits. Codificar a mesma string usando o algoritmo MD5 sempre resultará na mesma saída hash de 128 bits. Os hashes MD5 são comumente usados com strings menores ao armazenar senhas, números de cartão de crédito ou outros dados confidenciais em bancos de dados como o popular MySQL. Essa ferramenta fornece uma maneira rápida e fácil de codificar um hash MD5 a partir de uma string simples de até 256 caracteres.
Os hashes MD5 também são usados para garantir a integridade dos dados dos arquivos. Como o algoritmo de hash MD5 sempre produz a mesma saída para a mesma entrada fornecida, os usuários podem comparar um hash do arquivo de origem com um hash recém-criado do arquivo de destino para verificar se está intacto e não modificado.
Um hash MD5 NÃO é criptografia. É simplesmente uma impressão digital da entrada fornecida. No entanto, é uma transação unilateral e, como tal, é quase impossível fazer engenharia reversa de um hash MD5 para recuperar a string original.
https://www.md5hashgenerator.com/
Entendendo a Árvore de Merkle, que seria uma arvore sobre os hashs:
https://en.wikipedia.org/wiki/Merkle_tree
https://tylercipriani.com/blog/2016/03/21/Visualizing-Git-Merkle-DAG-with-D3.js/

ANTES DE EXECUTAR QUALQUER AÇÃO NO IFPS DEVEMOS EXECUTAR NO DIRETÓRIO ipfs-go O SEGUINTE:
Ipfs daemon
Abra o site do IPFS:
Localhost:5001/webui
Depois abra um novo terminal e adicione os arquivos que tenha os hashs.

Agora vamos a intalação do IPFS no seu Windows e Ubuuntu:
http://docs.ipfs.io.ipns.localhost:8080/install/command-line/#system-requirements
Inatale no Windows ou qualquer outro sistema operacional que você estiver usando.
Você instalará a pasta go-ipfs (tem no outro material, procure sobre a instalação do ifps, mas provável ser executar em seu terminal: ipfs install    procure no seu material) vou fazer o diretório git hub para isso.
instalado vamos em nosso começar instalar algumas coisas: 
abra o direitorio:
cd go-ipfs
depois confira os arquivos que estão la dentro com: 

Seguinte resultado:
 
continuando execute após conferir e executar o seguinte:
sudo .install.sh
usei o ipfs install
Porém, como eu já havia instalado já existe o arquivo, mas continue e execute agora:
npm init
Feito isso, deve ter o seguinte resultado:
 

A identidade de pares abaixo:
Peer identity: 12D3KooWMKCvbNY1haNcZeRW8TXFFjAf5Uz8JP1m7p8N7uAavAcK
Vamos executar:
Ipfs daemon
Deve solicitar a permissão na sua tela e dar o seguinte resultado:
 

Agora abra o prompt de comando do Windows  e execute;
Ipfs swarm peers
Basicamente é o comando que executamos para conectar com o computador. ( não funcionaou no Ubuntu) https://github.com/ipfs/go-ipfs/issues/2540
Aqui tem o site para baixar o ipfs:
https://docs.ipfs.io/reference/http/api/#getting-started
Vamos continuar executando nos dois...
Feito isso, tanto no Ubuntu quanto no Windows agora abra no seu navegador o IPFS DIGITANDO:
Localhost:5001/webui

Dessa forma abrirá o seguinte:

 
No próprio site em PARES termos todas as conexões do mundo:
 
Verifique os arquivos no seu Prompt do Windows executando:
dir
Dentro do diretório go-ipfs insira uma pasta que deseja colocar os arquivos que irão para o IPFS, abaixo o exemplo tanto do Windows quanto do UBUNTU:
na sua linha de comando quando se tem algum projeto: 
ipfs add -r (nome da pasta) no nosso caso é “arquivos”

 
Repare que foi criado os hashs dos documentos.
Use para limpar no Windows e ubuntu:
cls
clear
Vamos no IPFS add na linha de comando https://docs.ipfs.io/reference/cli/#ipfs-add
Repare que consegui adicionar no Ubuntu com o seguinte código:
Ipfs add (nome do arquivo e formato) – devendo estar dentro da pasta selecionada
Dessa forma é gerado um hash específico.
Vamos abrir o hash dentro do IPFS 
 

Cole o hash gerado quando adicionou a pasta ou o documento/arquivo/etc e clique em especionar. 
 
Repare que todos os documentos da pasta existem um hash.
O site com as referencias de códigos a serem executados caso tenha alguma duvida: http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs
Vamos aprender sobre o IPFS pin; http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs-pin
Para abrir o pin de qualquer arquivo através do hash dele digite em seu terminal:
Ipfs pin (hash da pasta) no meu caso: QmZiRADiM2kstpGck6QMcjN4we4cwabVMuEkmWgcugiHUT
Aqui vai indicar de onde é o arquivo e outras informações dele.
Agora vamos aprender a copiar um arquivo no nosso terminal (useiPrompt Windows pq eu executei o daemon no windows)
Crie um diretório ou use algum que exista um arquivo oou etc. e execute o ipfs na pasta inteira ... no meu caso criei um chamado test e inseri as imagens (para criar ou digite mkdir test e depois cd test ou já crie na pasta direto o arquivo test e no terminal abra ele com cd test), dessa forma execute no terminal:
Ipfs add -r test ( que seria o nome da pasta)
Copie o hash da pasta dos arquivos:
QmcsptAs5Y1fVEVCgkJpypwrpetYqwZY3QK44EUapqPAcb
QmT44ervhpu2iZhgY6TZuzHCHW3d4xjHQm4JRk15JHJ3sG
Agora Execute no terminal:
cd test (ou a pasta que vc criou)
agora execute:
dir
ls
deve aparecer os arquivos dentro do diretório e para copiar um deles digite o seguinte:
copy nomedoarquivo.png copied-nomedoarquivo.png
cp nomearquivo.jpg copied-nomearquivo.jpg
Feito isso execute no terminal:
dir
ls
Agora termos o resultado dentro do diretório com o arquivo copiado e etc:
ubuntu
 
windows
 
Agora vamos pegar a pasta toda que geramos o hash e criar uma segunda pasta e nova do mesmo hash. Execute no seu terminal:
Ipfs files cp /ipfs/QmbMHZZxi4kyw3i8TFkgVyGRs4dCgMTf1PKgRbrFkwdWvR /new-(nome pasta)
(pulei essa parte, não consegui mas para aprender vá em http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs-files-cp )
Aprenda a criar uma pasta: 
http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs-files-mkdir
Agora vamos aprender com 
http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs-files-stat

Vamos ler um arquivo em texto no terminal com o hash do documento:
Crie uma pasta com um documento em texto no meu caso fiz ipfs_teste e inseri um arquivo de texto escrito: “ola mundo, sou afonso”. Desse modo vá no seu terminal e adicione a pasta que contem o arquivo:
Ipfs add -r ipfs_teste
Irá ter o seguinte resultado com os hashs
 
Agora vá em sei terminal e digite ipfs cat (hash do arquivo em texto) e terá a mensagem descrita e qual o endereço no caso o “root@LAPTOP-A7IVGKPF”
Agora vamos acessar os arquivos que você adicionou na rede IPFS, lembrando que devemos adiciona-lo no import do localhost que acessamos no nosso navegador, segue exemplo:
 
Repare que adicionei o arquivo ‘jurisprudencia e estudos.docx” ao digitar no terminal:
Ipfs files ls / 
Irá aparecer o seguinte:
 
Ou seja, o hash da pasta e o hash do documento. Para olhar as configurações e hash da pasta digite em seu terminal:
ipfs files stat /pasta
 
E terá os blocos e tipo de documento sendo diretório.
Para partilhar um documento no exemplo do arquivo “Jurisprudencia e estudos.docx” copie e cole no seu navegadro:
https://ipfs.io/ipfs/QmfRSMcNiyZkW4DLxikpUv6MVTkTiBNoPu2UHwxoBXGQdh?filename=Jurisprudencias%20e%20estudo.docx

obs. O diretório/pasta não deve ter “espaço” no prompt de comando tanto do ubuntu quanto do Windows não reconhecem espaço.
Para olhar o hash especifico do arquivo dentro do diretório execute:
ipfs files stat /pasta/copied-7.png
(lembre-se deve ser ipfs com letra minúscula)
Deve aparecer o seguinte resultado:
 

Agora vamos aprende o comenado ipfs files write http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs-files-write
Como escrever textos e criar arquivos, siga o exemplo e escreva o código abaixo:
echo "Ola mundo do Udemy" | ipfs files write --create /pasta/first-file
Execute agora o:
ipfs files ls /pasta
resultados:
 

Vamos descobrir o hash do arquivo criado:
ipfs files stat /pasta/first-file
o resultado do hash: QmUfXouV5yHZALKkU5aZUyDFx9ZUgmERP7k2N5mzxGmXHG
Agora execute:
ipfs cat QmUfXouV5yHZALKkU5aZUyDFx9ZUgmERP7k2N5mzxGmXHG
Resultado:
 
Agora vamos aprender a criar e inserir pastas em outras pastas. http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs-files-mkdir
Crie uma pasta executando em seu terminal:
mkdir udemyIPFS
feito isso, vamos colocar esse novo diretório dentro de outro diretório chamado “pasta” que está no nosso ipfs, execute:
ipfs files mkdir /pasta/udemyIPFS
Agora execute:
ipfs files ls /pasta
Resultado:
 
Vamos aprender o comando ipfs get. http://docs.ipfs.io.ipns.localhost:8080/reference/cli/#ipfs-get
Abra as pastas e arquivos execute para saber quais pastas tem e quer abrir:
ipfs files ls
ipfs files ls /pasta
ipfs files stat /pasta/first-file
Agora terá o hash, no meu caso é: QmUfXouV5yHZALKkU5aZUyDFx9ZUgmERP7k2N5mzxGmXHG
Agora vamos transportar o arquivo acima para um diretório que criamos:
ipfs get -o udemyIPFS/imported-first-file QmUfXouV5yHZALKkU5aZUyDFx9ZUgmERP7k2N5mzxGmXHG
E dará o seguinte resultado:
 
Com isso pegamos o diretório definifo após o “get -o” sendo a udemyIPFS e importamos o arquivo selecionado depois de “/imported-“, ou seja, o first-file e seu hash. Portanto teremos um diretório udemyIPFS com o arquivo imported-first-file.
Para conferir vá no terminal:
cd udemyIPFS
ls
Seguinte resultado:
 
Para conferir o conteudo do arquivo que importamos:
cat imported-first-file
irá aparecer a mensagem que digitamos dentro dele.

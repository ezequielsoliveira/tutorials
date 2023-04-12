# Sobre o arquivo Hosts

O arquivo "hosts" é um arquivo de configuração que armazena informações sobre os endereços IP e seus respectivos nomes de host correspondentes. Ele é usado pelo sistema operacional para mapear nomes de domínio para endereços IP.

Quando um computador tenta se conectar a um servidor ou dispositivo em uma rede, ele precisa saber o endereço IP correspondente para estabelecer a conexão. Em vez de fazer uma consulta de DNS (Domain Name System) toda vez que um endereço é acessado, o sistema operacional primeiro verifica o arquivo "hosts" para ver se o nome de host pode ser resolvido localmente. Se a entrada existir no arquivo "hosts", o sistema usará o endereço IP correspondente. Se não, ele fará uma consulta de DNS para resolver o nome de host.

O arquivo "hosts" é útil para fins de teste e depuração, quando é necessário testar um servidor ou aplicativo localmente sem um nome de domínio registrado publicamente ou quando é necessário redirecionar um endereço para outro endereço IP específico. No entanto, é importante lembrar que as entradas no arquivo "hosts" só têm efeito no computador local e não são compartilhadas com outros computadores na rede.

# Exemplos de uso

- Mapear um nome de host para o endereço "localhost":
  - ```# Arquivo hosts
127.0.0.1   localhost```
> Esse exemplo mapeia o nome de host "localhost" para o endereço IP 127.0.0.1, que é o endereço IP da máquina local.

- Mapear um nome de host para o endereço "www.meusite.com":
  - ```# Arquivo hosts
127.0.0.1   localhost
192.168.0.10   www.meusite.com```
> Esse exemplo mapeia o nome de host "www.meusite.com" para o endereço IP 192.168.0.10. Isso pode ser útil para testar um site em um servidor local antes de fazer o upload para um servidor de produção.

- Mapear um nome de host para sobrepor um endereço existente:
  - ```# Arquivo hosts
127.0.0.1   localhost
192.168.0.10   www.meusite.com
192.168.0.50   www.facebook.com```
> Esse exemplo mapeia o nome de host "www.facebook.com" para o endereço IP 192.168.0.50, que é um endereço endereço IP da rede local. Isso também impede que o navegador acesse o site do Facebook.


# Trabalho realizado nas Semanas #2 e #3

## Identificação

- Vulnerabilidade na biblioteca OpenSSL que permite leitura de memória do servidor remoto.
- Afeta as versões do OpenSSL da 1.0.1 à 1.0.1f em servidores que utilizam SSL(secure socket layer)/TLS(transport layer security.
- Impacta servidores web e serviços que usam HTTPS para criptografia de dados.
- Aplicações vulneráveis mais notáveis: Apache e Nginx. Em risco: e-mail, VPNs e serviços bancários online.

## Catalogação

- Descoberto por uma equipa independente de engenheiros de segurança(Riku, Antti e Matti) na Codenomicon e por Neel Mehta do Google Security em abril de 2014.
- Classificado como grave, com um CVSS de 5.0 devido à exposição de dados sensíveis.
- Não houve bug-bounty associado; foi identificado através de autoridades de segurança.
- A OpenSSL lançou rapidamente um patch (1.0.1g) e recomendações de atualização urgente.

## Exploit

- O exploit conhecido permite que um atacante leia até 64KB de memória do servidor (por hearbeat/conexão), incluindo chaves privadas e dados sensíveis.
- Diversos exploits disponíveis em repositórios de segurança e incluídos em ferramentas de teste.
- Não há automação direta no Metasploit, mas scripts e POCs são amplamente utilizados.
- Explorável sem autenticação (enviado e respondido na fase de handshake), o que aumenta o risco para sistemas expostos.

## Ataques

- Explorada em ataques reais para roubar informações confidenciais, como credenciais e chaves SSL.
- Relatos de vazamento de dados de serviços populares, incluindo o Yahoo, o Flickr e até mesmo servidores governamentais.
- Potencial para causar danos financeiros e comprometer milhões de contas online.   
- Empresas correram para aplicar patches, mas a vulnerabilidade continuou a ser explorada por meses após descoberta. ex.: red hat

## Mais informação
- https://heartbleed.com/
- https://access.redhat.com/security/cve/cve-2014-0160
- https://www.exploit-db.com/exploits/32745
- https://nvd.nist.gov/vuln/detail/CVE-2014-0160
- https://www.yahoo.com/news/why-heartbleed-called-heartbleed-170047727.html?guccounter=1 

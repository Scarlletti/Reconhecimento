## Informações Gerais

* **Atacante:** Kali Linux (máquina virtual configurada em modo NAT)
* **Domínio alvo:** testphp.vulnweb.com
* **Ferramenta utilizada:** theHarvester

---

## Objetivo

O objetivo desta atividade foi realizar a **coleta de informações públicas (OSINT)** relacionadas ao domínio **testphp.vulnweb.com**, com foco na identificação de e-mails, hosts, URLs, ASN e endereços IP que pudessem contribuir para a fase inicial de reconhecimento.

---

## Metodologia

Foi utilizada a ferramenta **theHarvester**, amplamente empregada durante a fase de reconhecimento para coleta de informações a partir de múltiplas fontes públicas.

O comando executado no terminal do Kali Linux foi:

```
theHarvester -d testphp.vulnweb.com -b all
```

Neste comando:

* `-d` define o domínio alvo
* `-b all` instrui a ferramenta a consultar todas as fontes disponíveis

---

## Resultados

A execução da ferramenta não resultou na identificação de endereços de e-mail associados ao domínio analisado. No entanto, foram coletadas outras informações relevantes:

* **ASN identificado:** 1
* **URLs encontradas:** 10
* **Endereço IP:** 1
* **Hosts identificados:** 7

Mesmo sem a coleta de e-mails, os dados obtidos contribuem para o mapeamento da infraestrutura do alvo e podem auxiliar em etapas posteriores do reconhecimento.

---

## Análise

A ausência de e-mails públicos pode indicar boas práticas de segurança por parte da organização, como a não exposição de endereços eletrônicos em fontes indexadas ou mecanismos de proteção contra coleta automatizada.

Por outro lado, a identificação de hosts, URLs, ASN e IP fornece insumos importantes para:

* enumeração adicional de serviços,
* análise de superfície de ataque,
* correlação com outras ferramentas de reconhecimento.

---

## Conclusão

Embora a ferramenta **theHarvester** não tenha retornado endereços de e-mail, os resultados obtidos demonstram sua utilidade na fase de reconhecimento, reforçando que informações indiretas também possuem grande valor durante um processo de pentest.

A coleta e correlação desses dados devem ser combinadas com outras técnicas e ferramentas para uma visão mais completa do ambiente analisado.

---

*Este write-up possui finalidade exclusivamente educacional e foi realizado em ambiente controlado para fins de estudo em segurança ofensiva.*

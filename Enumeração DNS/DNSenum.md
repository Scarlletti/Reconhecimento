## Informações Gerais

* **Atacante:** Kali Linux (máquina virtual configurada em modo NAT)
* **Domínio alvo:** testphp.vulnweb.com
* **Ferramenta utilizada:** DNSenum

---

## Objetivo

O objetivo desta atividade foi realizar a enumeração de DNS do domínio **testphp.vulnweb.com**, buscando identificar possíveis subdomínios públicos que pudessem ampliar a superfície de ataque.

---

## Metodologia

Inicialmente, foi executado o comando padrão do DNSenum no terminal do Kali Linux:

```
dnsenum testphp.vulnweb.com
```

O resultado retornou apenas o endereço IP associado ao domínio principal, não apresentando nenhum subdomínio público.

Diante disso, foi adotada uma abordagem mais abrangente, utilizando uma wordlist nativa do Kali Linux, denominada **dnsmap.txt**, com o intuito de realizar uma enumeração baseada em força bruta.

O comando utilizado foi:

```
dnsenum -f /usr/share/wordlists/dnsmap.txt testphp.vulnweb.com
```

---

## Resultados

Mesmo com o uso de uma wordlist mais extensa, nenhum subdomínio público respondeu às requisições realizadas pela ferramenta.

---

## Conclusão

Com base nos testes realizados, conclui-se que o domínio **testphp.vulnweb.com** não possui subdomínios publicamente expostos ou que estes estão devidamente ocultos por mecanismos de segurança, como configurações restritivas de DNS ou filtragem de consultas.

Este tipo de resultado reforça a importância de combinar diferentes técnicas e ferramentas durante a fase de enumeração, bem como considerar que a ausência de resultados também é uma informação relevante dentro do processo de pentest.

---

*Este write-up tem caráter educacional e foi realizado em ambiente controlado para fins de estudo em segurança ofensiva.*

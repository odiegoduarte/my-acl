# ACLs - CA


## Sectigo / Comodo / USERTrust

A **Sectigo**, **Comodo CA** e **USERTrust** fazem parte da mesma estrutura corporativa e compartilham a mesma infraestrutura de emissão de certificados.

Dessa forma, os domínios abaixo devem ser tratados como um único grupo (**Sectigo**) e liberados em conjunto no proxy.


```text
crl.usertrust.com
ocsp.usertrust.com
crl.comodoca.com  (certificados legados)
ocsp.comodoca.com (certificados legados)
crl.sectigo.com
ocsp.sectigo.com
```

## Entrust

A CA **Entrust** teve seus certificados TLS removidos da lista de autoridades confiáveis do Google Chrome para certificados emitidos a partir de **12 de novembro de 2024**.

Sites que ainda utilizam certificados Entrust afetados podem apresentar avisos de segurança no navegador, independentemente de qualquer bloqueio ou liberação configurada no proxy.


#### 📚 Referências
- [Google Security Blog - Revoga certificados da Entrust no Google Chrome](https://security.googleblog.com/2024/06/sustaining-digital-certificate-security.html)
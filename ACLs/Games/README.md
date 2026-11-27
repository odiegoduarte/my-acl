# ACLs - Games

## Steam

#### Liberação via WPAD

Caso a liberação seja realizada por **WPAD**, é possível liberar o domínio:
```
*.dominio.com
```


#### Portas para autenticação e download de conteúdo
Necessárias para iniciar sessão no Steam e baixar jogos e atualizações.

| Protocolo | Porta(s) | Direção |
|-----------|-----------|---------|
| TCP | 80 (HTTP) | Remota |
| TCP | 443 (HTTPS) | Remota |
| UDP | 27015-27050 | Remota |
| TCP | 27015-27050 | Remota |


#### Cliente Steam
| Protocolo | Porta(s) | Finalidade |
|-----------|-----------|------------|
| UDP | 27000-27250 | Tráfego de jogos |
| UDP | 27031-27036 | Remote Play |
| TCP | 27036 | Remote Play |
| UDP | 4380 | Comunicação do cliente |


#### Servidores dedicados ou Listen Server
| Protocolo | Porta | Finalidade |
|-----------|--------|------------|
| TCP | 27015 | Porta RCON (SRCDS) |
| UDP | 27015 | Tráfego do jogo |


#### Steamworks P2P e Chat de Voz
| Protocolo | Porta(s) | Finalidade |
|-----------|-----------|------------|
| UDP | 3478 | Rede P2P |
| UDP | 4379 | Rede P2P |
| UDP | 4380 | Rede P2P |
| UDP | 27014-27030 | Rede P2P e chat de voz |


#### Observações
- Para ambientes que utilizam **Proxy/WPAD**, recomenda-se permitir os domínios necessários da Valve.
- A maior parte do tráfego do Steam utiliza **UDP**, embora alguns serviços também utilizem **TCP**.
- Os endereços IP pertencem ao **AS32590 (Valve Corporation)**.


#### 📚 Referências
- [Resolução de problemas de conectividade de rede](https://help.steampowered.com/pt/faqs/view/669A-2F68-D1D1-A5EC)
- [Portas necessárias para o Steam
](https://help.steampowered.com/pt/faqs/view/2EA8-4D75-DA21-31EB)
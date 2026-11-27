# ACLs - Acesso Remoto

## AnyDesk

### Portas utilizadas

| Protocolo | Porta(s) | Finalidade |
|-----------|-----------|------------|
| TCP | 80 | Comunicação HTTP |
| TCP | 443 | Comunicação HTTPS |
| TCP | 6568 | Comunicação principal do AnyDesk |
| UDP | 50001-50003 | Recurso Discovery (LAN) |

### Discovery (LAN)

O recurso **Discovery** utiliza os seguintes parâmetros por padrão:

- **Portas UDP:** `50001-50003`
- **Endereço Multicast:** `239.255.102.18`

### Exceções de domínio WPAD
```
*.net.anydesk.com
```

### Observações
- O **AnyDesk** utiliza a porta **6568/TCP** para comunicação com seus servidores.

## TeamViewer

### Portas utilizadas

| Protocolo | Porta(s) | Finalidade |
|-----------|-----------|------------|
| TCP/UDP | 5938 | Porta principal de comunicação |
| TCP | 443 | Comunicação via HTTPS (fallback) |
| TCP | 80 | Comunicação HTTP (fallback) |

### Exceções de domínio WPAD

```
*.teamviewer.com
```

### Portas utilizadas por sistema operacional

| Sistema Operacional | TCP/UDP 5938 | TCP 443 | TCP 80 |
|---------------------|:------------:|:-------:|:------:|
| Windows             | ✅ | ✅ | ✅ |
| macOS               | ✅ | ✅ | ✅ |
| Linux               | ✅ | ✅ | ✅ |
| ChromeOS            | ✅ | ✅ | ✅ |
| iOS                 | ✅ | ❌ | ✅ |
| Android             | ✅ | ✅ | ✅ |
| Windows Mobile      | ✅ | ❌ | ❌ |


### Observações

- O **TeamViewer** prioriza a porta **5938/TCP e UDP**. Caso ela não esteja disponível, utiliza **443/TCP** e, por último, **80/TCP**.


## 📚 Referências

- [AnyDesk](https://support.anydesk.com/knowledge/firewall)
- [TeamViewer](https://www.teamviewer.com/pt-br/global/support/knowledge-base/teamviewer-classic/troubleshooting/ports-used-by-teamviewer/)
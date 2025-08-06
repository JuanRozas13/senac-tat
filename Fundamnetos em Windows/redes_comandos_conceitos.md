
# 📄 Comandos e Conceitos de Redes (Windows)

## 🧪 Comandos utilizados

### `ipconfig`
Exibe as **informações básicas de rede** do computador.
Mostra:
- Endereço IPv4
- Máscara de sub-rede
- Gateway padrão

**Exemplo de saída:**
```
Endereço IPv4. . . . . . . . . . . . . .: 192.168.0.10
Máscara de Sub-rede . . . . . . . . . .: 255.255.255.0
Gateway Padrão . . . . . . . . . . . . : 192.168.0.1
```

---

### `ipconfig /all`
Exibe **todas as informações detalhadas** da conexão de rede.
Inclui:
- Nome do host
- DHCP ativado
- Endereço físico (MAC)
- Servidores DNS
- Data/hora de concessão do IP (DHCP Lease)

---

### `ping www.site.com.br`
Envia pacotes para um site para **testar conectividade** com a rede ou a internet.
Mostra:
- Tempo de resposta (latência)
- Se o site está **acessível**
- Se o **DNS está funcionando**

**Exemplo:**
```
ping www.google.com
```

**Saída esperada:**
```
Resposta de 142.250.78.100: bytes=32 tempo=25ms TTL=116
```

---

## 📚 Conceitos de Redes

### 🔸 DNS (Domain Name System)
É um sistema que **converte nomes de domínio** (ex: `www.google.com`) em **endereços IP** (ex: `142.250.78.100`).  
É como uma **agenda de contatos da internet**: você digita o nome e ele encontra o número (IP).  
Sem o DNS, precisaríamos decorar os IPs de cada site.

---

### 🔸 APIPA (Automatic Private IP Addressing)
É um recurso do Windows que **atribui automaticamente** um IP na faixa `169.254.x.x` quando **não consegue contato com o servidor DHCP**.  
Serve como **recurso de emergência** para comunicação local (LAN), mas **não fornece acesso à internet**.

**Indica problema com:**
- DHCP desativado
- Cabo de rede desconectado
- Falha no roteador

---

### 🔸 DHCP (Dynamic Host Configuration Protocol)
É o **protocolo que distribui IPs automaticamente** para dispositivos em uma rede.  
O servidor DHCP pode ser o **roteador** ou um servidor dedicado.

Ele fornece:
- Endereço IP
- Máscara de sub-rede
- Gateway
- Servidores DNS

**Vantagens:**
- Não precisa configurar IPs manualmente
- Evita conflitos de IP
- Facilita a administração da rede

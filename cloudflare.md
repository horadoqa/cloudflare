# cloudflare

Subir um site com o Cloudflare envolve alguns passos simples, mas importantes. O Cloudflare é uma plataforma de segurança e performance para sites, que oferece CDN (Content Delivery Network), proteção contra ataques DDoS, otimização de desempenho e outros serviços. Aqui está um guia passo a passo para integrar seu site ao Cloudflare:

### Passo 1: Criar uma conta no Cloudflare
1. Acesse o site do Cloudflare: [https://www.cloudflare.com/](https://www.cloudflare.com/).
2. Clique em **"Sign Up"** (Inscrever-se) no canto superior direito.
3. Preencha seus dados para criar uma conta, incluindo e-mail e senha.

### Passo 2: Adicionar seu site ao Cloudflare
1. Após se inscrever e fazer login, você será direcionado para o painel do Cloudflare.
2. Clique em **"Add Site"** (Adicionar Site).
3. Digite o domínio do seu site (por exemplo, `www.seusite.com`) e clique em **"Add Site"**.

### Passo 3: Verificar configurações do DNS
1. O Cloudflare irá escanear os registros DNS do seu site. Isso pode levar alguns minutos.
2. Após a varredura, ele mostrará todos os registros DNS que ele encontrou. Verifique se os registros estão corretos (se você estiver usando um servidor de hospedagem específico ou um serviço, como o cPanel, os registros estarão corretos).
3. Você pode fazer ajustes se necessário, como adicionar ou editar registros de **A**, **CNAME**, **MX**, etc.
   
   **Nota**: O Cloudflare automaticamente adiciona um ícone de nuvem laranja ao lado dos registros DNS que ele está protegendo (esses registros estarão passando pelo Cloudflare). Se a nuvem estiver cinza, significa que o tráfego não passará pela rede do Cloudflare.

### Passo 4: Escolher um plano
1. O Cloudflare oferece vários planos. Para sites pequenos e pessoais, o plano **gratuito** é suficiente.
2. Escolha o plano desejado e clique em **"Confirm Plan"** (Confirmar plano).

### Passo 5: Atualizar os servidores de nomes (DNS) no seu provedor de domínio
1. O Cloudflare fornecerá dois servidores de nomes (NS), por exemplo:
   - `jane.ns.cloudflare.com`
   - `bob.ns.cloudflare.com`
2. Vá até o provedor de domínio onde você comprou seu domínio (ex: GoDaddy, Registro.br, etc.).
3. Acesse a área de gerenciamento de DNS e substitua os servidores de nomes existentes pelos que o Cloudflare forneceu.
4. Salve as alterações. Pode levar até 24 horas para que as alterações se propaguem, mas geralmente é mais rápido.

### Passo 6: Verificar se o site está funcionando com o Cloudflare
1. Após a propagação dos servidores de nomes, o tráfego do seu site passará através da rede do Cloudflare.
2. Você pode verificar o status do seu site no painel do Cloudflare. Ele deve indicar que está protegido e funcionando corretamente.

### Passo 7: Configurações adicionais (opcionais)
Após integrar seu site ao Cloudflare, você pode explorar algumas configurações adicionais para otimizar seu site, como:
- **Regras de firewall**: proteger seu site contra ataques.
- **Desempenho**: habilitar o cache de conteúdo, otimizar imagens e recursos estáticos.
- **SSL**: garantir que seu site esteja funcionando com HTTPS (Cloudflare oferece SSL gratuito).

---

Esse processo configura seu site para usar os serviços de segurança e otimização do Cloudflare. Você pode ajustar as configurações conforme necessário, mas a configuração básica é muito simples e pode ser feita rapidamente.
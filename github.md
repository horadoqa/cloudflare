Para configurar um **domínio personalizado** (como `www.horadoqa.com.br`) no **GitHub Pages**, você precisa seguir alguns passos simples. Vou te guiar no processo.

### 1. **Comprar e configurar o domínio (se ainda não fez isso)**
Se você ainda não tem o domínio `horadoqa.com.br`, você precisa comprá-lo em um provedor de domínios (como **GoDaddy**, **HostGator**, **Registro.br**, entre outros). Após comprar, você terá acesso ao painel de controle onde pode configurar o DNS do seu domínio.

### 2. **Configurar o DNS do seu domínio**
Após ter o domínio, você precisa configurar os **registros DNS** para apontar para o GitHub Pages. Para isso, você precisará adicionar alguns **registros A** ou **CNAME** no painel de controle do seu provedor de domínio.

1. **Adicionar registros A** (para domínios raiz como `horadoqa.com.br`):
   
   Adicione os seguintes registros **A** no painel DNS do seu provedor de domínio (o número IP abaixo é para GitHub Pages):
   - **Host**: `@` ou `horadoqa.com.br` (dependendo do provedor)
   - **Tipo**: A
   - **Valor**: `185.199.108.153`
   - **Valor**: `185.199.109.153`
   - **Valor**: `185.199.110.153`
   - **Valor**: `185.199.111.153`

   Esses registros A apontam o domínio raiz para o GitHub Pages.

2. **Adicionar um registro CNAME** (para o subdomínio `www.horadoqa.com.br`):

   - **Host**: `www`
   - **Tipo**: CNAME
   - **Valor**: `horadoqa.github.io`

   O registro CNAME vai fazer com que o **www.horadoqa.com.br** aponte para o seu repositório no GitHub Pages.

### 3. **Configurar o GitHub Pages no seu repositório**
Agora que o DNS está configurado, você precisa fazer a configuração no repositório do GitHub para reconhecer o domínio personalizado.

1. **Crie o arquivo `CNAME` no repositório**:
   No seu repositório GitHub onde você está hospedando o site (por exemplo, `moon`), crie um arquivo chamado **`CNAME`** (sem extensão). Esse arquivo deve conter apenas o nome do domínio que você deseja usar. No seu caso, o conteúdo do arquivo `CNAME` será:

   ```
   www.horadoqa.com.br
   ```

   O GitHub usará este arquivo para associar o domínio personalizado ao seu repositório.

   Para criar o arquivo `CNAME`:
   - No GitHub, acesse o seu repositório.
   - Clique em **Add file** e selecione **Create new file**.
   - No campo de nome do arquivo, digite `CNAME`.
   - No campo de conteúdo, coloque o seu domínio: `www.horadoqa.com.br`.
   - Clique em **Commit new file**.

2. **Verifique a configuração do GitHub Pages**:
   - Vá para **Settings** do repositório no GitHub.
   - Na seção **GitHub Pages**, em "Custom domain", adicione `www.horadoqa.com.br` (se ainda não estiver lá).
   - Marque a opção **Enforce HTTPS** se possível (isso garante que a conexão seja segura).

### 4. **Aguarde a propagação do DNS**
A propagação do DNS pode levar de **algumas horas até 48 horas** para ser completamente propagada, dependendo do provedor de domínio. Durante esse tempo, o domínio pode não estar acessível imediatamente.

### 5. **Teste seu domínio**
Após a propagação do DNS, você pode acessar seu site através de **http://www.horadoqa.com.br**. Ele deverá redirecionar para o conteúdo do seu repositório GitHub Pages.

---

### Resumo dos passos:
1. **Compre o domínio** e configure os registros DNS no painel de controle do seu provedor de domínio:
   - **Registros A** para o domínio raiz (`horadoqa.com.br`).
   - **Registro CNAME** para o subdomínio `www.horadoqa.com.br` apontando para `horadoqa.github.io`.
   
2. **Crie o arquivo `CNAME`** no seu repositório GitHub com o conteúdo `www.horadoqa.com.br`.

3. **Habilite o GitHub Pages** e insira o domínio no campo de "Custom domain" nas configurações.

4. **Aguarde a propagação do DNS** (pode levar até 48 horas).

Isso deve configurar corretamente seu domínio personalizado no GitHub Pages. Se você encontrar algum erro ou precisar de mais detalhes, me avise!
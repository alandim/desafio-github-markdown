# **Princípios do Git e GitHub**

## **Introdução ao Git**
O Git é um sistema de controle de versão distribuído amplamente utilizado em projetos de software. Ele permite que vários desenvolvedores trabalhem simultaneamente em um projeto, rastreando as mudanças no código e facilitando a colaboração.

### **Principais Conceitos do Git**:
- **Repositório**: Um diretório contendo todos os arquivos do projeto e o histórico completo de todas as alterações.
- **Branch**: Representa uma linha de desenvolvimento separada, permitindo trabalhar em funcionalidades sem impactar a versão principal.
- **Commit**: Um instantâneo do estado atual do código. Cada commit contém uma mensagem descritiva e um identificador único.
- **Merge**: Combina alterações de diferentes branches em um único branch.
- **Pull e Push**: Sincronizam as mudanças entre o repositório local e o remoto. 
  - `Push`: Envia as mudanças locais para o repositório remoto.
  - `Pull`: Atualiza o repositório local com as mudanças do remoto.

---

## **GitHub**
O GitHub é uma plataforma baseada na web que hospeda repositórios Git, oferecendo uma interface amigável e funcionalidades adicionais para facilitar a colaboração.

### **Funcionalidades do GitHub**:
- **Repositórios Públicos e Privados**: Repositórios públicos podem ser visualizados por qualquer pessoa, enquanto os privados são restritos.
- **Issues e Pull Requests**: Ferramentas para discutir, revisar e integrar mudanças em projetos.
- **GitHub Actions**: Automação de fluxos de trabalho para CI/CD (Integração Contínua/Entrega Contínua).
- **GitHub Pages**: Hospedagem gratuita de sites estáticos diretamente a partir de um repositório.

---

## **Autenticação no GitHub**
Com a evolução da segurança, o GitHub deixou de aceitar autenticação por senha para operações Git. A autenticação agora requer **Tokens de Acesso Pessoal (PAT)** ou **chaves SSH**.

### **Tipos de Autenticação**:
1. **Token de Acesso Pessoal (PAT)**: Um token gerado na interface do GitHub que pode ser usado como uma senha.
   - Permite granularidade nas permissões, como leitura/escrita em repositórios específicos.
   - [Como gerar um PAT](https://github.com/settings/tokens)
   
2. **Autenticação via SSH**: Usa um par de chaves (pública e privada) para autenticação segura.
   - Oferece mais segurança e é amplamente utilizada para contribuições frequentes.
   - [Configurar SSH no GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

---

## **Colaboração com Git e GitHub**

A colaboração em projetos com Git e GitHub segue um fluxo básico para garantir que múltiplas pessoas possam contribuir de forma organizada e eficiente.

### **Fluxo de Trabalho de Colaboração**:
1. **Fork e Clone**: 
   - Faça um fork do repositório para sua conta e clone-o localmente.
   - `git clone <url-do-repositório>`

2. **Crie uma Branch**: 
   - Ao adicionar uma nova funcionalidade ou corrigir um bug, crie uma nova branch.
   - `git checkout -b nome-da-branch`

3. **Commit das Alterações**: 
   - Após fazer alterações no código, use `git add .` para preparar os arquivos e `git commit -m "Mensagem descritiva"` para salvar o commit.

4. **Envio das Alterações**: 
   - Envie suas alterações para o repositório remoto com `git push origin nome-da-branch`.

5. **Pull Request (PR)**:
   - No GitHub, crie um **Pull Request** para revisar e mesclar suas alterações na branch principal.

6. **Revisão e Merge**:
   - A equipe revisa o PR e, se aprovado, faz o merge para a branch principal.

---

## **Comandos Úteis**
```bash
# Clonar um repositório
git clone <url-do-repositório>

# Criar uma nova branch
git checkout -b <nome-da-branch>

# Adicionar arquivos para commit
git add <arquivo>  # ou git add .

# Fazer commit das alterações
git commit -m "mensagem do commit"

# Enviar as alterações para o repositório remoto
git push origin <nome-da-branch>

# Fazer pull para sincronizar o repositório local com o remoto
git pull origin main

# Documentação Hackathon - Solução para processamento de vídeos e geração de frames

Este documento fornece uma visão abrangente de todos os repositórios da família de projetos `hackathon-video` e suas respectivas responsabilidades.

## Visão Geral

O projeto hackathon-video está organizado em múltiplos repositórios especializados, cada um responsável por um aspecto específico do sistema:

---

## Repositórios

### 1. **hackathon-video-docs** 📚
- **Linguagem**: Markdown/Documentação
- **Licença**: MIT
- **Responsabilidade**: Hub central de documentação para todo o projeto hackathon-video. Contém diretrizes do projeto, documentação de arquitetura e boas práticas.
- **Repositório**: [postech-group-fiap-188/hackathon-video-docs](https://github.com/postech-group-fiap-188/hackathon-video-docs)

### 2. **hackathon-video-frontend** 🎨
- **Linguagem**: TypeScript
- **Licença**: MIT
- **Responsabilidade**: Aplicação client-side que fornece a interface do usuário para visualização e interação com os vídeos do hackathon. Implantado na Vercel.
- **Homepage**: https://hackaton-video-frontend.vercel.app
- **Repositório**: [postech-group-fiap-188/hackathon-video-frontend](https://github.com/postech-group-fiap-188/hackathon-video-frontend)

### 3. **hackathon-video-processor** ⚙️
- **Linguagem**: TypeScript
- **Licença**: MIT
- **Responsabilidade**: Microsserviço para processamento de vídeos. Responsável por ingestão de vídeos, transcodificação e extração de frames (quadros) de imagem dos vídeos.
- **Repositório**: [postech-group-fiap-188/hackathon-video-processor](https://github.com/postech-group-fiap-188/hackathon-video-processor)

### 4. **hackathon-video-management** 🔧
- **Linguagem**: TypeScript
- **Licença**: Não especificada
- **Responsabilidade**: Serviço de backend responsável por orquestrar os fluxos de vídeo, gerenciar metadados e coordenar a comunicação entre outros serviços.
- **Repositório**: [postech-group-fiap-188/hackathon-video-management](https://github.com/postech-group-fiap-188/hackathon-video-management)

### 5. **hackathon-video-infra** ☁️
- **Linguagem**: HCL (Terraform)
- **Licença**: MIT
- **Responsabilidade**: Repositório de Infraestrutura como Código (IaC). Contém todas as configurações do Terraform para provisionamento e gerenciamento de infraestrutura em nuvem, serviços e recursos necessários para a aplicação.
- **Repositório**: [postech-group-fiap-188/hackathon-video-infra](https://github.com/postech-group-fiap-188/hackathon-video-infra)

### 6. **hackathon-video-infra-db** 🗄️
- **Linguagem**: HCL (Terraform)
- **Licença**: MIT
- **Responsabilidade**: Repositório responsável pela definição e provisionamento da infraestrutura de banco de dados utilizada pelos serviços da aplicação, seguindo o padrão de Infraestrutura como Código (IaC).
- **Repositório**: [postech-group-fiap-188/hackathon-video-infra-db](https://github.com/postech-group-fiap-188/hackathon-video-infra-db)

---

## Visão Geral da Arquitetura

O diagrama completo da arquitetura pode ser acessado no link abaixo:

👉 **Diagrama de Arquitetura:**  
https://drive.google.com/file/d/1UReHKiSJ6oVvaPVv5ZergaCGDy0lQ46c/view?usp=sharing

## 🧩 Manifests

Esse repositório contém os manifests utilizados para implantar a aplicação hello-app por meio do Argo CD.

Este repositório trabalha em conjunto com o repositório [hello-app](https://github.com/VitoriaAmelia/hello-app). Nele você econtra, inclusive, o passo a passo no Argo CD para realizar concluir o processo.

---

### 📁 Arquivos

- **deployment.yaml**
  - Cria o *Deployment* da aplicação
  - Define 3 réplicas do container  
  - Define a imagem Docker gerada no outro repositório 
  - Usa a estratégia de atualização RollingUpdate
  - Expõe a aplicação na porta 80

- **service.yaml**
  - Cria o *Service* para expor a aplicação  
  - Tipo de serviço: NodePort  
  - Porta interna: 80
  - Porta externa (acesso): 30080

  Com isso, será possível acessar no navegador por meio de: `http://localhost:30080/`

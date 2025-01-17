### **Desafio Técnico: Sistema de Criação de Modelos com Montagem de Imagens**  

#### **Descrição Geral**  
Desenvolver um sistema web completo para gerenciar recortes de um produto, permitindo que esses recortes sejam visualizados em camadas que, combinadas, formam uma única imagem final. O sistema deve possibilitar a criação, edição, exclusão e visualização desses recortes, além de permitir o upload de imagens associadas aos recortes e o gerenciamento da ordem de exibição das camadas.  

#### **Objetivo**  
- Criar um sistema eficiente e escalável que permita o armazenamento e organização de recortes de imagens, combinando-os de forma ordenada para formar um modelo final.  
- Utilizar um serviço de armazenamento em nuvem para gerenciar as imagens, gerando links únicos que serão usados na exibição e montagem da imagem final (ex.: Firebase).  
- Implementar uma lógica para gerenciar a ordem de exibição das camadas, garantindo que o resultado final respeite a sobreposição correta dos recortes (Manipulação de css usando o position).  

---

Link do figma: https://www.figma.com/design/jjOiJZD7z2KgD4CRTg4gNf/DESAFIO-TECH?node-id=1003-551&t=WqnmSIe8BWFqu5IK-1

---

### **Fluxo do Sistema**  

1. **Cadastro de Recortes**  
   - Cada recorte deve conter as seguintes informações:  
     - Nome do modelo (ex.: "Aba Frontal").  
     - Ordem de exibição (definindo qual camada aparece por cima).  
     - SKU (código único).  
     - Tipo do recorte (ex.: "aba", "copa"...).  
     - Posição do recorte no produto (ex.: "frente", "traseira").  
     - Tipo do produto (ex.: "boné americano", "boné trucker").  
     - Material do recorte (ex.: "linho").  
     - Cor do material (ex.: "azul marinho").  
     - Link gerado pela cloud (após o upload da imagem).  

2. **Montagem da Key para o Link da Imagem**  
   - Cada recorte armazenado na nuvem terá sua URL gerada seguindo o padrão:  
     ```
     https://cloud_api_img_exemplo.com/assets/[modelo]-[tipo do recorte]-[tecido]-[cor do tecido]
     ```  
   - Exemplo:  
     ```
     https://cloud_api_img_exemplo.com/assets/americano_frente_linho_azul-marinho
     ```  

3. **Visualização e Montagem de Modelos**  
   - Na tela de "Visualização", os recortes cadastrados serão carregados e combinados em camadas.  
   - A ordem das camadas será baseada no campo "Ordem de Exibição" do recorte, sendo a camada com ordem **1** exibida por baixo e as camadas seguintes sobrepostas.  
   - As imagens de todos os recortes devem possuir a mesma proporção para garantir a montagem correta.  

4. **Upload de Imagens**  
   - Implementar funcionalidade de upload de imagens, utilizando um serviço de armazenamento em nuvem (como AWS S3, Cloudinary ou Firebase Storage).  
   - Após o upload, salvar o link gerado no banco de dados para uso nas camadas de montagem.  

---

1. **Tipos de recorte**  
   - frente
   - aba
   - lateral
2. **Modelos disponíveis**
   - Trucker
   - Americano
3. **Tecidos disponíveis**
   - Linho
4. **Cores dos tecidos**
   - Azul marinho
   - Laranja
---

### **Requisitos do Sistema**  

#### **Funcionalidades Básicas**  

1. **Autenticação e Autorização**  
   - Implementar login e logout utilizando JWT.  
   - Garantir que apenas usuários autenticados possam acessar as funcionalidades do sistema.  

2. **CRUD de Recortes**  
   - **Criar:** Permitir o cadastro de novos recortes com as informações detalhadas acima.  
   - **Ler:** Listar todos os recortes, com suporte à paginação.  
   - **Atualizar:** Editar as informações de um recorte existente.  
   - **Excluir:** Remover um recorte, excluindo também sua imagem associada na nuvem.  

3. **Visualização de Modelos**  
   - Permitir a visualização dos modelos completos, montados a partir dos recortes cadastrados.  

4. **Upload de Imagens**  
   - Permitir o upload de imagens associadas aos recortes.  
   - Salvar os links gerados no banco de dados.  

5. **Filtros e Ordenação (Opcional)**  
   - Adicionar funcionalidade para buscar recortes por nome, tipo, ou SKU.  
   - Implementar ordenação por ordem de exibição ou nome do modelo.  

---

#### **Requisitos Técnicos**  

##### **Front-End**  
- **Framework:** React (ou Next.js, se preferir).  
- **Estilização:** Responsividade obrigatória, utilizando TailwindCSS, Styled Components ou CSS puro.  
- **Recursos:**  
  - Interface intuitiva para upload e gerenciamento de recortes.  
  - Tela de visualização com montagem dinâmica das camadas.  

##### **Back-End**  
- **Linguagem:** Node.js (ou outra linguagem, caso preferido).  
- **Banco de Dados:**  
  - Relacional (PostgreSQL/MySQL) ou NoSQL (MongoDB).  
- **ORM:** Prisma, Sequelize ou Mongoose.  
- **Armazenamento de Imagens:** Utilizar serviços como AWS S3, Cloudinary ou Firebase Storage.  
- **Autenticação:** JWT para autenticação e autorização de usuários.  

---

### **Entrega**  

O prazo de entrega é de **7 dias**. Caso tenha dúvidas ou precise de suporte durante o desafio, entre em contato.  

Boa sorte e sucesso no desenvolvimento! 🚀

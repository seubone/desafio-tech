### **Desafio Técnico: Sistema de criação de modelos**

#### **Descrição:**
Desenvolver um sistema web completo para gerenciar várias partes/recortes de um determinado produto e possibilitar a acoplagem desses rescortes e montar uma imagem só. O sistema deve permitir criar, visualizar, editar e excluir recortes, além de incluir funcionalidades para subir imagens dos recortes.

#### **Conceito:**
- Cada recorte reune um grupo de informações que vai montar uma KEY, essa KEY deve ser o nome do arquivo que será armazenado em uma cloud de sua preferência. Armaze o link gerado pela cloud no banco de dados, use esses links para exibir as imagens no montador de produto.
- O intuito do projeto é armazenar vários links de recortes diferentes e na aba de "Visulização" mostrada no figma, esses recorte (todos tem a mesma proporção) deve se unir em "Camadas" diferentes para montar uma só imagem
- Não se esqueça de armazenar a ordem de exibição do recorte, ela irá determinar qual recorte irá aparecer primeiro na camada

#### **Montagem da Key no link:**
> https://cloud_api_img_exemplo.com/assets/aba-frente-americano-linho-azul_marinho
> https://cloud_api_img_exemplo.com/assets/[tipo do recorte]-[posição do boné]-[tipo do boné]-[tecido do boné]-[cor do tecido]

Link do figma: [https://www.figma.com/design/jjOiJZD7z2KgD4CRTg4gNf/DESAFIO-TECH?node-id=1003-551&p=f&t=WqnmSIe8BWFqu5IK-0](https://www.figma.com/design/jjOiJZD7z2KgD4CRTg4gNf/DESAFIO-TECH?node-id=1003-551&t=WqnmSIe8BWFqu5IK-1)

---

### **Requisitos do Sistema**

#### **Funcionalidades Básicas:**
1. **Autenticação e Autorização:**
   - Implementar login e logout utilizando JWT.
   - Permitir apenas usuários autenticados acessarem as rotas do sistema.

2. **CRUD de Produtos:**
   - **Criar:** Adicionar um novo recorte com informações como Nome do modelo, ordem de exibição, sku, link da cloud imagens, tipo do recorte, posição da imagem, tecidos e cor do tecido.
   - **Ler:** Listar todos os recortes com paginação.
   - **Atualizar:** Editar as informações de um recorte.
   - **Excluir:** Remover um recorte.

3. **Upload e Manipulação de Imagens (Front-End):**
   - Permitir o upload de imagens de produtos.
   - Use APENAS as imagens fornecidas no desafio, para realizar o upload

4. **Filtros e Ordenação: (Opcional)**
   - Permitir buscar recortes por nome.

---

#### **Requisitos Técnicos:**

##### **Front-End:**
- **Framework:** React (ou outro framework moderno, caso preferido pelo candidato) ou Next.
- **Design:** Interface responsiva usando CSS puro, TailwindCSS ou styled components.

##### **Back-End:**
- **Linguagem:** Node.js (ou outro, caso preferido pelo candidato).
- **Banco de Dados:** Relacional (PostgreSQL ou MySQL) ou NoSQL (MongoDB).
- **ORM:** Prisma, Sequelize ou Mongoose.
- **Armazenamento de Imagens:** Utilizar um serviço como AWS S3, Cloudinary, ou Firebase Storage (Google).


---

### **Entrega**
O candidato terá 1 semana para concluir o desafio. O código deve ser entregue em um repositório público no GitHub. 

---

Caso precise de mais detalhes ou ajuda para formular o desafio, entre em contato!

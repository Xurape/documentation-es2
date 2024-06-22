<a name="top"></a>

<div align="center">
    <img src="https://i.ibb.co/86C8ByY/ESTG-Simbolo-RGB.png" width="50%"><br/>

# Documentação do projeto ES2

Neste readme, vais encontrar os comandos que vais precisar para trabalhar no projeto **sem qualquer problema**. Para começar deves criar uma *branch* nova [aqui](https://github.com/luisteofilo/estg-esof2-turno-bc) caso sejas do turno B ou C, ou [aqui](https://github.com/luisteofilo/estg-esof2-turno-a) caso sejas do turno A, ou [aqui](https://github.com/luisteofilo/estg-esof2-turno-d) caso sejas do turno D.

</div>

## 😅 Como crio uma branch? 

1. Para criares uma ***branch***, dirige-te à pagina do projeto referente ao teu turno, depois selecionas a opçaõ "master" no canto superior esquerdo, abaixo da topbar e do nome do projeto;

![Imagem1](https://i.ibb.co/BKqvWCy/Screenshot-2024-06-22-at-17-39-08.png)

2. Depois colocamos o nome da nossa ***branch***, que deve ser o nome da feature que vamos desenvolver, por exemplo: `wine_crud`;

![Imagem2](https://i.ibb.co/kHzvKCP/Screenshot-2024-06-22-at-17-40-58.png)

3. Por fim, clicamos em "Create branch" e a nossa ***branch*** está criada.

## 😎 Depois, já posso trabalhar?

Calma! Antes de começares já a trabalhar:

1. Deves fazer um **pull** da tua ***branch*** para o PC. Para isso, deves clicar no botão "Code" e copiar o link que aparece.

2. Depois, no terminal, deves correr o seguinte comando:
```bash
git clone link_que_copiaste
```

> [!TIP]
> Se usares o **Rider** como *IDE*, podes sempre usar o sistema de *Get from Version Control* para clonar o projeto. Para isso, ao abrir o Rider escolhes *Get from Version Control* e colas o link que copiaste anteriormente e clicas em *Clone*.

![Imagem3](https://i.ibb.co/Tw23wG4/imagem.png)

3. Depois de clonares o projeto, deves correr o seguinte comando para mudares para a tua ***branch***:
```bash
git checkout nome_da_tua_branch
```

> [!TIP]
> Se usares o **Rider** como *IDE*, podes, no canto superior esquerdo, clicar no nome da ***branch*** atual e selecionar a tua ***branch*** a partir do *Remote*.

4. Agora sim, podes trabalhar e no final, dás um **commit** e um **push** para a tua ***branch***.

5. Após tudo realizado, crias um **pull request** para a ***branch master*** e pedes ***review*** a algum dos utilizadores presentes no projeto (Não é necessário pedir pois os tech leads serão encarregues disso).

## 📚 Comandos
### ↣ Ligar o projeto

Para ligar o projeto, deves correr:
1. Frontend: http
2. WebAPI: http
   
![Imagem1](https://i.ibb.co/Js4jkpZ/Screenshot-2024-06-22-at-17-27-42.png)

### ↣ Comandos relacionados com a base de dados

Para ligares o base de dados segue o que está [aqui](#-ligar-a-base-de-dados-do-projeto).

#### ✨ Ver as migrations
```bash
dotnet ef migrations list
```

#### ✨ Criar uma migration
```bash
dotnet ef migrations add nome_da_migration
```

#### ✨ Apagar a última migration
```bash
dotnet ef migrations remove
```

#### ✨ Dar run às migrations
```bash
dotnet ef database update
```

### ↣ Relacionado com o Docker

#### ✨ Ligar a base de dados do projeto

- Maneira 1:
```bash
docker compose up --build database
```

- Maneira 2:
```bash
docker compose up -d database
```

#### ✨ Desligar a base de dados

```bash
docker compose down
```

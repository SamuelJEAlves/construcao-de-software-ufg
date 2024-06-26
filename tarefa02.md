## 0. Configure seu nome e e-mail:

git config user.name "seu nome aqui"

git config user.email "nome@qualquercoisa.com"

## 1. Crie uma pasta chamada cs-aulagit

mkdir cs-aulagit

## 2. Entre na pasta e inicie um repositório local

cd cs-aulagit
git init

## 3. Verifique se o repositório foi criado

dir.git
Ou apenas dir

## 4. Remova o repositório

rmdir /s .git

## 5. Crie o repositório novamente

git init

## 6. Crie um arquivo chamado cs.txt e na primeira linha adicione o seu nome.

echo "Samuel Alves" > cs.txt

## 7. Verifique se o status do arquivo é "Untracked files" (Status: work directory)

git status

## 8. Adiciona o arquivo ao "Stage" e verifique o status novamente (agora deve ser "Changes to be committed" - que indica a etapa de Staging area)

git add cs.txt
git status

## 9. Faça o commit desse arquivo no seu repositório local. Coloque o comentário "Arquivo cs.txt criado com o meu nome"

git commit -m "Arquivo cs.txt criado com o meu nome"

## 10. Verifique o status do repositório

git status

## 11. Verifique os arquivos sob o controle do git

git ls-files

## 11. Altere o arquivo cs.txt: inclua uma nova linha com o nome da disciplina.

echo "Disciplina: Construcao de Software" >> cs.txt

## 12. Crie um novo arquivo chamado engenharia-software.txt e no conteúdo dê uma descrição do curso (2 ou 3 linhas).

echo "Curso de Engenharia de Software: O curso prepara profissionais para projetar, desenvolver e manter sistemas de software, abordando desde a concepção até a implementação e manutenção." >> engenharia-software.txt

## 13. Verifique o satus dos dois arquivos e procure entender a diferença

git status

## 14. Verifique os arquivos sob o controle do git novamente (git ls-files). Ambos os arquivos são listados? por que (procure entender e se não souber pesquise/pergunte)?

git ls-files

## 15. Adicione os dois arquivo para "Staged area": 

git add .

## 16. Retorne o arquivo cs.txt para a etapa de Work directory

git reset cs.txt

## 17. Verifique o status e "entenda" que os dois arquivos estão em etapa diferentes (Work Directory e Staged area)

git status

## 18. Adicione no arquivo cs.txt mais uma linha: "INF - Instituto de Informatica"

echo "INF - Instituto de Informatica" >> cs.txt

## 19. "Mova" esse arquivo para Staged

git add cs.txt

## 20. Faça o commit dos dois arquivos com o seguinte comentário: "Definição do Curso de Engenharia de Software do INF"

git commit -m "Definição do Curso de Engenharia de Software do INF"

## 21. Verifique o "log" de mudanças

git log

## 22. Verifique o "log" de mudanças do arquivo "cs.txt"

git log cs.txt

## 23. Altere o arquivo "cs.txt" adicionando a seguinte linha: "UFG - Universidade Federal de Goiás"

echo "UFG - Universidade Federal de Goiás" >> cs.txt

## 24. Verifique a diferença entre a versão "comitada" e a versão atual do arquivo cs.txt

git diff cs.txt

## 25 Adicione o arquivo cs.txt ao Staged area

git add cs.txt

## 26. Volte o arquivo cs.txt para a área de staged. 

git reset eu.txt

## 27. Agora mova o arquivo para a area de Staged e depois faça o commit. Não esqueça o comentário:

git add cs.txt
git commit -m "Adicionada linha sobre a UFG"

## 28. Veja os branches existentes

git branch

## 29. Crie um novo "branch" chamado "develop" e entre nele

git checkout -b develop

## 30. Vejas os branches existentes

git branch

## 31. Faça uma mudança no arquivo "engenharia-software.txt". Adicione uma linha com a carga horaria total do curso.

echo "Carga horária total: 3200 horas" >> engenharia-software.txt

## 32. Crie um outro arquivo com o nome estudo-git.txt e, dentro dele, explique brevemente o comando "git status"

echo "O comando 'git status' é utilizado para verificar o estado atual do repositório Git. Ele exibe informações sobre arquivos não rastreados, arquivos modificados, arquivos na Staging Area e o nome do branch atual." >> estudo-git.txt

## 33. Verifique o status dos arquivos

git status

## 34. Move os arquivos para Staged area e depois faça o commit.

git add .
git commit -m "Adicionadas informações sobre carga horária e sobre git status"

## 35. Mude para a branch master

git checkout master

## 36. Verifique se o arquivo "estudo-git.txt" está na branch master.

git ls-files

## 37. Verifique se a mudança realizada existe no arquivo "engenharia-software.txt". Pesquise/pergunte se não conseguiu entender o motivo da mudança não constar aqui.



## 38. Faça o "merge" das mudanças realizadas no "develop" para a branch "master"

### 38.1 Certifique-se que está na master

git branch

### 38.2. Faça o merge

git merge develop


## 39. Apague a branch "develop"

git branch -D develop

## 40. Verifique se a branch foi excluída

git branch

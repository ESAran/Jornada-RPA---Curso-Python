# RPA Challenge
Versão final com interface, busca de dados na web e preenchimento de formulário. Construção base feita em sala de aula, mantendo a estrutura e incrementando algumas funcionalidades.

## Funcionamento

## Configurações

## Arquivos
### gui.py [📄](https://github.com/ESAran/Jornada-RPA-Curso-Python/blob/main/Funda%C3%A7%C3%B5es/RPA%20Challenge/gui.py)

### challenge.py [📄](https://github.com/ESAran/Jornada-RPA-Curso-Python/blob/main/Funda%C3%A7%C3%B5es/RPA%20Challenge/challenge.py)

### fake_data.py [📄](https://github.com/ESAran/Jornada-RPA-Curso-Python/blob/main/Funda%C3%A7%C3%B5es/RPA%20Challenge/fake_data.py)
Possui a função fake_data para obtenção de dados gerados na Web aleatoriamente para preencher o RPA Challenge.
> #### Imports
>
> Funções dos arquivos *navigation* e *file_manipulation*.
>
> ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/6d32e131-4570-4f0b-837f-04fc2c4bc2d2)

> #### Funções
>
> *fake_data:* tem as variáveis de site e caminho do arquivo, obtém o driver e utiliza das funções dos outros scripts para criar o csv que será importado ao RPA Challenge.
>
> ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/25b302a8-76cf-4ac7-9899-deafb5cc5f20)




### file_manipulation.py [📄](https://github.com/ESAran/Jornada-RPA-Curso-Python/blob/main/Funda%C3%A7%C3%B5es/RPA%20Challenge/file_manipulation.py)
Manipulação de arquivo, leitura e criação de CSV/XLSX
> #### Imports
>
> Utilização de pandas, csv e os.
>
> ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/920ef1b7-4e19-471b-840a-cff36c493e62)

> #### Funções
> O arquivo não tem uma classe definida, mas consta com duas funções.
>
> > *le_dados_challenge:* Faz a leitura de um arquivo CSV/XLSX, salvando as células em variáveis e retornando um vetor que será usado para preencher os campos posteriormente.
> >
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/fe731ebb-c699-4149-939d-7497e6b8594f)
> >
> > *cria_csv e escreve_csv:* Cria e adiciona linhas ao CSV
> > 
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/c7c17e3e-758c-4329-9604-387d5779aa61)




### navigation.py [📄](https://github.com/ESAran/Jornada-RPA-Curso-Python/blob/main/Funda%C3%A7%C3%B5es/RPA%20Challenge/navigation.py)
Arquivo de navegação, funções do site para obter o driver e navegação na página com 3 classes.
> #### Imports
> 
> Utilização da biblioteca Selenium para navegar na Web.
> 
> ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/0d99b444-cd1f-4284-acad-660ebd5bd1c8)

> #### Classe Browser
> 
>  Possui a função chrome_browser que recebe um site por parâmetro e retorna o driver que será usado posteriormente pela biblioteca Selenium.
> > *chrome_browser*
> > 
> >  ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/2e1899db-6094-4635-b253-daf89f2443b1)


> #### Classe PageObjects
> 
> Possui as funções de iniciar(recebendo driver por parâmetro) e executar(recebendo driver e linha) o challenge, juntamente com a função de executar o fake_data.
>
> > *inicia_challenge:* Clica no botão de **Start** da tela inicial do RPA Challenge.
> >
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/bc28d17f-0854-482f-abf5-c5cf6eeb38c0)
> >
> > *executa_challenge:* Idêntifica por **XPATH** os caminhos dos campos à serem preenchidos e envia as informações do vetor "row" recebido por parâmetro.
> > 
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/2e9ced32-1fd5-42de-b342-10b0b0db8d5b)
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/1ffed725-3a96-48b5-bc60-e23dd9a469b9)
> >
> > *executa_fake_data:* Busca por **XPATH** os elementos da página e retorna em um vetor, para posteriormente ser salvo em um csv.
> >
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/12709dae-524d-4653-b9e9-19b0006bd78d)
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/2e84599e-9fa0-47de-aefa-271c3ae69eda)

> #### Classe Waits
>
> Possui funções para aguardar um elemento na tela.
>
> > ![image](https://github.com/ESAran/Jornada-RPA-Curso-Python/assets/105756006/d93557a1-3b12-4781-b04b-ed2d5afe265c)






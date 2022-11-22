**Como consumir uma API em Python:**

Instalar biblioteca request:

-> Abrir prompt   
>pip install requests  
*(instalar a biblioteca requests pelo pip)*

-> No vscode já é possível fazer o import request nos modulos      
>import requests    
*(importar biblioteca para o módulo)*
	
	
-> Logo após, a variável response vai receber uma função de obter dados da biblioteca request, o get:    
>response = requests.get('https://viacep.com.br/ws/01001000/json')      


Para printar o status da requisição:               
>print(response.status_code)            

Para printar o corpo da requisição         
>print(response.text)          

Porém é interessante trazer em formato de json/dicionário pois assim é possível manipular melhor os dados:           
>print(response.json())           

Exemplo de como trazer apenas o campo "logradouro" da requisição:        
>dados_cep = response.json()          
print(dados_cep['logradouro'])    


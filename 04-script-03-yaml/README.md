**Ответ на вопрос №1:**  
Ошибки: нет запятой между элементами "elements", нет закрывающих ковычек у ip второго элемента, ip адресс не в ковычках, ip адрес первого элемента невалидный, ниже верный JSON
```json
    { "info" : "Sample JSON output from our service",
        "elements" :[
            { "name" : "first",
            "type" : "server",
            "ip" : "71.78.22.42" 
            },
            { "name" : "second",
            "type" : "proxy",
            "ip" : "71.78.22.43"
            }
        ]
    }
```
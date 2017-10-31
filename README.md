# numeros-impares 

import asyncio                           
import datetime                          
import random                            
                                         
def Numero_Impares():                    
    yield "Numero"                       
    yield "Impares"                      
                                         
def generar_secuencia():                 
    numero = 1                           
    while True:                          
        yield numero                     
        numero = numero + 2              
                                         
                                         
                                         
if __name__ == "__main__":               
    generador = Numero_Impares()         
    print(next(generador))               
    print(next(generador))               
                                         
    numeros = generar_secuencia()        
    for n in numeros:                    
        print(n)                         
        if n >100:                       
            break                        
                                         
                                         
                                         
                                         
    loop = asyncio.get_event_loop()      

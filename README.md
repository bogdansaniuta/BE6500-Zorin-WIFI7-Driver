# BE6500 Zorin WIFI7 Driver

Driver experimental para adaptador WiFi 7 BE6500 en Linux (Zorin OS).

## ⚠️ Estado
- Experimental
- No oficial
- Basado en rtw89 (DKMS)   

## 🧪 Probado en:
- Zorin OS
- Kernel 6.x

### ⚠️ Advertencia importante

Este driver es **experimental y no oficial**.  
Está diseñado específicamente para el adaptador: 
https://www.tp-link.com/es/home-networking/high-gain-adapter/archer-tbe400uh/
Mirar bien  desplazandose con <  > en la imagen

TP-Link Archer TBE400UH (WiFi 7 USB)
- Probado únicamente en Zorin OS (Core y Pro)
- Funcionando correctamente en entorno real (fibra de alta velocidad)

❗ Si utilizas otro dispositivo o configuración diferente:
- Puede no funcionar correctamente
- Puede generar inestabilidad del sistema
- Puede requerir revertir cambios o reinstalar drivers

👉 No se recomienda su uso si no tienes conocimientos básicos de Linux.

### 🔐 Secure Boot (OBLIGATORIO)

Para que el driver funcione correctamente:

1. Reinicia el equipo  
2. Accede a la BIOS/UEFI  
3. Desactiva temporalmente Secure Boot  

❗ Si no haces esto, el sistema bloqueará el driver.

👉 Tras la instalación, puedes volver a activarlo bajo tu responsabilidad.
### 🧪 Uso bajo responsabilidad

Este software se proporciona **“tal cual”**, sin garantías de ningún tipo.

El autor:
- No garantiza compatibilidad con todos los sistemas  
- No garantiza estabilidad en todos los entornos  
- No se hace responsable de posibles fallos, pérdida de datos o mal funcionamiento  

👉 El uso de este driver es bajo tu propia responsabilidad.

### 🚀 Experiencia personal

En pruebas realizadas:
- Funcionamiento correcto en Zorin OS  
- Conexión estable  
- Alto rendimiento en red  

### 📌 Nota final

Este proyecto está basado en modificaciones del driver rtw89  
y ha sido adaptado para uso específico en este hardware.

Cada sistema puede comportarse de forma diferente.

## 🔧 Descarga y Instalación 
Archivo completo: formato .ZIp 
https://mega.nz/file/5nIS3TJQ#Fq3fG6Hfcqv85XUJFU72SRUWH4kGcq6efbXZxJo4P2Q

En terminal pone  una a una linea por linea  si sois experto ya sabeis como funciona Disfrutenlo..
-----------------TERMINAL ZORIN--------------------------
 ```bash                                               
 unzip "BE6500 Zorin WIFI7.zip"                        
  cd rtw89-1.0                                          
  sudo dkms add .                                       
  sudo dkms build rtw89/1.0                             
  sudo dkms install rtw89/1.0                           
  sudo modprobe rtw89_8852cu_git                        


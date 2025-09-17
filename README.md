# vm-terraform
Pablo Fernando Pineda P. -
 A00395831

Este proyecto utiliza Terraform para crear y gestionar una máquina virtual Linux en Microsoft Azure de forma automatizada.

## ¿Qué hace este proyecto?

Este proyecto despliega una infraestructura completa en Azure que incluye:

### Recursos creados:
- **Máquina Virtual Linux**: Ubuntu 22.04 LTS con tamaño Standard_B1s
- **Red Virtual**: Red privada con rango de direcciones 10.0.0.0/22
- **Subred**: Subred interna con rango 10.0.2.0/24
- **IP Pública**: IP estática para acceso externo a la VM
- **Grupo de Seguridad de Red**: Reglas de firewall que permiten acceso SSH (puerto 22)
- **Interfaz de Red**: Conecta la VM a la red virtual y asocia la IP pública
- **Grupo de Recursos**: Contenedor que organiza todos los recursos

### Características principales:
- **Sistema Operativo**: Ubuntu Server 22.04 LTS
- **Autenticación**: Por contraseña (configurable)
- **Conectividad**: Acceso SSH habilitado desde cualquier IP
- **Almacenamiento**: Disco del SO con almacenamiento estándar LRS
- **Tamaño de VM**: Standard_B1s (1 vCPU, 1 GB RAM) - ideal para pruebas y desarrollo

## Variables configurables

- `prefix`: Prefijo para todos los recursos (default: "example")
- `location`: Región de Azure donde crear los recursos (default: "eastus")
- `admin_username`: Usuario administrador de la VM
- `admin_password`: Contraseña para el usuario administrador

## Outputs

El proyecto proporciona la siguiente información después del despliegue:
- Nombre de la máquina virtual
- Nombre del grupo de recursos
- Dirección IP pública de la VM


## Demostración del Despliegue

### Paso 1: Inicialización de Terraform
```bash
terraform init
```

### Paso 2: Planificación del Despliegue
```bash
terraform plan
```

### Paso 3: Aplicación de la Infraestructura
```bash
terraform apply
```
### Paso 4: Verificación en Azure Portal
#### Azure Portal - VM Creada
<img width="1846" height="466" alt="image" src="https://github.com/user-attachments/assets/477c6068-dbb5-43e9-995f-5aa6fb326da9" />


#### Azure Portal - Recursos
<img width="1566" height="324" alt="image" src="https://github.com/user-attachments/assets/e4107e2f-4419-4ded-8449-acb54a1bfafc" />


### Paso 5: Conexión SSH a la VM
```bash
ssh <admin_username>@<ip_publica>
```
<img width="692" height="827" alt="image" src="https://github.com/user-attachments/assets/aa90d938-1983-4621-a0ab-7360af1cd0b7" />








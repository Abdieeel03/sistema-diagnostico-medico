# 🧑‍⚕️ Sistema de Diagnóstico Médico (Chatbot)

## Clonar el repositorio con los submódulos
Por defecto `git clone` solo te traería el repositorio padre, y los demás repos estarían vacíos.

Para hacer un git clone del repo padre y traer tambien los submódulos se debe ejecutar el siguiente comando:

```bash
git clone --recurse-submodules https://github.com/Abdieeel03/sistema-diagnostico-medico.git
```

Si es que ya hiciste un git clone del repo padre sin el flag `--recurse-submodules` entonces puedes ejecutar el siguiente comando después para actualizar los submódulos:

```bash
git submodule update --init --recursive
```

## Configurar repositorios con SSH (opcional)

Por defecto, el proyecto utiliza URLs HTTPS para facilitar la clonación en cualquier entorno.

Si tienes configuradas claves SSH para GitHub y prefieres utilizarlas, ejecuta los siguientes comandos después de clonar el proyecto:

### Repositorio principal

```bash
git remote set-url origin git@github.com:Abdieeel03/sistema-diagnostico-medico.git
```

### Submódulos

```bash
cd diagnostico-prologEngine
git remote set-url origin git@github.com:Abdieeel03/diagnostico-prologEngine.git

cd ../diagnostico-pythonConversationEngine
git remote set-url origin git@github.com:Abdieeel03/diagnostico-pythonConversationEngine.git

cd ../diagnostico-scalaBackendAPI
git remote set-url origin git@github.com:Abdieeel03/diagnostico-scalaBackendAPI.git

cd ../diagnostico-frontendChatbot
git remote set-url origin git@github.com:Abdieeel03/diagnostico-frontendChatbot.git

cd ..
```

### Verificar configuración

```bash
git remote -v

git -C diagnostico-prologEngine remote -v
git -C diagnostico-pythonConversationEngine remote -v
git -C diagnostico-scalaBackendAPI remote -v
git -C diagnostico-frontendChatbot remote -v
```

Las URLs mostradas deberían comenzar con:

```text
git@github.com:
```

lo que indica que Git utilizará autenticación mediante claves SSH.

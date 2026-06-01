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

* mkdir <имя папки>
* touch <имя файла>
* git init
* git status
* git add -all
* git commit -m 'Мой первый коммит!'
* git log 
* создание репозитория на GitHub
* привязка локального к удаленному
# создание ключа
* cd ~
* ls -la .ssh/ # вывели список созданных ключей 
* ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" 
* ls -a ~/.ssh 
* скопировать содержимое ключа в буфер обмена:
clip < ~/.ssh/id_ed25519.pub 
*  Перейдите на GitHub и выберите пункт Settings (англ. «настройки») в меню аккаунта.
В меню слева нажмите на пункт SSH and GPG keys.
В открывшейся вкладке выберите New SSH key (англ. «новый SSH-ключ»).
В поле Title (англ. «заголовок») напишите название ключа. Например, Personal key (англ. «личный ключ»).
В поле Key type (англ. «тип ключа») должно быть Authentication Key (англ. «ключ аутентификации»).
В поле Key скопируйте ваш ключ из буфера обмена.
* Проверьте правильность ключа с помощью следующей команды.
$ ssh -T git@github.com 
* Привязать удалённый репозиторий к локальному — git remote add 
Перейдите на страницу удалённого репозитория, выберите тип SSH и скопируйте URL. Кнопка справа позволит сделать это мгновенно.
git remote add origin git@github.com:%ИМЯ_АККАУНТА%/first-project.git 
*Убедиться, что репозитории связаны 
git remote -v
* Отправить изменения на удалённый репозиторий
git push
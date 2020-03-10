# Flutter

---

## Instalação

---

- Clonar repositório

      https://github.com/flutter/flutter.git -b stable

- Configurações de Path:

      export ANDROID_HOME="$HOME/Android/Sdk"
      export PATH="$PATH:$ANDROID_HOME/emulator"
      export PATH="$PATH:$ANDROID_HOME/tools"
      export PATH="$PATH:$ANDROID_HOME/tools/bin"
      export PATH="$PATH:$ANDROID_HOME/platform-tools"
      export PATH="$PATH:$HOME/flutter/bin"

- Configurações Android:

  - download android studio
  - download de bibliotecas adicionais no ubuntu

          sudo apt install \
          cpu-checker \
          qemu-kvm \
          libvirt-bin \
          ubuntu-vm-builder \
          bridge-utils \
          ia32-libs-multiarch \
          adb

  - configurações adicionais de usuario no ubuntu

    sudo adduser douglas-paz kvm
    sudo chown douglas-paz /dev/kvm

  - Instalar sdk
  - Instalar emulator (for android license and sdk required)
  - Marcar opção:
    - "Android sdk tool (obsolete)" no menu sdk tool (desmarcar hide obsolete packages for show)
  - Atualização das configurações finais
    /home/douglas-paz/Android/Sdk/tools/bin/sdkmanager --update

- Checagens de instalação final:
  - flutter
  - flutter precache
  - flutter doctor -v
  - fluter doctor --android-licenses

---

## Caracteristicas

---

- tudo é widget
- aplicacoes construidas em árvores de widget
- atomic design
- ui em codigo
- tudo é dart, mas se precisar dá pra usar o kotlin e o swift em uns pedacinhos...
- transpila para kotlin e/ou para swift para rodar nativo
- widgets não são transpilados, a interface grafica é feita pixel por pixel pelo skia

---

## Estado

---

stateless:

- customizado a partir dos parametros
- assim que renderizado o estado definido não muda
- quando os parametros mudam externamento o componente é renderizado novamente
- só atualiza a interface grafica por interferencia externa
  statefull:
- adicionalmente o widget contem um estado interno que quando atualizado pode renderizar a interface grafica novamente

comunicacao-direta:

- o pai passa diretamente ao filho a informação que ele precisa para ser renderizado
- passagem de parametros para o componente filho via construtor

comunicacao-indireta:

- o filho sinaliza ao pai uma alteração de dados e transmite os dados ao pai
- chamada de uma função de callback que altere o estado da aplicação

---

## Widgets

---

### Layout:

#### Container:

- Uso
  - Perfeito para alinhamento e estilo personalizado
- caracteristicas:
  - aceita um filho
  - alinhamento flexivel
  - estilo
  - largura flexivel (padrao = largura do filho)

#### column-row:

- Uso
  - Quando os widgets estiverem próximos ou acima um do outro
    caracteristicas:
  - aceita lista de filhos
  - alinhamento flexivel
  - sem estilo
  - sempre ocupa todo o escaço disponivel (largura = column, altura = row)

### Listas:

#### listview

- lista

#### gridview:

- grade

#### listTitle

- elemento para ser listado

### Conteudo:

#### text

#### image

#### icon

### input:

#### textField

#### raisedButton

#### flatButton

#### gestureDetector

#### InkWell

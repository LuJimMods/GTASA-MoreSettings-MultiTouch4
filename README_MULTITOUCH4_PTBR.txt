Patch: botão JPatch MultiTouch4 no menu do More Settings

O que foi alterado:
- main.cpp agora cria um item clicável no menu Game:
  "JPatch MultiTouch4"
- Ao mudar OFF/ON, ele salva em:
  net.rusjj.jpatch.ini
  [Gameplay]
  MultiTouch4=0 ou 1

Observação:
- O JPatch provavelmente lê MultiTouch4 ao iniciar. Se você mudar no menu e não aplicar na hora, feche e abra o jogo.

Como compilar:
1. Instale Android NDK no PC.
2. Edite ndkpath.txt ou use ndk-build diretamente.
3. Na pasta do projeto, rode:
   ndk-build NDK_PROJECT_PATH=. APP_BUILD_SCRIPT=Android.mk NDK_APPLICATION_MK=Application.mk
4. Pegue a lib gerada em:
   libs/armeabi-v7a/libmoresettings.so
5. Substitua no AML:
   mods/libMoreSettings.so

Seu APK/mod é 32-bit, então o ABI já está em armeabi-v7a.

# OrganizaDia — Android

Aplicativo offline de tarefas e compromissos. Cadastra título, prazo, categoria, prioridade e observações; permite editar, excluir, concluir, pesquisar e filtrar; destaca tarefas atrasadas; preserva os dados no aparelho pelo armazenamento local da WebView; exporta backup pelo menu de compartilhamento do Android e importa backup JSON colado no app. Não pede conta nem acessa internet.

## Criar o APK

1. Crie um repositório vazio no GitHub e envie o conteúdo deste ZIP para a raiz, **incluindo a pasta `.github`**.
2. Em **Actions**, abra **Gerar APK Android** e escolha **Run workflow**. Um push também inicia a compilação.
3. Quando a execução terminar, baixe **OrganizaDia-APK** na seção **Artifacts** e extraia o arquivo `app-debug.apk`.
4. Instale esse APK no celular. No Android, permita a instalação pelo app usado para abrir o arquivo quando aparecer a solicitação.

O workflow usa Java 17, Gradle 8.9 e Android Gradle Plugin 8.7.3. O APK é de depuração para que a WebView apareça em `chrome://inspect/#devices` durante a atividade PPDM2.

## Dados e backup

Os dados são salvos somente neste aparelho. Limpar os dados ou desinstalar o app pode apagá-los. Use **Backup e restauração → Compartilhar backup** antes disso. Para restaurar, copie o texto JSON recebido, cole no campo do app e toque **Importar tarefas**. A importação não substitui as tarefas existentes com o mesmo identificador. O backup inclui as observações, então escolha com cuidado onde compartilhá-lo.

## Entrega prática PPDM2

Com o app aberto no celular, habilite a depuração USB, conecte um cabo de dados e autorize o computador. No Chrome do computador, abra `chrome://inspect/#devices`; a WebView do OrganizaDia deve aparecer. O professor solicita o print da inspeção e a foto real da bancada. Essas imagens precisam ser capturadas com seus aparelhos.

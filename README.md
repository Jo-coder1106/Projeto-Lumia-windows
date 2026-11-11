# LumIA Java para Windows

Versão de referência: **LumIA Java v0.6 Revisado**. Este repositório é exclusivo do aplicativo Java/Windows. O projeto web fica em [Jo-coder1106/Lumia-Web](https://github.com/Jo-coder1106/Lumia-Web).

## Gerar executáveis Windows

O workflow **Build LumIA Windows EXE** compila com JDK 17 e empacota:
- `LumIA.exe`: aplicativo desktop Swing.
- `LumIA-Servidor-Demo.exe`: servidor local de demonstração com banco H2.

Após cada push na `main`, baixe o pacote em **Actions → Build LumIA Windows EXE → Artifacts**. Para publicar também em **Releases**, crie uma tag `v0.6.1`; o workflow anexará `LumIA-Windows-v0.6.1-x64.zip` à release.

## Executar

1. Extraia o ZIP completo.
2. Abra `LumIA-Servidor-Demo.exe` e aguarde a inicialização.
3. Abra `LumIA.exe`.
4. O modo demo usa dados fictícios e o banco H2 em `demo-data`. Não use dados reais.

O pacote não incorpora a chave privada do Gemini nem o arquivo de logins. Para o modo MariaDB, use a distribuição de código e configure as variáveis de ambiente conforme `LEIA-ME.md`.

## Projetos relacionados

- Aplicativo Java/Windows: este repositório.
- Aplicação web: https://github.com/Jo-coder1106/Lumia-Web

**Observação:** o executável é gerado pelo runner Windows do GitHub Actions. O ambiente de desenvolvimento desta sessão é Linux e não consegue produzir um PE/EXE Windows nativo localmente.

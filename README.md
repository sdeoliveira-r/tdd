# Technical Design Document (TDD) - Exportar Propostas como PDF e DOCX

**Versão:** 1.0

**Data:** 07/05/2025

**Autor:** Rafael

**Revisores:** Equipe de Desenvolvimento

**Projeto:** TheFuture



## 1. Objetivo

Implementar a capacidade de exportar propostas (geradas por IA ou criadas manualmente) para os formatos PDF e/ou DOCX, utilizando um layout de marca predefinido. O objetivo é garantir consistência visual nas entregas e aprimorar a comunicação profissional com os clientes.

## 2. Escopo

- Inclui:
  - Ícone de exportação na tela de edição da proposta;
  - Modal para seleção de formato (PDF e/ou DOCX);
  - Geração de arquivos com layout padrão predefinido;
  - Suporte a download e envio por e-mail;
  - Compatibilidade com dispositivos móveis e desktops.

- Não inclui:
  - Integração com APIs externas para armazenamento de arquivos.
  - Personalização de layout por usuário (além do padrão da marca predefinido anteriormente).

## 3. Descrição Técnica

1. Adicionar ícone de exportação ao lado do ícone de edição da proposta.
2. Abrir modal ao clicar no ícone de exportação, com seleção de formatos (PDF e/ou DOCX).
3. Renderizar proposta como HTML no cliente ou servidor, seguindo o layout padrão predefinido.
4. Sugestão de bibliotecas para gerar arquivos:
   - Gerar PDF: Puppeteer, pdf-lib, jsPDF
   - Gerar DOCX: npm docx, PandaDoc (opcional viabilizar custos)
5. Permitir download imediato e envio por e-mail da proposta em PDF e/ou DOCX direto do modal.
6. Garantir compatibilidade com desktops, dispositivos móveis e responsividade.
7. Validar desempenho, compatibilidade e robustez da implementação.

## 4. Critérios de Aceitação

- O ícone de exportação está presente e funcional ao usuário.
- Modal permite seleção da proposta no formato PDF e/ou DOCX.
- Arquivos seguem layout da marca predefinido.
- Propostas incluem: cabeçalho, cliente, itens, notas, rodapé.
- Funcionalidade responsiva em desktop e mobile.
- Suporte a download e envio por e-mail.
- Código otimizado, validado e revisado.

## 5. Riscos ou Dependências

- Dependência de bibliotecas externas para geração de arquivos (viabilizar custos).
- Riscos de inconsistência visual entre formatos.
- Compatibilidade com navegadores e dispositivos móveis.
- Configuração de serviço de e-mail.

## 6. Tópicos Adicionais Importantes

- **Tratamento de Erros:** Definir como os erros durante o processo de exportação serão tratados e como o usuário será notificado.
- **Segurança:** Considerar aspectos de segurança, especialmente se informações sensíveis forem incluídas nas propostas e enviadas por e-mail.
- **Acessibilidade:** Garantir que os arquivos PDF gerados sejam acessíveis seguindo as diretrizes de acessibilidade para documentos PDF.

## 7. Histórico de Versões

| Versão | Data       | Alterações                      | Autor         |
|--------|------------|----------------------------------|---------------|
| 1.0    | 07/05/2025 | Criação inicial do documento     | Rafael  |

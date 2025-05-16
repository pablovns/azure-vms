# 📘 Guia Prático: Criação e Configuração de Máquinas Virtuais no Azure

## 🛠️ 1. Criando uma VM no Portal do Azure

### Etapas Básicas:
1. Acesse o [Portal do Azure](https://portal.azure.com).
2. Navegue até **Máquinas Virtuais** e clique em **Criar**.
3. Preencha as informações necessárias:
   - **Assinatura** e **Grupo de Recursos**.
   - **Nome da VM**, **Região** e **Imagem do SO** (ex: Windows Server 2022).
   - **Tamanho da VM** conforme a carga de trabalho esperada.
   - **Nome de usuário** e **método de autenticação** (senha ou chave SSH).
4. Configure as opções de **Disco**:
   - Escolha entre SSD Premium, SSD Padrão ou HDD Padrão.
   - Adicione discos de dados conforme necessário.
5. Defina as configurações de **Rede**:
   - Selecione ou crie uma **Rede Virtual** e **Sub-rede**.
   - Configure o **Endereço IP Público** e o **Grupo de Segurança de Rede (NSG)**.
6. Revise as configurações e clique em **Criar** para implantar a VM.

> ℹ️ Para mais detalhes, consulte o [Guia de Criação Rápida de VM no Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal).

---

## 🧩 2. Configurações Adicionais e Gerenciamento

### 🔄 Anexar Discos de Dados:
- Acesse a VM no portal.
- Vá para **Discos** > **Criar e anexar um novo disco**.
- Configure o tamanho e tipo do disco, e clique em **Salvar**.

> 🔗 Referência: [Anexar Disco Gerenciado a uma VM](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/attach-managed-disk-portal).

### 🧰 Gerenciamento com Windows Admin Center:
- Permite gerenciar a VM sem necessidade de RDP ou PowerShell.
- Funcionalidades incluem:
  - Gerenciamento de arquivos e compartilhamentos.
  - Monitoramento de desempenho.
  - Gerenciamento de usuários e grupos locais.
  - Acesso ao PowerShell integrado.

> 🔗 Saiba mais: [Gerenciar VMs com Windows Admin Center](https://learn.microsoft.com/pt-br/windows-server/manage/windows-admin-center/azure/manage-vm).

---

## 🔒 3. Práticas Recomendadas de Segurança

- **Atualizações Regulares**: Mantenha o sistema operacional e aplicativos atualizados.
- **Controle de Acesso**: Utilize o Azure Active Directory e atribua permissões mínimas necessárias.
- **Criptografia**:
  - Ative a criptografia de discos com o Azure Disk Encryption.
  - Utilize o Azure Key Vault para gerenciamento de chaves.
- **Monitoramento**:
  - Habilite o Azure Monitor e o Microsoft Defender para Nuvem.
  - Configure alertas para atividades suspeitas.

> 🔗 Consulte: [Melhores Práticas de Segurança para VMs no Azure](https://learn.microsoft.com/en-us/azure/security/fundamentals/iaas).

---

## 📈 4. Monitoramento e Otimização

- **Azure Monitor**: Coleta métricas e logs para análise de desempenho.
- **Log Analytics**: Permite consultas avançadas sobre os dados coletados.
- **Azure Advisor**: Fornece recomendações para otimizar custos, desempenho e segurança.

> 🔗 Mais informações: [Práticas Recomendadas para Monitoramento de VMs](https://learn.microsoft.com/en-us/azure/azure-monitor/vm/best-practices-vm).

---

## 💡 Dicas Finais

- **Automatização**: Utilize scripts ARM, Azure CLI ou PowerShell para automatizar a criação e configuração de VMs.
- **Backups**: Configure backups regulares com o Azure Backup.
- **Redundância**: Implante VMs em conjuntos de disponibilidade para alta disponibilidade.
- **Custos**: Monitore o uso de recursos e ajuste tamanhos de VMs conforme necessário para otimizar custos.

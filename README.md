# Armazenamento no Azure

O armazenamento no Azure é uma solução de nuvem escalável e segura que oferece várias opções para armazenar dados, atender diferentes casos de uso e necessidades de negócios, como backup, recuperação, arquivamento, análise, entre outros. Abaixo, uma visão detalhada sobre as principais ofertas e aspectos do armazenamento no Azure:

## Azure Storage Account
Uma **conta de armazenamento no Azure** é o contêiner que abriga diferentes tipos de serviços de armazenamento. Ela fornece uma maneira unificada de gerenciar e acessar recursos de armazenamento, incluindo blobs, arquivos, filas e tabelas. Existem diferentes tipos de contas de armazenamento:

- **General-purpose v2**: Suporta os serviços mais recentes e é recomendada para a maioria dos cenários.
- **Premium storage**: Oferece alta performance para cargas de trabalho críticas, como aplicações que requerem baixa latência.

## Tipos de Armazenamento
O Azure oferece diferentes tipos de armazenamento para atender diversas necessidades de desempenho e custo:

### Blob Storage
O **Blob Storage** é utilizado para armazenar grandes volumes de dados não estruturados, como imagens, vídeos, backups e arquivos de logs. Existem três tipos de blobs:

- **Blobs de blocos**: Ideais para armazenar arquivos de dados grandes, como imagens e documentos. Dividem os dados em blocos que podem ser carregados ou modificados separadamente.
- **Blobs de anexos (Append blobs)**: Usados principalmente para logs de auditoria e arquivos que são atualizados regularmente com a adição de dados no final.
- **Blobs de páginas**: Projetados para armazenar arquivos de acesso aleatório e são usados frequentemente como discos para máquinas virtuais.

### Discos Gerenciados (Managed Disks)
Os **Discos Gerenciados no Azure** são discos virtuais que podem ser anexados a máquinas virtuais. Eles fornecem diferentes tipos de discos para atender a uma variedade de cargas de trabalho:

- **Standard HDD**: Discos baseados em HDD para cargas de trabalho leves.
- **Standard SSD**: Melhor opção de desempenho que HDDs, usados para cargas de trabalho que requerem maior performance.
- **Premium SSD**: Para cargas de trabalho críticas que exigem alta velocidade de leitura e gravação com baixa latência.
- **Ultra Disk**: Para cargas de trabalho de missão crítica que demandam taxas extremamente altas de IOPS e baixa latência.

### File Storage (Azure Files)
O **Azure Files** oferece armazenamento de arquivos como um compartilhamento de rede na nuvem. Ele é compatível com os protocolos SMB e NFS, facilitando o acesso a arquivos via rede por diferentes dispositivos e sistemas operacionais. Pode ser montado em VMs do Azure ou em servidores locais, permitindo compartilhamento de dados entre várias instâncias.

### Filas
O **Queue Storage** é um serviço que permite o armazenamento de grandes quantidades de mensagens que podem ser acessadas de forma assíncrona por diferentes componentes de uma aplicação. É ideal para o gerenciamento de tarefas ou fluxos de trabalho em larga escala, permitindo comunicação eficiente entre componentes distribuídos.

### Tabelas
O **Table Storage** oferece uma solução de armazenamento NoSQL para dados estruturados com esquema flexível, adequado para grandes volumes de dados, como logs, sensores e outros registros. É altamente escalável e ideal para armazenar milhões de registros de forma simples e acessível.

## Classes de Acesso (Access Tiers)
O **Azure Blob Storage** oferece diferentes classes de acesso para otimizar os custos com base na frequência com que os dados são acessados:

- **Hot**: Para dados acessados com frequência. Oferece o melhor desempenho, mas com custo de armazenamento mais elevado.
- **Cool**: Para dados que são acessados com menos frequência (por exemplo, uma vez por mês). O custo de armazenamento é mais baixo, mas o custo de recuperação é maior.
- **Archive**: Para dados raramente acessados, como arquivos de longo prazo e backup. O custo de armazenamento é extremamente baixo, mas os dados precisam ser "reidratados" antes de serem acessados, resultando em maior tempo e custo para recuperação.

## Redundância de Dados
O Azure oferece várias opções de redundância para garantir alta disponibilidade e resiliência dos dados:

- **Locally Redundant Storage (LRS)**: Replica os dados três vezes dentro de uma única região, garantindo alta disponibilidade local, mas sem proteção contra falhas regionais.
- **Zone-Redundant Storage (ZRS)**: Armazena os dados em três zonas diferentes dentro de uma região, proporcionando maior proteção contra falhas em zonas específicas.
- **Geo-Redundant Storage (GRS)**: Replica os dados em duas regiões separadas geograficamente, garantindo resiliência em caso de desastres regionais.
- **Read-Access Geo-Redundant Storage (RA-GRS)**: Oferece a mesma redundância do GRS, mas permite o acesso de leitura aos dados replicados na região secundária, aumentando a disponibilidade.

## Segurança no Armazenamento
A segurança dos dados no Azure Storage é uma prioridade. Algumas das principais funcionalidades de segurança incluem:

- **Criptografia em repouso (Encryption at Rest)**: Todos os dados armazenados no Azure são automaticamente criptografados, usando chaves gerenciadas pelo Azure ou pelo cliente.
- **Criptografia de dados em trânsito**: Para proteger os dados enquanto eles trafegam entre o cliente e o serviço de armazenamento.
- **Azure Active Directory (Azure AD)**: Integração para controle de acesso baseado em identidade (IAM), permitindo que os administradores definam permissões granulares para usuários e aplicações.
- **Firewalls e redes virtuais**: Permitem restringir o acesso aos dados, garantindo que apenas endereços IP ou redes específicas possam acessar os recursos de armazenamento.

## Gerenciamento e Monitoramento
O Azure oferece várias ferramentas para gerenciamento e monitoramento do armazenamento, permitindo que os administradores acompanhem o desempenho e o uso:

- **Azure Monitor**: Para monitorar métricas e diagnósticos de performance dos recursos de armazenamento.
- **Azure Advisor**: Recomendações de otimização de custos e desempenho com base no uso.
- **Azure Storage Explorer**: Uma ferramenta que permite explorar e gerenciar os dados de armazenamento localmente ou na nuvem.

## Backup e Recuperação
O Azure fornece soluções robustas para backup e recuperação, garantindo a continuidade dos negócios:

- **Azure Backup**: Para a criação de backups automáticos de VMs, bancos de dados e arquivos.
- **Snapshots**: Para criar cópias pontuais de discos gerenciados, facilitando a recuperação rápida em caso de falhas.

## Databox

O **Azure Data Box** é um serviço oferecido pela Microsoft Azure para facilitar a transferência de grandes quantidades de dados de maneira rápida e segura para a nuvem. Ele é ideal para organizações que precisam mover grandes volumes de dados, mas que enfrentam limitações em suas redes, como baixa largura de banda ou custos elevados para transferências de dados pela internet. O Data Box usa dispositivos físicos para transportar dados, o que permite evitar a transferência via rede e, em muitos casos, acelera o processo.

### Características e Funcionalidades do Azure Data Box

**Dispositivos Físicos de Armazenamento**  
O Data Box é um dispositivo físico de armazenamento fornecido pela Microsoft. Após solicitar o Data Box, o dispositivo é enviado para a organização, que pode transferir seus dados localmente para o dispositivo, e, em seguida, ele é devolvido à Microsoft para que os dados sejam carregados diretamente no Azure.

**Capacidade de Armazenamento**  
Existem diferentes opções de dispositivos, cada um com capacidades de armazenamento específicas:

- **Azure Data Box**: Capacidade de até 80 TB de dados. Ideal para grandes transferências.
- **Data Box Disk**: Uma opção menor, com discos de até 7 TB cada, sendo possível usar até cinco discos para um total de 35 TB.
- **Data Box Heavy**: Para cenários de transferência em massa, com capacidade de até 800 TB.

## AzCopy

O **AzCopy** é uma ferramenta de linha de comando desenvolvida pela Microsoft para facilitar a transferência eficiente de dados entre o armazenamento local e os serviços de armazenamento do Azure, como Azure Blob Storage, Azure File Storage, e Azure Table Storage. Ele é projetado para ser altamente otimizado para transferências em larga escala e pode lidar com grandes volumes de dados com facilidade.

### Características e Funcionalidades do AzCopy
Transferência de Dados Rápida:
O AzCopy utiliza técnicas avançadas de otimização para garantir que os dados sejam transferidos rapidamente. Isso inclui a transferência paralela de arquivos, que permite que vários arquivos sejam enviados ou recebidos simultaneamente, aproveitando ao máximo a largura de banda disponível.

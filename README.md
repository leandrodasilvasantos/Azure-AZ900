# Azure-AZ900

## 1. Overview

---

Podemos ter 

1. processamento (Virtual Machines)
2. Rede 
3. Armazenamento

Tudo na nuvem.

Podemos ter uma **nuvem privada → não divide por ninguém,** não fornece acesso aos usuários fora da organização.

Microsoft Azure → nuvem pública → tem vários clientes em vários lugares do mundo, pra quem quiser pagar.

Nuvem híbrida → pode ser a implementação do datacenter da empresa (privada), com um serviço pago público como o da azure, existe também casos de multi cloud, que possui diversos serviços de nuvem como AWS, Azure etc… Mais o datacenter privado da empresa.

## 2. Comparação de modelos de nuvem

---

Nuvem pública → Cloud, Azure

1. depende o quanto vai pagar, NÃO É NA HORA, vai ter o acesso e dependendo do consumo etc, vai pagando lá na frente.
2. Os aplicativos podem ser provisionados e desprovisionados rapidamente. (se algo der errado, pode excluir rapidamente para não haver cobranças)
3. Paga apenas por o que utiliza. (PAGA CONFORME O USO)

Nuvem privada → Ambiente físico

1. A organização tem controle total
2. São responsáveis pela manutenção e atualização.

**→ Despesas de capital (CapEx)**

- Gasto inicial de dinheiro em infraestrutura física.
- As despezas do CapEx têm um valor que se reduz com o tempo (primeiro compra as máquinas tudo, valor ALTO, depois é apenas LUZ, ETC… se reduz)

**→ Despesas operacionais (OpEx)**

- Gasta com produtos e serviços conforme o necessário, paga o que usa, é cobrado imediatamente.

## 3. Benefícios da Nuvem Azure

---

1. **Alta disponibilidade →**  SLA (Service Legal Agreement), vai ter uma disponibilidade X, caso não cumpra, a empresa se responsabiliza. Azure SLA → 99% → 99.9% que pode estar disponível os serviços como exemplo do Azure, é um acordo estar disponível esse tempo. os 99% pode estar indisponível 1.68 hrs por semana e 7.2 hrs por mês, mas está dentro do acordo.
    
    O cliente pode receber créditos caso ultrapasse esse tempo indisponível.
    
2. **Escalabilidade →**  Paga apenas o necessário, se a demanda cair, reduz custos, se demanda subir, eleva custos, essa escalabilidade é ADAPTAÇAO ESPECÍFICA Á UMA DETERMINADA NECESSIDADE, AJUSTES.

3. **Elasticidade →** Se tiver 75% de requisição por X tempo → Adicione mais um servidor → Se a média dos 2 tiver 75% tambem → Adicione outro
Se reduzir para 25% de consumo → Remova um servidor
Ou seja, é a elasticidade, só paga o que usa.

4. **Confiabilidade →** A nuvem permite que você tenha recursos implantados em várias regiões do mundo.
Azure Well-Architected Framework
Azure tem poder de manutenção, ambiente confiável, se algo der errado, o sistema fica minimamente fora do ar.

5. **Previsibilidade →** Permite que você avance com confiança, seja no desempenho ou no custo, influenciadddas pelo Azure Well-Architected Framework também.

6. **Segurança →** A nuvem oferece ferramentas de segurança que atende às necessidades dos clientes, mas é importante lembrar que a IMPLEMENTAÇÃO DE MUITAS DELAS DEVEM SER REALIZADAS PELO CLIENTE.

7. **Gerenciamento →** Capacidade de setar escalabilidade e outras características como segurança e fatores de previsibilidade.


## 4. Tipos de Serviço de Nuvem

---

→ **IaaS (Infraestrutura como Serviço)**

Eu (cliente) me envolvo mais com o sistema, exemplo quando eu crio uma maquina virtual, temos que organizar muita configurações, depois de ligada, temos que ir monitorando a máquina virtual. Esse modelo de infraestrutura como serviço podemos ter mais liberdade para trabalhar.

Criamos uma infraestrutura de Ti de pagamento conforme o uso alugando:

- Virtual Machines
- Armazenamento
- Redes
- Sistemas operacionais

De um provedor de nuvem.

É a categoria mais flexível. Você aluga a infraestrutura de TI (servidores e máquinas virtuais, armazenamento, redes) de um provedor de nuvem em um modelo pré-pago.

- **O que o Azure gerencia:** Apenas o hardware físico (datacenters, eletricidade, refrigeração) e a virtualização.
- **O que VOCÊ gerencia:** Tudo o que está dentro da máquina. O sistema operacional (Windows/Linux), as atualizações (patches), o middleware, o runtime, os dados e a aplicação.
- **Quando usar:**
    - Migrações "Lift and shift" (tirar do on-premise e jogar na nuvem sem alterar o código).
    - Quando você precisa de controle total sobre o sistema operacional.
    - Para ambientes de teste e desenvolvimento rápidos.
- **Exemplos no Azure:**
    - **Azure Virtual Machines (VMs)**
    - **Azure Virtual Networks (VNETs)**
    - **Azure Disk Storage**

> Analogia: É como alugar um lote vazio. O proprietário garante que o terreno existe e tem acesso à rua, mas você precisa construir a casa, instalar a encanação, pintar as paredes e decorar.
> 

**→ PaaS (Plataform as a service)**

Fornece um ambiente para a criação, teste e implantação de aplicativos de software, sem focar no gerenciamento da infraestrutura.

Projetado para desenvolvedores. O Azure fornece um ambiente para criar, testar e implantar aplicativos de software sem que você precise se preocupar com a configuração ou gerenciamento da infraestrutura subjacente (servidores, armazenamento, rede, banco de dados).

- **O que o Azure gerencia:** Hardware, virtualização, **Sistema Operacional**, middleware e runtime. O Azure cuida dos patches de segurança do Windows/Linux automaticamente.
- **O que VOCÊ gerencia:** Apenas os **aplicativos** (código) e os **dados**.
- **Quando usar:**
    - Desenvolvimento de novas aplicações web ou mobile.
    - Quando você não quer perder tempo configurando servidores ou atualizando o Windows.
    - Para usar recursos como Serverless ou Bancos de Dados gerenciados.
- **Exemplos no Azure:**
    - **Azure App Service** (para hospedar sites).
    - **Azure SQL Database** (banco de dados gerenciado).
    - **Azure Functions** (computação serverless).

> Analogia: É como alugar um quarto de hotel. A estrutura, a limpeza, a manutenção elétrica e a mobília são problemas do hotel. Você só precisa levar suas malas (código) e viver lá.
> 

→ **SaaS (Software as a Service)**

Os usuários se conectam e usam aplicativos com base em nuvem pela internet, exemplo Office 365.

É o software fornecido pela internet. É uma solução completa e pronta para uso. A maioria das aplicações SaaS que usamos no dia a dia roda na nuvem.

- **O que o Azure/Microsoft gerencia:** **Tudo**. Do hardware até o código da aplicação.
- **O que VOCÊ gerencia:** Apenas a configuração, o acesso dos usuários e os dados que você coloca lá.
- **Quando usar:**
    - Para funções de negócios padrão (e-mail, colaboração, CRM).
    - Quando você quer uma solução pronta "out-of-the-box".
- **Exemplos no ecossistema Microsoft:**
    - **Microsoft 365** (Office, Outlook, Teams).
    - **Dynamics 365**.
    - **OneDrive**.

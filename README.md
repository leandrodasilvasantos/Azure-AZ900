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

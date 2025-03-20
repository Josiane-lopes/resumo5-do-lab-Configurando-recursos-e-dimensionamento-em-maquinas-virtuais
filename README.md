# resumo5-do-lab-Configurando-recursos-e-dimensionamento-em-maquinas-virtuais
"Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO - Serviços de computação e rede do Azure.".

Serviços de computação e rede do Azure. 

Três opções de computação (máquinas virtuais, contêineres e funções do Azure). 
Recursos de rede (redes virtuais do Azure, DNS do Azure e Azure ExpressRoute).

⦁	O que veremos:
⦁	Tipos de computação, incluindo instâncias de contêiner, máquinas virtuais e funções.
⦁	Opções de máquina virtual, incluindo VMs (máquinas virtuais), conjuntos de dimensionamento de máquinas virtuais, conjuntos de disponibilidade de máquinas virtuais e Área de Trabalho Virtual do Azure.
⦁	Recursos necessários para máquinas virtuais.
⦁	Opções de hospedagem de aplicativos, incluindo Aplicativos Web, contêineres e máquinas virtuais do Azure.
⦁	Rede virtual, incluindo a finalidade das Redes Virtuais do Azure, sub-redes virtuais do Azure, emparelhamento, DNS do Azure, Gateway de VPN e ExpressRoute.
⦁	Pontos de extremidade públicos e privados.

Descrever máquinas virtuais do Azure
Com as VMs (Máquinas Virtuais) do Azure, você pode criar e usar VMs na nuvem. As VMs fornecem IaaS (infraestrutura como serviço) na forma de um servidor virtualizado e podem ser usadas de várias maneiras. Como em um computador físico, você pode personalizar todos os programas de software em execução na VM. As VMs são uma opção ideal quando você precisa de:
⦁	Controle total sobre o SO (sistema operacional).
⦁	Capacidade para executar um software personalizado.
⦁	Usar configurações personalizadas de hospedagem.
Uma VM do Azure oferece a flexibilidade da virtualização sem a necessidade de comprar e manter o hardware físico que a executa. No entanto, como uma oferta de IaaS, você ainda precisa configurar, atualizar e manter o software executado na VM.
Você pode até mesmo criar ou usar uma imagem já criada para provisionar rapidamente VMs. Você pode criar e provisionar uma VM em minutos quando seleciona uma imagem de VM pré-configurada. Uma imagem é um modelo usado para criar uma VM e pode já incluir um sistema operacional e outros softwares, como ferramentas de desenvolvimento ou ambientes de hospedagem na Web.
Dimensionar VMs no Azure
Você pode executar VMs únicas para teste, desenvolvimento ou para tarefas secundárias. Ou pode agrupar VMs para fornecer alta disponibilidade, escalabilidade e redundância. O Azure também pode gerenciar o agrupamento de VMs para você com recursos como conjuntos de dimensionamento e conjuntos de disponibilidade.
conjuntos de escala de máquina virtual
Os Conjuntos de Dimensionamento de Máquinas Virtuais 
Os Conjuntos de Dimensionamento de Máquinas Virtuais permitem criar e gerenciar um grupo de VMs idênticas e com balanceamento de carga. Se você simplesmente criou várias VMs com a mesma finalidade, precisará garantir que todas elas foram configuradas de modo idêntico e configurar parâmetros de roteamento de rede para garantir a eficiência. Você também precisa monitorar a utilização para determinar se precisa aumentar ou diminuir o número de VMs.
Em vez disso, com conjuntos de dimensionamento de máquinas virtuais, o Azure automatiza a maior parte desse trabalho. Os conjuntos de dimensionamento permitem que você gerencie, configure e atualize centralmente um grande número de VMs em minutos. O número de instâncias de VM pode aumentar ou diminuir automaticamente em resposta à demanda ou você pode defini-lo para uma escala com base em uma agenda definida. Os conjuntos de dimensionamento de máquinas virtuais também implantam automaticamente um balanceador de carga para garantir que seus recursos estejam sendo usados com eficiência. Com conjuntos de dimensionamento de máquinas virtuais, você pode criar serviços em grande escala para áreas como computação, big data e cargas de trabalho de contêiner.

Conjuntos de disponibilidade da máquina virtual
Os conjuntos de disponibilidade de máquinas virtuais são outra ferramenta para ajudá-lo a criar um ambiente mais resiliente e altamente disponível. Os conjuntos de disponibilidade foram projetados para garantir que as VMs escalonem atualizações e tenham conectividade de rede e energia variadas, impedindo que você perca todas as suas VMs com uma só falha de rede ou energia.
A disponibilidade atinge esses objetivos agrupando VMs de duas maneiras: atualizar domínio e domínio de falha.
Domínio de atualização: as VMs de grupos de domínio de atualização que podem ser reinicializadas ao mesmo tempo. Essa configuração permite aplicar atualizações sabendo que apenas um agrupamento de domínio de atualização está offline por vez. Todos os computadores em uma atualização de domínio de atualização. Um grupo de atualizações que passa pelo processo de atualização recebe um tempo de 30 minutos para se recuperar antes que a manutenção no próximo domínio de atualização seja iniciada.
Domínio de falha: o domínio de falha agrupa suas VMs por origem de energia comum e comutador de rede. Por padrão, um conjunto de disponibilidade divide suas VMs em até três domínios de falha. Isso ajuda a proteger contra uma falha de energia física ou de rede, tendo VMs em diferentes domínios de falha (portanto, sendo conectadas a diferentes recursos de energia e rede).
O melhor de tudo é que não há nenhum custo adicional para configurar um conjunto de disponibilidade. Você paga apenas pelas instâncias de VM criadas.
Exemplos de quando usar VMs
Alguns exemplos comuns ou casos de uso para máquinas virtuais incluem:
Durante o teste e o desenvolvimento. As VMs fornecem uma maneira rápida e fácil de criar diferentes configurações de sistema operacional e de aplicativo. A equipe de teste e desenvolvimento pode excluir facilmente as VMs quando não precisarem mais delas.
Ao executar aplicativos na nuvem. A capacidade de executar determinados aplicativos na nuvem pública, em vez de criar uma infraestrutura tradicional para executá-los, pode trazer benefícios econômicos substanciais. Por exemplo, um aplicativo pode precisar lidar com flutuações na demanda. Desligar VMs quando elas não são necessárias ou iniciá-las rapidamente para atender a um aumento repentino na demanda significa que você paga apenas pelos recursos que usa.
Ao estender seu datacenter para a nuvem: uma organização pode estender os recursos de sua própria rede local criando uma rede virtual no Azure e adicionando VMs a ela. Aplicativos como o SharePoint podem, então, ser executados em uma VM do Azure em vez de localmente. É mais fácil ou menos caro implantar dessa forma do que em um ambiente local.
Durante a recuperação de desastre: assim como acontece com a execução de determinados tipos de aplicativos na nuvem e com a extensão de uma rede local para a nuvem, você pode conseguir economias significativas usando uma abordagem baseada em IaaS para a recuperação de desastre. Se um datacenter primário falhar, você poderá criar VMs em execução no Azure para executar seus aplicativos críticos e desligá-los quando o datacenter primário ficar operacional novamente.
Migrar para a nuvem com VMs
As VMs também são uma excelente opção quando você migra de um servidor físico para a nuvem (também conhecido como lift-and-shift). Você pode criar uma imagem do servidor físico e hospedá-la em uma VM com poucas ou nenhuma alteração. Assim como um servidor local físico, você deve manter a VM: você é responsável por manter o sistema operacional e o software instalados.
Recursos da VM
Ao provisionar uma VM, você também terá a oportunidade de escolher os recursos associados a essa VM, incluindo:
⦁	Tamanho (finalidade, número de núcleos de processador e quantidade de RAM)
⦁	Discos de armazenamento (unidades de disco rígido, unidades de estado sólido etc.)
⦁	Rede (rede virtual, endereço IP público e configuração de porta)
Descrever a área de trabalho virtual do Azure
Outro tipo de máquina virtual é a Área de Trabalho Virtual do Azure. A Área de Trabalho Virtual do Azure é um serviço de virtualização de área de trabalho e aplicativos que é executado na nuvem. Ele permite que você use uma versão do Windows hospedada na nuvem em qualquer localização. A Área de Trabalho Virtual do Azure opera em dispositivos e sistemas operacionais e funciona com aplicativos que você pode usar para acessar áreas de trabalho remotas ou a maioria dos navegadores modernos.
Aprimorar a segurança
A Área de Trabalho Virtual do Azure fornece gerenciamento de segurança centralizado para áreas de trabalho dos usuários com o Microsoft Entra ID. Você pode habilitar a autenticação multifator para proteger as entradas do usuário. Você também pode proteger o acesso aos dados atribuindo RBACs (controles de acesso baseados em função) granulares aos usuários.
Com a Área de Trabalho Virtual do Azure, os dados e aplicativos ficam separados do hardware local. A área de trabalho e os aplicativos reais estão em execução na nuvem, o que significa que o risco de dados confidenciais serem deixados em um dispositivo pessoal é reduzido. Além disso, as sessões de usuário são isoladas em ambientes de sessão única e de várias sessões.
Implantação de Windows 10 ou do Windows 11 de várias sessões
A Área de Trabalho Virtual do Azure permite que você use a multissessão do Windows 10 ou Windows 11 Enterprise, o único sistema operacional baseado em cliente Windows que habilita vários usuários simultâneos em uma VM. A Área de Trabalho Virtual do Azure também fornece uma experiência mais consistente com suporte a aplicativos mais amplo em comparação com sistemas operacionais baseados no Windows Server.
Descrever contêineres do Azure
Embora as máquinas virtuais sejam uma excelente maneira de reduzir os custos em comparação com os investimentos necessários para o hardware físico, elas ainda estão limitadas a um sistema operacional por máquina virtual. Se você quer executar várias instâncias de um aplicativo em um só computador host, os contêineres são uma ótima opção.
O que são contêineres?
Contêineres são um ambiente de virtualização. Assim como a execução de várias máquinas virtuais em um só host físico, você pode executar vários contêineres em apenas um host físico ou virtual. Diferentemente das máquinas virtuais, você não gerencia o sistema operacional para um contêiner. Máquinas virtuais parecem ser uma instância de um sistema operacional que você pode gerenciar e ao qual pode se conectar. Os contêineres são leves e projetados para serem criados, dimensionados e interrompidos dinamicamente. É possível criar e implantar máquinas virtuais à medida que a demanda do aplicativo aumenta, mas os contêineres são um método mais leve e ágil. Os contêineres foram projetados para permitir que você responda às alterações sob demanda. Com contêineres, você pode reiniciar rapidamente se houver uma falha ou de uma interrupção de hardware. Um dos mecanismos de contêiner mais populares é o Docker, e o Azure é compatível com o Docker.

Comparar máquinas virtuais e contêineres
Instâncias de Contêiner do Azure
As Instâncias de Contêiner do Azure oferecem a maneira mais rápida e simples de executar um contêiner no Azure, sem a necessidade de gerenciar máquinas virtuais nem adotar serviços adicionais. Instâncias de Contêiner do Azure são uma oferta de PaaS (plataforma como serviço). As Instâncias de Contêiner do Azure permitem que você carregue seus contêineres e, a seguir, o serviço executa os contêineres para você.

Aplicativos de Contêiner do Azure
Os Aplicativos de Contêiner do Azure são semelhantes, em muitos aspectos, a uma instância de contêiner. Eles permitem que você comece a trabalhar imediatamente, removem a parte de gerenciamento de contêineres e são uma oferta de PaaS. Os Aplicativos de Contêiner têm benefícios extras, como a capacidade de incorporar balanceamento de carga e colocação em escala. Essas outras funções permitem que você seja mais flexível em seu design.

Serviço de Kubernetes do Azure
O Serviço de Kubernetes do Azure (AKS) é um serviço de orquestração de contêiner. Um serviço de orquestração gerencia o ciclo de vida dos contêineres. Quando você está implantando uma frota de contêineres, o AKS pode tornar o gerenciamento de frota mais simples e eficiente.

Usar contêineres em suas soluções
Contêineres geralmente são usados para criar soluções que utilizam uma arquitetura de microsserviço. Essa arquitetura é onde você divide as soluções em partes menores e independentes. Por exemplo, você pode dividir um site em um contêiner que hospeda o front-end, outro que hospeda o back-end e um terceiro para o armazenamento. Essa divisão permite separar as partes do aplicativo em seções lógicas que podem ser mantidas, dimensionadas ou atualizadas de forma independente.
Imagine que o back-end do seu site atinja a capacidade máxima, mas o front-end e o armazenamento não estejam sob pressão. Com os contêineres, você pode ampliar o back-end separadamente para aprimorar o desempenho. Se algo exigisse tal alteração, você também poderia optar por alterar o serviço de armazenamento ou modificar o front-end sem afetar nenhum dos outros componentes.
Descrever funções do Azure
O Azure Functions é uma opção de computação sem servidor controlada por eventos que não requer a manutenção de máquinas virtuais ou contêineres. Se você criar um aplicativo usando VMs ou contêineres, esses recursos precisarão estar "em execução" para que seu aplicativo funcione. Com o Azure Functions, um evento desperta a função, reduzindo a necessidade de manter os recursos provisionados quando não há eventos.
Computação sem servidor no Azure
Benefícios do Azure Functions
Usar o Azure Functions é ideal quando você está preocupado apenas com o código que executa o serviço, e não com a plataforma ou a infraestrutura subjacente. As funções costumam ser usadas quando você precisa executar um trabalho em resposta a um evento (geralmente por meio de uma solicitação REST), um temporizador ou uma mensagem de outro serviço do Azure e quando esse trabalho pode ser concluído dentro de segundos.
As funções são dimensionadas automaticamente com base na demanda, portanto, podem ser uma boa opção quando a demanda é variável.
O Azure Functions executa seu código quando ele é acionado e desaloca automaticamente os recursos quando a função é concluída. Nesse modelo, o Azure cobra apenas pelo tempo de CPU usado durante a execução da função.
As funções podem ser sem estado ou com estado. Quando eles são sem estado (o padrão), eles se comportam como se fossem reiniciados sempre que respondem a um evento. Quando são com estado (chamadas de Durable Functions), um contexto é passado pela função para acompanhar a atividade anterior.
As funções são um componente chave da computação sem servidor. Elas também são uma plataforma de computação geral para executar qualquer tipo de código. Se as necessidades do aplicativo do desenvolvedor forem alteradas, você poderá implantar o projeto em um ambiente que não seja sem servidor. Essa flexibilidade permite gerenciar o dimensionamento, executar em redes virtuais e até mesmo isolar completamente as funções.
Descrever as opções de hospedagem de aplicativo
Se você precisar hospedar seu aplicativo no Azure, poderá inicialmente recorrer a uma VM (máquina virtual) ou contêineres. Tanto VMs quanto contêineres fornecem excelentes soluções de hospedagem. As VMs oferecem o controle máximo do ambiente de hospedagem e permitem que você o configure exatamente como deseja. As VMs também poderão ser o método de hospedagem mais familiar se você for novo na nuvem. Os contêineres, com a capacidade de isolar e gerenciar individualmente diferentes aspectos da solução de hospedagem, também podem ser uma opção robusta e atraente.
Há outras opções de hospedagem que você pode usar com o Azure, incluindo Serviço de Aplicativo do Azure.
Serviço de aplicativo do Azure
O Serviço de Aplicativo permite que você crie e hospede aplicativos Web, trabalhos em segundo plano, back-ends de dispositivos móveis e APIs RESTful na linguagem de programação de sua escolha sem gerenciar a infraestrutura. Ele oferece dimensionamento automático e alta disponibilidade. O Serviço de Aplicativo é compatível com o Windows e o Linux. Ele permite implantações automatizadas do GitHub, Azure DevOps ou qualquer repositório Git para dar suporte a um modelo de implantação contínua.
O Serviço de Aplicativo do Azure é uma opção de hospedagem robusta que você pode usar para hospedar seus aplicativos no Azure. O Serviço de Aplicativo do Azure permite que você se concentre em criar e manter seu aplicativo, e o Azure se concentra em manter o ambiente em funcionamento.
O Serviço de Aplicativo do Azure é um serviço com base em HTTP para hospedagem de aplicativos Web, APIs REST e back-ends móveis. Ele dá suporte a várias linguagens, incluindo .NET, .NET Core, Java, Ruby, Node.js, PHP ou Python. Ele também dá suporte a ambientes Windows e Linux.

Tipos de serviços de aplicativos
Com o Serviço de Aplicativo, você pode hospedar os estilos mais comuns de serviço de aplicativos, como:
⦁	Aplicativos Web
⦁	Aplicativos de API
⦁	WebJobs
⦁	Aplicativos móveis
O Serviço de Aplicativo cuida da maioria das decisões de infraestrutura com as quais você lida ao hospedar aplicativos acessíveis pela Web:
⦁	A implantação e o gerenciamento são integrados à plataforma.
⦁	Pontos de extremidade podem ser protegidos.
⦁	Sites podem ser dimensionados rapidamente para lidar com cargas de alto tráfego.
⦁	O balanceamento de carga interno e o gerenciador de tráfego fornecem alta disponibilidade.
Todos esses estilos de aplicativos são hospedados na mesma infraestrutura e compartilham esses benefícios. Essa flexibilidade torna o Serviço de Aplicativo a escolha ideal para hospedar aplicativos voltados para a Web.
Aplicativos Web
O Serviço de Aplicativo inclui suporte completo para a hospedagem de aplicativos Web usando ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP ou Python. Você pode escolher Windows ou Linux como sistema operacional do host.
Aplicativos de API
Da mesma forma como se hospeda um site, você pode criar APIs Web baseadas em REST usando a linguagem e a estrutura que você quiser. Receba o suporte completo do Swagger e a capacidade de empacotar e publicar sua API no Azure Marketplace. Os aplicativos produzidos podem ser consumidos por qualquer cliente baseado em HTTP ou em HTTPS.
WebJobs
Você pode usar o recurso do WebJobs para executar um script (.cmd, .bat, PowerShell ou Bash) ou um programa (.exe, Java, PHP, Python ou Node.js) no mesmo contexto de um aplicativo Web, aplicativo de API ou aplicativo móvel. Eles também podem ser agendados ou executados por um gatilho. O WebJobs geralmente é usado para executar tarefas em segundo plano como parte da lógica do aplicativo.
Aplicativos móveis
Use o recurso Aplicativos Móveis do Serviço de Aplicativo para criar rapidamente um back-end para aplicativos iOS e Android. Com apenas algumas ações no portal do Azure, você pode:
⦁	Armazenar dados de aplicativo móvel em um Banco de Dados SQL baseado em nuvem.
⦁	Autentique clientes em provedores sociais comuns, como MSA, Google, X e Facebook.
⦁	Enviar notificações por push.
⦁	Executar a lógica personalizada de back-end no C# ou Node.js.
No lado do aplicativo móvel, há suporte do SDK para aplicativos nativos para iOS, Android, Xamarin e React.
Descrever a rede virtual do Azure
As redes virtuais e as sub-redes virtuais do Azure permitem que recursos do Azure, como VMs, aplicativos Web e bancos de dados, comuniquem-se uns com os outros, com usuários na Internet e com computadores cliente locais. Você pode pensar em uma rede do Azure como uma extensão de sua rede local com recursos que vinculam outros recursos do Azure.

As redes virtuais do Azure oferecem as seguintes funcionalidades de rede essenciais:
⦁	Isolamento e segmentação
⦁	Comunicação pela Internet
⦁	Comunicação entre recursos do Azure
⦁	Comunicação com os recursos locais
⦁	Rotear tráfego de rede
⦁	Filtrar tráfego de rede
⦁	Conectar redes virtuais
A rede virtual do Azure dá suporte a pontos de extremidade públicos e privados para habilitar a comunicação entre recursos externos ou internos com outros recursos internos.
Pontos de extremidade públicos têm um endereço IP público e podem ser acessados de qualquer lugar do mundo.
Pontos de extremidade privados existem em uma rede virtual e têm um endereço IP privado dentro do espaço de endereço dessa rede virtual.
Isolamento e segmentação
A rede virtual do Azure permite criar várias redes virtuais isoladas. Quando você configura uma rede virtual, define um espaço de endereço IP privado usando intervalos de endereços IP públicos ou privados. O intervalo de IP existe somente na rede virtual e não é roteável pela Internet. Você pode dividir esse espaço de endereços IP em sub-redes e alocar parte do espaço de endereço definido para cada sub-rede nomeada.
Para resolução de nomes, você pode usar o serviço de resolução de nomes integrado ao Azure. Você também pode configurar a rede virtual para usar um servidor DNS interno ou externo.
Comunicações com a Internet
É possível habilitar conexões de entrada da Internet atribuindo um endereço IP público a um recurso do Azure ou colocar o recurso atrás de um balancear carga público.
Comunicação entre recursos do Azure
Convém habilitar recursos do Azure para que se comuniquem entre si com segurança. Você pode fazer isso de duas maneiras:
As redes virtuais podem conectar não apenas VMs, mas outros recursos do Azure, como Ambiente do Serviço de Aplicativo para Power Apps, Serviço de Kubernetes do Azure e os conjuntos de dimensionamento de máquinas virtuais do Azure.
Os pontos de extremidade de serviço podem se conectar a outros tipos de recursos do Azure, como bancos de dados SQL do Azure e contas de armazenamento. Essa abordagem permite vincular vários recursos do Azure às redes virtuais para melhorar a segurança e fornecer o encaminhamento ideal entre recursos.
Comunicação com os recursos locais
As redes virtuais do Azure permitem vincular recursos em seu ambiente local e na assinatura do Azure. Na verdade, você pode criar uma rede que abranja os ambientes locais e de nuvem. Há três mecanismos para você obter essa conectividade:
⦁	As conexões de rede virtual privada ponto a site são de um computador fora da organização de volta para a rede corporativa. Nesse caso, o computador cliente inicia uma conexão VPN criptografada para se conectar à rede virtual do Azure.
⦁	Redes virtuais privadas site a site vinculam seu dispositivo VPN ou gateway de VPN local ao Gateway de VPN do Azure em uma rede virtual. Na verdade, os dispositivos no Azure podem aparecer como estando na rede local. A conexão é criptografada e funciona pela Internet.
⦁	O Azure ExpressRoute fornece uma conectividade privada dedicada para o Azure que não passa pela Internet. O ExpressRoute é útil para ambientes em que você precisa de maior largura de banda e níveis de segurança ainda mais altos.

Rotear tráfego de rede
Por padrão, o Azure faz o roteamento de tráfego entre sub-redes em redes virtuais conectadas, em redes locais e na Internet. Você também pode controlar o roteamento e substituir essas configurações da seguinte maneira:
As tabelas de rotas permitem definir regras sobre como o tráfego deve ser direcionado. Você pode criar tabelas de rotas personalizadas que controlam como os pacotes são encaminhados entre as sub-redes.
O BGP (Border Gateway Protocol) funciona com Gateways de VPN do Azure, Servidor de Rota do Azure ou Azure ExpressRoute para propagar as rotas BGP locais para redes virtuais do Azure.
Filtrar tráfego de rede
As redes virtuais do Azure permitem filtrar o tráfego entre sub-redes usando as seguintes abordagens:
Grupos de segurança de rede são recursos do Azure que podem conter várias regras de segurança de entrada e saída. Você pode definir essas regras para permitir ou bloquear tráfego com base em fatores como endereço IP de origem e de destino, porta e protocolo.
Soluções de virtualização de rede são VMs especializadas que podem ser comparadas a um dispositivo de rede protegida. Uma solução de virtualização de rede realiza uma função de rede específica, como execução de um firewall ou otimização de WAN (rede de longa distância).
Conectar redes virtuais
Você pode vincular redes virtuais usando o emparelhamento dessas redes. O emparelhamento permite que duas redes virtuais se conectem diretamente entre si. O tráfego de rede entre redes emparelhadas é privado e viaja na rede de backbone da Microsoft, nunca entrando na Internet pública. O emparelhamento permite que os recursos em cada rede virtual se comuniquem entre si. Essas redes virtuais podem estar em regiões separadas. Esse recurso permite que você crie uma rede interconectada global por meio do Azure.
As UDR (rotas definidas pelo usuário) permitem controlar as tabelas de roteamento entre sub-redes em uma rede virtual ou entre redes virtuais. Isso permite maior controle sobre o fluxo de tráfego de rede.
Descrever redes virtuais privadas do Azure (VPN)
Uma VPN (rede virtual privada) usa um túnel criptografado dentro de outra rede. As VPNs costumam ser implantadas para conectar duas ou mais redes privadas confiáveis entre si em uma rede não confiável (normalmente a Internet pública). O tráfego é criptografado ao viajar pela rede não confiável para evitar interceptação ou outros ataques. As VPNs podem permitir que as redes compartilhem informações confidenciais de modo seguro e protegido.
Gateways VPN
Um gateway de VPN é um tipo de gateway de rede virtual. As instâncias do Gateway de VPN do Azure são implantadas em uma subrede dedicada da rede virtual e permitem a seguinte conectividade:
⦁	Conecte datacenters locais a redes virtuais por meio de uma conexão site a site.
⦁	Conecte dispositivos individuais a redes virtuais por meio de uma conexão ponto a site.
⦁	Conecte redes virtuais a outras redes virtuais por meio de uma conexão rede a rede.
Todas as transferências de dados são criptografadas em um túnel privado à medida que atravessam a Internet. Você pode implantar apenas um gateway de VPN em cada rede virtual. Porém, você pode usar um gateway para se conectar a vários locais, incluindo outras redes virtuais ou datacenters locais.
Ao configurar um gateway de VPN, você deve especificar o tipo de VPN: baseada em política ou baseada em rota. A principal distinção entre esses dois tipos é como eles determinam qual tráfego precisa de criptografia. No Azure, independentemente do tipo de VPN, o método de autenticação empregado é uma chave pré-compartilhada.
⦁	Gateways de VPN baseados em política especificam estaticamente o endereço IP dos pacotes que devem ser criptografados por meio de cada túnel. Esse tipo de dispositivo avalia cada pacote de dados em relação a esses conjuntos de endereços IP para escolher o túnel para o qual o pacote será enviado.
⦁	Em gateways baseados em rota, os túneis IPSec são modelados como um adaptador de rede ou uma interface de túnel virtual. O roteamento de IP (protocolos de roteamento dinâmico ou rotas estáticas) decide qual dessas interfaces de túnel usar ao enviar cada pacote. VPNs baseadas em rota são o método preferido para conectar dispositivos locais. Elas são mais resilientes a alterações de topologia, como a criação de novas sub-redes.
Use um gateway de VPN baseado em rota se precisar de qualquer um dos seguintes tipos de conectividade:
⦁	Conexões entre redes virtuais
⦁	Conexões ponto a site
⦁	Conexões multissite
⦁	Coexistência com um gateway do Azure ExpressRoute
⦁	Cenários de alta disponibilidade
Se você está configurando uma VPN para manter suas informações seguras, é importante ter certeza de que ela é uma configuração VPN altamente disponível e tolerante a falhas. Há alguns modos de maximizar a resiliência do gateway de VPN.
Ativo/em espera
Por padrão, gateways de VPN são implantados como duas instâncias em uma configuração ativa/em espera, mesmo se você vê apenas um recurso de gateway de VPN no Azure. Quando a manutenção planejada ou a interrupção não planejada afeta a instância ativa, a instância de modo de espera assume automaticamente a responsabilidade pelas conexões sem nenhuma intervenção do usuário. Durante esse failover, as conexões são interrompidas, mas normalmente são restauradas em alguns segundos para manutenção planejada e dentro de 90 segundos em caso de interrupções não planejadas.
Ativo/ativo
Com a introdução da compatibilidade com o protocolo de roteamento BGP, você também pode implantar os gateways de VPN em uma configuração ativo/ativo. Nessa configuração, você atribui um endereço IP público exclusivo a cada instância. Em seguida, cria túneis do dispositivo local para cada endereço IP. É possível estender a alta disponibilidade implantando um dispositivo VPN local adicional.
Failover do ExpressRoute
Outra opção de alta disponibilidade é configurar um gateway de VPN como um caminho de failover seguro para conexões ExpressRoute. Os circuitos ExpressRoute têm resiliência integrada. Porém, não são imunes a problemas físicos que afetam os cabos que fornecem conectividade nem a interrupções que afetam toda a localização do ExpressRoute. Em cenários de alta disponibilidade, nos quais há risco associado a uma interrupção de um circuito do ExpressRoute, você também pode provisionar um gateway de VPN que usa a Internet como um método alternativo de conectividade. Dessa forma, você pode garantir que sempre haja uma conexão com as redes virtuais.
Gateways com redundância de zona
Nas regiões que dão suporte a zonas de disponibilidade, os gateways de VPN e os gateways de ExpressRoute podem ser implantados em uma configuração com redundância de zona. Essa configuração oferece resiliência, escalabilidade e maior disponibilidade para os gateways de rede virtual. A implantação de gateways em zonas de disponibilidade do Azure separa de forma física e lógica os gateways em uma região, enquanto protege a conectividade de rede local com o Azure contra falhas no nível da zona. Esses gateways exigem SKUs (unidades de manutenção de estoque) de gateway diferentes e usam os endereços IP públicos Standard em vez dos Básicos.
Descrever o Azure ExpressRoute
O Azure ExpressRoute permite que você estenda suas redes locais para a nuvem da Microsoft em uma conexão privada com a ajuda de um provedor de conectividade. Essa conexão é chamada de Circuito do ExpressRoute. Com o ExpressRoute, você pode estabelecer conexões com os serviços em nuvem da Microsoft, como o Microsoft Azure e o Microsoft 365. Esse recurso permite que você conecte escritórios, datacenters ou outras instalações à nuvem da Microsoft. Cada local teria o próprio circuito do ExpressRoute.
A conectividade pode ocorrer de uma rede any-to-any (VPN de IP), uma rede Ethernet ponto a ponto ou uma conexão cruzada virtual por meio de um provedor de conectividade em uma colocação. As conexões do ExpressRoute não passam pela Internet pública. Essa configuração permite que as conexões do ExpressRoute ofereçam mais confiabilidade, velocidades mais rápidas, latências consistentes e maior segurança do que as conexões típicas pela Internet.
Recursos e benefícios do ExpressRoute
Há vários benefícios de usar o ExpressRoute como o serviço de conexão entre o Azure e as redes locais.
⦁	Conectividade com os serviços de nuvem da Microsoft em todas as regiões da região geopolítica.
⦁	Conectividade global com os serviços da Microsoft em todas as regiões com o Alcance Global do ExpressRoute.
⦁	Roteamento dinâmico entre sua rede e a Microsoft por meio do BGP (Border Gateway Protocol).
⦁	Redundância interna em cada local de emparelhamento para proporcionar maior confiabilidade.
⦁	Conectividade com serviços em nuvem da Microsoft
O ExpressRoute permite acesso direto aos seguintes serviços em todas as regiões:
⦁	Microsoft Office 365
⦁	Microsoft Dynamics 365
⦁	Serviços de computação do Azure, como as Máquinas Virtuais do Azure
⦁	Serviços de Nuvem do Azure, como o Azure Cosmos DB e o Armazenamento do Azure
⦁	Conectividade global
Você pode habilitar o Alcance Global do ExpressRoute para trocar dados entre sites locais conectando seus circuitos do ExpressRoute. Por exemplo, digamos que você tenha um escritório na Ásia e um datacenter na Europa, ambos com circuitos do ExpressRoute os conectando à rede da Microsoft. Você pode usar o Alcance Global do ExpressRoute para conectar essas duas instalações, permitindo que elas se comuniquem sem transferir dados pela Internet pública.
Roteamento dinâmico
O ExpressRoute usa o BGP. O BGP é usado para trocar rotas entre as redes locais e os recursos em execução no Azure. Esse protocolo permite o roteamento dinâmico entre a rede local e os serviços em execução na nuvem da Microsoft.
Redundância interna
Cada provedor de conectividade usa dispositivos redundantes para verificar se as conexões estabelecidas com a Microsoft estão altamente disponíveis. É possível configurar vários circuitos para complementar esse recurso.
Modelos de conectividade do ExpressRoute
O ExpressRoute dá suporte a quatro modelos que podem ser usados para conectar a rede local à Microsoft Cloud:
⦁	Colocação do CloudExchange
⦁	Conexão Ethernet ponto a ponto
⦁	Conexão qualquer para qualquer
⦁	Direto de sites do ExpressRoute
Colocalização em um compartilhamento de nuvem
A colocação refere-se ao datacenter, ao escritório ou a outra instalação que está sendo fisicamente colocada em uma troca de nuvem, como um ISP. Se sua instalação estiver colocada em uma troca de nuvem, você poderá solicitar uma conexão cruzada virtual à nuvem da Microsoft.
Conexão Ethernet ponto a ponto
A conexão de Ethernet ponto a ponto se refere ao uso de uma conexão ponto a ponto para conectar sua instalação à Microsoft Cloud.
Redes qualquer para qualquer
Com a conectividade any-to-any, você pode integrar sua WAN (rede de longa distância) ao Azure fornecendo conexões aos seus escritórios e datacenters. O Azure é integrado à sua conexão WAN para fornecer uma conexão, da mesma forma que você teria entre o datacenter e as filiais.
Direto de sites do ExpressRoute
Você pode se conectar diretamente à rede global da Microsoft em um local de emparelhamento distribuído estrategicamente em todo o mundo. O ExpressRoute Direct fornece oferece conectividade dupla de 100 Gbps ou 10 Gbps, compatível com conectividade Ativa/Ativa em escala.
Considerações de segurança
Com o ExpressRoute, seus dados não viajam pela Internet pública, reduzindo os riscos associados às comunicações com a Internet. O ExpressRoute é uma conexão particular de sua infraestrutura local com a infraestrutura do Azure. Mesmo que você tenha uma conexão do ExpressRoute, consultas DNS, verificações de listas de certificados revogados e solicitações da Rede de Distribuição de Conteúdo do Azure ainda serão enviadas pela Internet pública.
Descrever o DNS do Azure
O DNS do Azure é um serviço de hospedagem para domínios DNS que fornece a resolução de nomes usando a infraestrutura do Microsoft Azure. Ao hospedar seus domínios no Azure, você pode gerenciar seus registros DNS usando as mesmas credenciais, APIs, ferramentas e cobrança que seus outros serviços do Azure.
Benefícios do DNS do Azure
O DNS do Azure usa o escopo e a escala do Microsoft Azure para proporcionar inúmeros benefícios, incluindo:
⦁	Confiabilidade e desempenho
⦁	Segurança
⦁	Facilidade de uso
⦁	Personalizar redes virtuais
⦁	Registros de alias
⦁	Confiabilidade e desempenho
Domínios DNS no DNS do Azure são hospedados na rede global do Azure de servidores de nomes DNS, fornecendo resiliência e alta disponibilidade. O DNS do Azure usa a rede anycast, de modo que o servidor DNS disponível mais próximo responde a cada consulta DNS, fornecendo desempenho rápido e alta disponibilidade para seu domínio.
Segurança
O DNS do Azure baseia-se no Azure Resource Manager, que fornece recursos como:
⦁	Azure RBAC (controle de acesso baseado em função do Azure) para controlar quem tem acesso a ações específicas da sua organização.
⦁	Log de atividades para monitorar como um usuário em sua organização modificou um recurso ou para encontrar um erro ao solucionar problemas.
⦁	Bloqueio de recursos para bloquear uma assinatura, um grupo de recursos ou um recurso. O bloqueio impede que os usuários em sua organização acidentalmente excluam ou modifiquem recursos essenciais.
Fácil de uso
O DNS do Azure pode gerenciar os registros DNS para serviços do Azure e também fornece o DNS para recursos externos. O DNS do Azure é integrado ao portal do Azure e usa as mesmas credenciais, cobrança e contrato de suporte que outros serviços do Azure.
Como o DNS do Azure está em execução no Azure, você pode gerenciar seus domínios e registros com o portal do Azure, cmdlets do Azure PowerShell e a CLI do Azure multiplataforma. Aplicativos que requerem gerenciamento automatizado de DNS podem se integrar no serviço usando a API REST e os SDKs.
Redes virtuais personalizáveis com domínios privados
O DNS do Azure também dá suporte a domínios DNS privados. Esse recurso permite que você use seus nomes de domínio personalizados em suas redes virtuais privadas, em vez ficar atrelado aos nomes fornecidos pelo Azure.
Registros de alias
O DNS do Azure também dá suporte a conjuntos de registros de alias. É possível usar um conjunto de registros de alias para se referir a um recurso do Azure, como um endereço IP público do Azure, um perfil do Gerenciador de Tráfego do Azure ou um ponto de extremidade CDN (Rede de Distribuição de Conteúdo) do Azure. Se o endereço IP do recurso subjacente for alterado, o conjunto de registros de alias se atualizará perfeitamente durante a resolução de DNS. O alias registra os pontos de configuração na instância do serviço e a instância do serviço é associada a um endereço IP.
 Importante
Você não pode usar o DNS do Azure para comprar um nome de domínio. Por um valor anual, você pode comprar um nome de domínio usando domínios do Serviço de Aplicativo ou um registrador de nomes de domínio de terceiros. Depois de comprados, seus domínios podem ser hospedados no DNS do Azure para gerenciamento de registros.

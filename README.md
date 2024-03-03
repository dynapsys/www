# [www.dynapsys.com](https://www.dynapsys.com/)

[DYNAPSYS -text.to.services](https://text.to.services/)

![Animiertes Logo 500x500 px](https://github.com/dynapsys/www/assets/5669657/d6046bf3-7b0e-47fc-8aeb-6691581daac8)


Dynapsys provides a dynamic infrastructure through DNS configurations, utilizing CNAME RECORDS for FaaS provider redirection and TXT RECORDS for Git repository URLs, enabling source-code access, deployment definitions, and configurations for ready-to-use services on FaaS platforms.

DNS-configured services leverage the Domain Name System (DNS) to manage and map domain names to the internet resources, providing dynamic and scalable solutions for directing user requests to appropriate servers, load balancing, and even implementing failover mechanisms or geo-targeting strategies. These services utilize DNS records, such as A records for IP address mapping, CNAME records for domain aliasing, TXT records for metadata, and others, to configure how traffic to a domain should be handled, enabling more efficient and flexible deployment of web applications, content delivery networks (CDNs), and other online services.


- **A and AAAA Records**: Direct domain names to IP addresses of servers hosting the services.
- **CNAME Records**: Alias one domain name to another, allowing a single service to be accessed through multiple domain names or directing to cloud services and content delivery networks (CDNs).
- **TXT Records**: Store text information in DNS for various purposes, including verification of domain ownership, SPF records for email security, and could be creatively used to store metadata for services.
- **SRV Records**: Used in some services to define the location of servers or services, specifying a hostname and port number for specific services, making it useful for services that require multiple ports or protocols.
- **DNS Load Balancing**: Distributing traffic across multiple servers to ensure no single server becomes overwhelmed, improving service reliability and latency.


## About

**dynapsys** is a dynamic infrastructure of services based on DNS configuration with CNAME RECORD for redirection to FaaS provider and TXT RECORD as url of git repository with:
+ source-code
+ definition for deployment purpose
+ configuration of ready to use service on FaaS platform/marketplace
  

"Dynapsys" give a specific implementation strategy for a dynamic infrastructure based on DNS configurations and cloud-based services. 


### DNS Configuration with CNAME Record for Redirection to FaaS Provider

DNS (Domain Name System) is like the phonebook of the internet that translates human-friendly domain names to IP addresses that computers use. A CNAME (Canonical Name) record is a type of DNS entry that maps an alias name to a true or canonical domain name. In the context of Dynapsys:
   - *Why to use:* CNAME records are useful for directing traffic from multiple domain names to a single domain, making it easy to manage and switch traffic between different cloud services or FaaS (Function as a Service) providers without changing the service's domain name.
   - *How to use:* You configure a CNAME record in your DNS settings to redirect requests from your domain to your chosen FaaS provider’s domain. So, for example, requests to `service.yourdomain.com` could be redirected to `yourapp.faasprovider.com`.

### TXT Record as URL to GitHub Source-Code and Definition for Deployment Purpose

A TXT record is another type of DNS entry that holds text information. This can be used for various purposes, including verification, description, and linking to related resources.
   - *Why to use:* Using a TXT record to store a URL to the GitHub source code and the definition for deployment allows for a level of indirection and documentation directly within DNS. It makes it possible to retrieve the source and instructions necessary for deploying a service through standard DNS queries.
   - *How to use:* You create a TXT record with the value being the URL to the GitHub repository where the source code resides. This URL might contain additional paths or directives that automation tools or deployment scripts could use to understand how to deploy the service.


By using DNS in this way, Dynapsys could allow dynamic and flexible infrastructural management. 
When updates or changes to the services are necessary, you can manage these through DNS updates, which propagate rapidly across the internet. 
Additionally, this strategy could be part of an infrastructure-as-code (IaC) system, automating the provisioning and management of infrastructure by using configuration files.

It’s important to note that while storing URLs in TXT records is possible, there are limits to the size of TXT records, so the url is too limited.
Moreover, some DNS providers offer APIs that might be more suited to automation than relying on DNS records for service management.


## Why

**Systemy rozproszone** stanowią fascynujący obszar w dziedzinie informatyki. Oto kilka rozważań na temat małych, rozproszonych usług:

1. **Architektura Mikrousług**:
    - **Mikrousługi** to jedna z odmian systemów rozproszonych. Polega na podziale aplikacji na **oddzielne komponenty** lub "usługi".
    - Każda mikrousługa obsługuje **konkretną funkcję biznesową**, taką jak płatności, zarządzanie użytkownikami czy obsługa produktów.
    - Dzięki temu podejściu można łatwiej skalować poszczególne komponenty i unikać **centralnych punktów awarii**.
    - Mikrousługi są **transparentne** – węzły mogą uzyskiwać dostęp do innych węzłów w systemie i komunikować się z nimi.

2. **Przewagi Systemów Rozproszonych**:
    - **Współdzielenie zasobów**: System rozproszony może współdzielić sprzęt, oprogramowanie lub dane.
    - **Przetwarzanie równoczesne**: Wiele komputerów może przetwarzać tę samą funkcję jednocześnie.
    - **Skalowalność**: Wydajność obliczeniową i przetwarzanie można skalować w razie potrzeby po rozszerzeniu o dodatkowe komputery.
    - **Wykrywanie błędów**: Awarie można łatwiej wykrywać.
    - **Transparentność**: Węzły mogą komunikować się ze sobą.

3. **Systemy Scentralizowane vs. Rozproszone**:
    - **System scentralizowany** to taki, w którym wszystkie obliczenia są wykonywane przez **jeden komputer** znajdujący się w pojedynczej lokalizacji.
    - W systemie scentralizowanym stan systemu jest zawarty w **centralnym węźle**, do którego klienci mają dostęp indywidualnie.
    - W przeciwności do tego, system rozproszony nie ma **jednego punktu awarii** i składa się z wielu oddzielnych węzłów.

4. **Małe Rozproszone Usługi**:
    - W przypadku małych rozproszonych usług, warto rozważyć **architekturę mikrousług**.
    - Każda mikrousługa może obsługiwać **konkretną funkcję** i być **wbudowana** w cały system.
    - Przykłady małych usług to: autoryzacja użytkowników, zarządzanie sesjami, obsługa płatności, czy zarządzanie produktami.
    - Ważne jest, aby **dokładnie przemyśleć granice** między poszczególnymi usługami, aby uniknąć nadmiernego skomplikowania systemu.


Źródło:
+ [Czym jest system rozproszony? - Atlassian](https://www.atlassian.com/pl/microservices/microservices-architecture/distributed-architecture)
+ [Systemy rozproszone - liczne zastosowania w przedsiębiorstwach](https://mindboxgroup.com/pl/systemy-rozproszone-liczne-zastosowania-w-przedsiebiorstwach-o-ktorych-warto-wiedziec/)





---
+ [edit](https://github.com/dynapsys/www/edit/main/README.md)
+ [project](https://github.com/dynapsys)

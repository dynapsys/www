# [www.dynapsys.com](https://www.dynapsys.com/)


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


---
+ [edit](https://github.com/dynapsys/www/edit/main/README.md)
+ [project](https://github.com/dynapsys)

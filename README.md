# [www.dynapsys.com](https://www.dynapsys.com/)

**dynapsys** is a dynamic infrastructure of services based on DNS configuration with CNAME RECORD for redirection to FaaS provider and TXT RECORD as url to github source-code and definition for deployment purpose

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

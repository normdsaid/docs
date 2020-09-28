---
title: Ausgehenden Webproxyserver konfigurieren
intro: 'Ein Proxyserver bietet eine zusätzliche Sicherheitsebene für {{ site.data.variables.product.product_location_enterprise }}.'
redirect_from:
  - /enterprise/admin/guides/installation/configuring-a-proxy-server/
  - /enterprise/admin/installation/configuring-an-outbound-web-proxy-server
  - /enterprise/admin/configuration/configuring-an-outbound-web-proxy-server
versions:
  enterprise-server: '*'
---

Wenn ein Proxyserver für {{ site.data.variables.product.product_location_enterprise }} aktiviert wird, werden ausgehende Nachrichten, die von {{ site.data.variables.product.prodname_ghe_server }} gesendet wurden, zunächst über den Proxyserver gesendet, sofern der Zielhost nicht als HTTP-Proxyausschluss hinzugefügt wurde. Zu den Typen ausgehender Nachrichten zählen ausgehende Webhooks, das Hochladen von Bundles und das Abrufen von veralteten Avataren. Die URL des Proxyservers ist das Protokoll, die Domain oder IP-Adresse plus die Portnummer, also beispielsweise `http://127.0.0.1:8123`.

{% note %}

**Hinweis:** Um zwischen {{ site.data.variables.product.product_location_enterprise }} und {{ site.data.variables.product.prodname_dotcom_the_website }} eine Verbindung herzustellen, muss Ihre Proxykonfiguration die Konnektivität zwischen `github.com` und `api.github.com` zulassen. Weitere Informationen finden Sie unter „[{{ site.data.variables.product.prodname_ghe_server }} mit {{ site.data.variables.product.prodname_dotcom_the_website }}](/enterprise/{{ currentVersion }}/admin/guides/developer-workflow/connecting-github-enterprise-server-to-github-com) verbinden“.

{% endnote %}

{{ site.data.reusables.enterprise_site_admin_settings.access-settings }}
{{ site.data.reusables.enterprise_site_admin_settings.management-console }}
{{ site.data.reusables.enterprise_management_console.privacy }}
4. Geben Sie unter **HTTP Proxy Server** (HTTP-Proxyserver) die URL Ihres Proxyservers ein. ![Feld zur Eingabe der HTTP-Proxyserver-URL](/assets/images/enterprise/management-console/http-proxy-field.png)
5. Geben Sie optional unter **HTTP Proxy Exclusion** (HTTP-Proxyausschluss) die Hosts ein, für die kein Proxyzugriff erforderlich ist. Trennen Sie dabei die Hosts durch Kommas voneinander. ![Feld zur Eingabe von HTTP-Proxyausschlüssen](/assets/images/enterprise/management-console/http-proxy-exclusion-field.png)
{{ site.data.reusables.enterprise_management_console.save-settings }}
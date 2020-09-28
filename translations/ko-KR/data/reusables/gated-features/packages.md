{{ site.data.variables.product.prodname_registry }} is available with {{ site.data.variables.product.prodname_free_user }}, {{ site.data.variables.product.prodname_pro }}, {{ site.data.variables.product.prodname_free_team }} for organizations, {{ site.data.variables.product.prodname_team }}, {{ site.data.variables.product.prodname_ghe_cloud }}, {{ site.data.variables.product.prodname_ghe_server }} 2.22, and {{ site.data.variables.product.prodname_ghe_one }}.
{% if currentVersion == "free-pro-team@latest" %}
<br>{{ site.data.variables.product.prodname_registry }} is not available for private repositories owned by accounts using legacy per-repository plans. Also, accounts using legacy per-repository plans cannot access {{ site.data.variables.product.prodname_github_container_registry }} since these accounts are billed by repository. {{ site.data.reusables.gated-features.more-info }}
{% endif %}
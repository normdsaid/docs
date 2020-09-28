---
title: 浏览 GitHub Advisory Database 中的安全漏洞
intro: '{{ site.data.variables.product.prodname_advisory_database }} 允许您浏览或搜索影响 {{ site.data.variables.product.company_short }} 上开源项目的漏洞。'
versions:
  free-pro-team: '*'
---

### 关于安全漏洞

{{ site.data.reusables.repositories.a-vulnerability-is }}

{{ site.data.variables.product.product_name }} will send you {{ site.data.variables.product.prodname_dependabot_alerts }} if we detect that any of the vulnerabilities from the {{ site.data.variables.product.prodname_advisory_database }} affect the packages that your repository depends on. 更多信息请参阅“[关于易受攻击的依赖项的警报](/github/managing-security-vulnerabilities/about-alerts-for-vulnerable-dependencies)”。

### 关于 {{ site.data.variables.product.prodname_advisory_database }}

{{ site.data.variables.product.prodname_advisory_database }} 包含已映射到 {{ site.data.variables.product.company_short }} 依赖关系图跟踪的软件包的安全漏洞列表。 {{ site.data.reusables.repositories.tracks-vulnerabilities }}

Each security advisory contains information about the vulnerability, including the description, severity, affected package, package ecosystem, affected versions and patched versions, impact, and optional information such as references, workarounds, and credits. 此外，国家漏洞数据库列表中的公告包含 CVE 记录链接，通过链接可以查看漏洞、其 CVSS 得分及其质化严重等级的更多详细信息。 更多信息请参阅国家标准和技术研究所 (National Institute of Standards and Technology) 的“[国家漏洞数据库](https://nvd.nist.gov/)”。

我们在[常见漏洞评分系统 (CVSS) 第 2.1.2 节](https://www.first.org/cvss/specification-document)中定义了以下四种可能的严重性等级：
- 低
- 中
- 高
- 关键

The {{ site.data.variables.product.prodname_advisory_database }} uses CVSS version 3.0 standards and the CVSS levels described above. {{ site.data.variables.product.product_name }} doesn't publish CVSS scores.

{{ site.data.reusables.repositories.github-security-lab }}

### 访问 {{ site.data.variables.product.prodname_advisory_database }} 中的通告

1. 导航到 https://github.com/advisories。
2. Optionally, to filter the list, use any of the drop-down menus. ![下拉过滤器](/assets/images/help/security/advisory-database-dropdown-filters.png)
3. 单击任何通告以查看详情。

{% note %}

也可以使用 GraphQL API 访问数据库。 更多信息请参阅“[`security_advisory` web 挂钩事件](/webhooks/event-payloads/#security_advisory)”。

{% endnote %}

### 搜索 {{ site.data.variables.product.prodname_advisory_database }}
您可以搜索数据库，并使用限定符将搜索范围缩小到在特定日期、特定生态系统或特定库中创建的公告。

{{ site.data.reusables.time_date.date_format }} {{ site.data.reusables.time_date.time_format }}

{{ site.data.reusables.search.date_gt_lt }}

| 限定符                   | 示例                                                                                                                      |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `ecosystem:ECOSYSTEM` | [**ecosystem:npm**](https://github.com/advisories?utf8=%E2%9C%93&query=ecosystem%3Anpm) 只显示影响 NPM 包的通告。                 |
| `severity:LEVEL`      | [**severity:high**](https://github.com/advisories?utf8=%E2%9C%93&query=severity%3Ahigh) 只显示严重程度高的公告。                    |
| `affects:LIBRARY`     | [**affects:lodash**](https://github.com/advisories?utf8=%E2%9C%93&query=affects%3Alodash) 只显示影响 lodash 库的通告。            |
| `sort:created-asc`    | [**sort:created-asc**](https://github.com/advisories?utf8=%E2%9C%93&query=sort%3Acreated-asc) 按照时间顺序对通告排序，最早的通告排在最前面。   |
| `sort:created-desc`   | [**sort:created-desc**](https://github.com/advisories?utf8=%E2%9C%93&query=sort%3Acreated-desc) 按照时间顺序对通告排序，最新的通告排在最前面。 |
| `sort:updated-asc`    | [**sort:updated-asc**](https://github.com/advisories?utf8=%E2%9C%93&query=sort%3Aupdated-asc) 按照更新顺序排序，最早更新的排在最前面。      |
| `sort:updated-desc`   | [**sort:updated-desc**](https://github.com/advisories?utf8=%E2%9C%93&query=sort%3Aupdated-desc) 按照更新顺序排序，最近更新的排在最前面。    |
| `is:withdrawn`        | [**is:withdrawn**](https://github.com/advisories?utf8=%E2%9C%93&query=is%3Awithdrawn) 只显示已经撤销的通告。                       |
| `created:YYYY-MM-DD`  | [**created:2019-10-31**](https://github.com/advisories?utf8=%E2%9C%93&query=created%3A2019-10-31) 只显示此日期创建的通告。          |
| `updated:YYYY-MM-DD`  | [**updated:2019-10-31**](https://github.com/advisories?utf8=%E2%9C%93&query=updated%3A2019-10-31) 只显示此日期更新的通告。          |

### 延伸阅读

- MITRE 的[“漏洞”定义](https://cve.mitre.org/about/terminology.html#vulnerability)
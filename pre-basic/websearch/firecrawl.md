---
description: 在 Cherry Studio 中使用 Firecrawl 联网搜索与 URL 获取
icon: fire
---

# Firecrawl 联网配置

[Firecrawl](https://www.firecrawl.dev/search?utm_source=cherry-studio&utm_medium=integration) 是面向 AI 的网页上下文 API，可搜索、抓取网页并与之交互。在 Cherry Studio 中，它可以同时用作 **搜索服务商** 和 **URL 获取服务商**：

* **搜索**：根据你的问题检索网页，每条结果附带网页正文（Markdown），而不只是摘要；
* **URL 获取**：抓取指定网址的正文并转换为 Markdown，支持 PDF 和需要 JavaScript 渲染的页面。

{% hint style="info" %}
Firecrawl **无需 API 密钥** 即可使用（免费额度）。填写自己的密钥可以提高额度。
{% endhint %}

## 用作搜索服务商

1. 打开 `设置 → 网络搜索`。
2. 在 **搜索服务商** 分区的下拉框中选择 **Firecrawl**，选中即作为默认搜索服务商。
3. 回到对话，点击输入框工具栏中的 🌐 **小地球** 图标开启联网。

<figure><img src="../../.gitbook/assets/v2/websearch-provider-dropdown.png" alt="网络搜索设置中的服务商下拉框，列表中包含 Firecrawl"><figcaption><p>在下拉框中选择 Firecrawl</p></figcaption></figure>

## 用作 URL 获取服务商

1. 打开 `设置 → 网络搜索`。
2. 在 **URL 获取服务商** 分区的下拉框中选择 **Firecrawl**。

之后，对话中需要读取网页正文时，Cherry Studio 会通过 Firecrawl 抓取。

{% hint style="info" %}
如果当前模型自带网页搜索或 URL 获取，且开启了 **优先使用模型内置 Web 工具**（默认开启），会先使用模型内置工具，不可用时再切换到上面配置的服务。想始终使用 Firecrawl，请关闭该开关。
{% endhint %}

## 填写 API 密钥（可选）

不填密钥也能用。免费额度用完、遇到限流提示，或需要更高额度时：

1. 打开 Firecrawl 的 [API Keys 页面](https://www.firecrawl.dev/app/api-keys?utm_source=cherry-studio&utm_medium=integration)，登录后复制密钥。也可以点击设置里 **API 密钥** 旁的 **获取密钥** 跳转。
2. 在 `设置 → 网络搜索` 中选中 Firecrawl，把密钥粘贴到 **API 密钥** 输入框。
3. 点击输入框右侧的检测图标（悬停显示「检测」），确认密钥可用。

{% hint style="info" %}
搜索和 URL 获取共用同一组 Firecrawl 密钥，只需填写一次。
{% endhint %}

## 使用自托管的 Firecrawl

如果你自己部署了 Firecrawl（参考 [自托管文档](https://docs.firecrawl.dev/contributing/self-host)），把 **API 地址** 从默认的 `https://api.firecrawl.dev` 改成你的服务地址。

{% hint style="warning" %}
**搜索服务商** 和 **URL 获取服务商** 两个分区的 API 地址是分开保存的。如果两处都选了 Firecrawl，需要分别修改。
{% endhint %}

***

### 获取帮助与提交反馈

如果您在配置或使用过程中遇到任何疑问、Bug 或有功能改进建议，请参考 [反馈与建议](../../question-contact/suggestions.md) 中提供的官方渠道。

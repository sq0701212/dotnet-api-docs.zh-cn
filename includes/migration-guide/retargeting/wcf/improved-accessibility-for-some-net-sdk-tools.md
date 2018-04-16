### <a name="improved-accessibility-for-some-net-sdk-tools"></a><span data-ttu-id="499e3-101">一些.NET SDK 工具的改进辅助功能</span><span class="sxs-lookup"><span data-stu-id="499e3-101">Improved accessibility for some .NET SDK tools</span></span>

|   |   |
|---|---|
|<span data-ttu-id="499e3-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="499e3-102">Details</span></span>|<span data-ttu-id="499e3-103">在.NET Framework SDK 4.7.1 中，svcconfigedit.exe 和 svctraceviewer.exe 工具已得到改进通过修复各种可访问性问题。</span><span class="sxs-lookup"><span data-stu-id="499e3-103">In the .NET Framework SDK 4.7.1, the svcconfigedit.exe and svctraceviewer.exe tools have been improved by fixing varied accessibility issues.</span></span> <span data-ttu-id="499e3-104">这些大部分了未定义的名称或未被正确实现特定的 UI 自动化模式等的小问题。</span><span class="sxs-lookup"><span data-stu-id="499e3-104">Most of these were small issues like a name not being defined or certain UI automation patterns not being implemented correctly.</span></span> <span data-ttu-id="499e3-105">虽然许多用户不会注意这些不正确的值，使用辅助技术，如屏幕阅读器的客户将发现这些 SDK 工具更易于访问。</span><span class="sxs-lookup"><span data-stu-id="499e3-105">While many users wouldn’t be aware of these incorrect values, customers who use assistive technologies like screen readers will find these SDK tools more accessible.</span></span> <span data-ttu-id="499e3-106">当然，这些修补程序更改某些以前的行为，如键盘焦点订单。若要获取所有可访问性修复在这些工具中，可以以下到 app.config 文件：</span><span class="sxs-lookup"><span data-stu-id="499e3-106">Certainly, these fixes change some previous behaviors, like keyboard focus order.In order to get all the accessibility fixes in these tools, you can the following to your app.config file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="499e3-107">范围</span><span class="sxs-lookup"><span data-stu-id="499e3-107">Scope</span></span>|<span data-ttu-id="499e3-108">边缘</span><span class="sxs-lookup"><span data-stu-id="499e3-108">Edge</span></span>|
|<span data-ttu-id="499e3-109">版本</span><span class="sxs-lookup"><span data-stu-id="499e3-109">Version</span></span>|<span data-ttu-id="499e3-110">4.7.1</span><span class="sxs-lookup"><span data-stu-id="499e3-110">4.7.1</span></span>|
|<span data-ttu-id="499e3-111">类型</span><span class="sxs-lookup"><span data-stu-id="499e3-111">Type</span></span>|<span data-ttu-id="499e3-112">重定目标</span><span class="sxs-lookup"><span data-stu-id="499e3-112">Retargeting</span></span>|

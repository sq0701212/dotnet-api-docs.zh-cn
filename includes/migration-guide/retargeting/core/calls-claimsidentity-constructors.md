### <a name="calls-to-claimsidentity-constructors"></a><span data-ttu-id="f6313-101">对 ClaimsIdentity 构造函数的调用</span><span class="sxs-lookup"><span data-stu-id="f6313-101">Calls to ClaimsIdentity constructors</span></span>

|   |   |
|---|---|
|<span data-ttu-id="f6313-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="f6313-102">Details</span></span>|<span data-ttu-id="f6313-103">从.NET Framework 4.6.2 开始，没有在如何更改<xref:System.Security.Claims.ClaimsIdentity>带构造函数<xref:System.Security.Principal.IIdentity?displayProperty=name>参数集<xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name>属性。</span><span class="sxs-lookup"><span data-stu-id="f6313-103">Starting with the .NET Framework 4.6.2, there is a change in how <xref:System.Security.Claims.ClaimsIdentity> constructors with an <xref:System.Security.Principal.IIdentity?displayProperty=name> parameter set the <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> property.</span></span> <span data-ttu-id="f6313-104">如果 <xref:System.Security.Principal.IIdentity?displayProperty=name> 参数是 <xref:System.Security.Claims.ClaimsIdentity> 对象，且该 <xref:System.Security.Claims.ClaimsIdentity> 对象的 <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> 属性不为 <code>null</code>，则 <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> 属性是使用 <xref:System.Security.Claims.ClaimsIdentity.Clone> 方法附加的。</span><span class="sxs-lookup"><span data-stu-id="f6313-104">If the <xref:System.Security.Principal.IIdentity?displayProperty=name> argument is a <xref:System.Security.Claims.ClaimsIdentity> object, and the <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> property of that <xref:System.Security.Claims.ClaimsIdentity> object is not <code>null</code>, the <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> property is attached by using the <xref:System.Security.Claims.ClaimsIdentity.Clone> method.</span></span> <span data-ttu-id="f6313-105">Framework 4.6.1 及早期版本中，在<xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name>作为现有的引用附加属性。由于此更改，从.NET Framework 4.6.2，开始<xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name>属性的新<xref:System.Security.Claims.ClaimsIdentity>对象是否不等于<xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name>属性的构造函数的<xref:System.Security.Principal.IIdentity?displayProperty=name>自变量。</span><span class="sxs-lookup"><span data-stu-id="f6313-105">In the Framework 4.6.1 and earlier versions, the <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> property is attached as an existing reference.Because of this change, starting with the .NET Framework 4.6.2, the <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> property of the new <xref:System.Security.Claims.ClaimsIdentity> object is not equal to the <xref:System.Security.Claims.ClaimsIdentity.Actor?displayProperty=name> property of the constructor's <xref:System.Security.Principal.IIdentity?displayProperty=name> argument.</span></span> <span data-ttu-id="f6313-106">在.NET Framework 4.6.1 及更早版本中，它是相等的。</span><span class="sxs-lookup"><span data-stu-id="f6313-106">In the .NET Framework 4.6.1 and earlier versions, it is equal.</span></span>|
|<span data-ttu-id="f6313-107">建议</span><span class="sxs-lookup"><span data-stu-id="f6313-107">Suggestion</span></span>|<span data-ttu-id="f6313-108">如果不需要此行为，可以在应用程序配置文件中将 <code>Switch.System.Security.ClaimsIdentity.SetActorAsReferenceWhenCopyingClaimsIdentity</code> 开关设置为 <code>true</code>，从而还原旧行为。</span><span class="sxs-lookup"><span data-stu-id="f6313-108">If this behavior is undesirable, you can restore the previous behavior by setting the <code>Switch.System.Security.ClaimsIdentity.SetActorAsReferenceWhenCopyingClaimsIdentity</code> switch in your application configuration file to <code>true</code>.</span></span> <span data-ttu-id="f6313-109">这要求你添加到以下<code>&lt;runtime&gt;</code>的 web.config 文件的部分：</span><span class="sxs-lookup"><span data-stu-id="f6313-109">This requires that you add the following to the <code>&lt;runtime&gt;</code> section of your web.config file:</span></span><pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.ClaimsIdentity.SetActorAsReferenceWhenCopyingClaimsIdentity=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="f6313-110">范围</span><span class="sxs-lookup"><span data-stu-id="f6313-110">Scope</span></span>|<span data-ttu-id="f6313-111">边缘</span><span class="sxs-lookup"><span data-stu-id="f6313-111">Edge</span></span>|
|<span data-ttu-id="f6313-112">版本</span><span class="sxs-lookup"><span data-stu-id="f6313-112">Version</span></span>|<span data-ttu-id="f6313-113">4.6.2</span><span class="sxs-lookup"><span data-stu-id="f6313-113">4.6.2</span></span>|
|<span data-ttu-id="f6313-114">类型</span><span class="sxs-lookup"><span data-stu-id="f6313-114">Type</span></span>|<span data-ttu-id="f6313-115">重定目标</span><span class="sxs-lookup"><span data-stu-id="f6313-115">Retargeting</span></span>|
|<span data-ttu-id="f6313-116">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="f6313-116">Affected APIs</span></span>|<ul><li><xref:System.Security.Claims.ClaimsIdentity.%23ctor(System.Security.Principal.IIdentity)?displayProperty=nameWithType></li><li><xref:System.Security.Claims.ClaimsIdentity.%23ctor(System.Security.Principal.IIdentity,System.Collections.Generic.IEnumerable{System.Security.Claims.Claim})?displayProperty=nameWithType></li><li><xref:System.Security.Claims.ClaimsIdentity.%23ctor(System.Security.Principal.IIdentity,System.Collections.Generic.IEnumerable{System.Security.Claims.Claim},System.String,System.String,System.String)?displayProperty=nameWithType></li></ul>|

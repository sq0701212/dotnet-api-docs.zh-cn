### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a><span data-ttu-id="494a6-101">引发 NullReferenceException HttpRuntime.AppDomainAppPath</span><span class="sxs-lookup"><span data-stu-id="494a6-101">HttpRuntime.AppDomainAppPath Throws a NullReferenceException</span></span>

|   |   |
|---|---|
|<span data-ttu-id="494a6-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="494a6-102">Details</span></span>|<span data-ttu-id="494a6-103">在.NET Framework 4.6.2 中，则运行时会引发<code>T:System.NullReferenceException</code>检索时<code>P:System.Web.HttpRuntime.AppDomainAppPath</code>包含 null 字符的值。在.NET Framework 4.6.1 和早期版本中，则运行时会引发<code>T:System.ArgumentNullException</code>。</span><span class="sxs-lookup"><span data-stu-id="494a6-103">In the .NET Framework 4.6.2, the runtime throws a <code>T:System.NullReferenceException</code> when retrieving a <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> value that includes null characters.In the .NET Framework 4.6.1 and earlier versions, the runtime throws an <code>T:System.ArgumentNullException</code>.</span></span>|
|<span data-ttu-id="494a6-104">建议</span><span class="sxs-lookup"><span data-stu-id="494a6-104">Suggestion</span></span>|<span data-ttu-id="494a6-105">你可以执行对此更改作出响应，请按照任一操作：</span><span class="sxs-lookup"><span data-stu-id="494a6-105">You can do either of the follow to respond to this change:</span></span><ul><li><span data-ttu-id="494a6-106">处理<code>T:System.NullReferenceException</code>如果你的应用程序在.NET Framework 4.6.2 上运行。</span><span class="sxs-lookup"><span data-stu-id="494a6-106">Handle the <code>T:System.NullReferenceException</code> if you application is running on the .NET Framework 4.6.2.</span></span></li><li><span data-ttu-id="494a6-107">升级到.NET Framework 4.7，也不能还原以前的行为会引发<code>T:System.ArgumentNullException</code>。</span><span class="sxs-lookup"><span data-stu-id="494a6-107">Upgrade to the .NET Framework 4.7, which restores the previous behavior and throws an <code>T:System.ArgumentNullException</code>.</span></span></li></ul>|
|<span data-ttu-id="494a6-108">范围</span><span class="sxs-lookup"><span data-stu-id="494a6-108">Scope</span></span>|<span data-ttu-id="494a6-109">边缘</span><span class="sxs-lookup"><span data-stu-id="494a6-109">Edge</span></span>|
|<span data-ttu-id="494a6-110">版本</span><span class="sxs-lookup"><span data-stu-id="494a6-110">Version</span></span>|<span data-ttu-id="494a6-111">4.6.2</span><span class="sxs-lookup"><span data-stu-id="494a6-111">4.6.2</span></span>|
|<span data-ttu-id="494a6-112">类型</span><span class="sxs-lookup"><span data-stu-id="494a6-112">Type</span></span>|<span data-ttu-id="494a6-113">重定目标</span><span class="sxs-lookup"><span data-stu-id="494a6-113">Retargeting</span></span>|
|<span data-ttu-id="494a6-114">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="494a6-114">Affected APIs</span></span>|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

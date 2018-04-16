### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a><span data-ttu-id="f9cbc-101">SignedXml.GetPublicKey 中返回 RSACng 对 net462 （或激活），而不重定目标更改</span><span class="sxs-lookup"><span data-stu-id="f9cbc-101">SignedXml.GetPublicKey returns RSACng on net462 (or lightup) without retargeting change</span></span>

|   |   |
|---|---|
|<span data-ttu-id="f9cbc-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="f9cbc-102">Details</span></span>|<span data-ttu-id="f9cbc-103">从.NET Framework 4.6.2，返回的对象的具体类型开始<xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType>方法 （不带特点） 从更改的 CryptoServiceProvider 实现 Cng 的实现。</span><span class="sxs-lookup"><span data-stu-id="f9cbc-103">Starting with the .NET Framework 4.6.2, the concrete type of the object returned by the <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> method changed (without a quirk) from a CryptoServiceProvider implementation to a Cng implementation.</span></span> <span data-ttu-id="f9cbc-104">这是因为实现更改从使用<code>certificate.PublicKey.Key</code>使用内部<code>certificate.GetAnyPublicKey</code>将转发到<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="f9cbc-104">This is because the implementation changed from using <code>certificate.PublicKey.Key</code> to using the internal <code>certificate.GetAnyPublicKey</code> which forwards to <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.</span></span>|
|<span data-ttu-id="f9cbc-105">建议</span><span class="sxs-lookup"><span data-stu-id="f9cbc-105">Suggestion</span></span>|<span data-ttu-id="f9cbc-106">从.NET Framework 4.7.1 上运行的应用开始，可以使用.NET Framework 4.6.1 中的默认情况下使用的 CryptoServiceProvider 实现，并通过添加下面的配置的早期版本切换到[运行时](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)你应用程序配置文件部分：</span><span class="sxs-lookup"><span data-stu-id="f9cbc-106">Starting with apps running on the .NET Framework 4.7.1, you can use the CryptoServiceProvider implementation used by default in the .NET Framework 4.6.1 and earlier versions by adding the following configuration switch to the [runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) section of your app config file:</span></span><pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="f9cbc-107">范围</span><span class="sxs-lookup"><span data-stu-id="f9cbc-107">Scope</span></span>|<span data-ttu-id="f9cbc-108">边缘</span><span class="sxs-lookup"><span data-stu-id="f9cbc-108">Edge</span></span>|
|<span data-ttu-id="f9cbc-109">版本</span><span class="sxs-lookup"><span data-stu-id="f9cbc-109">Version</span></span>|<span data-ttu-id="f9cbc-110">4.6.2</span><span class="sxs-lookup"><span data-stu-id="f9cbc-110">4.6.2</span></span>|
|<span data-ttu-id="f9cbc-111">类型</span><span class="sxs-lookup"><span data-stu-id="f9cbc-111">Type</span></span>|<span data-ttu-id="f9cbc-112">重定目标</span><span class="sxs-lookup"><span data-stu-id="f9cbc-112">Retargeting</span></span>|
|<span data-ttu-id="f9cbc-113">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="f9cbc-113">Affected APIs</span></span>|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

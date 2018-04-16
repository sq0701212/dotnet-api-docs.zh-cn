### <a name="rsacng-now-correctly-loads-rsa-keys-of-non-standard-key-size"></a><span data-ttu-id="3acbd-101">RSACng 现在正确加载非标准的密钥大小的 RSA 的密钥</span><span class="sxs-lookup"><span data-stu-id="3acbd-101">RSACng now correctly loads RSA keys of non-standard key size</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3acbd-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="3acbd-102">Details</span></span>|<span data-ttu-id="3acbd-103">在.NET Framework 4.6.2 之前的版本，客户的非标准的 RSA 证书的密钥大小不能访问通过这些密钥<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>和<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>扩展方法。</span><span class="sxs-lookup"><span data-stu-id="3acbd-103">In .NET Framework versions prior to 4.6.2, customers with non-standard key sizes for RSA certificates are unable to access those keys via the <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name> and <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name> extension methods.</span></span>  <span data-ttu-id="3acbd-104">A<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>并显示消息&quot;不支持所请求的密钥大小&quot;引发。</span><span class="sxs-lookup"><span data-stu-id="3acbd-104">A <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> with the message &quot;The requested key size is not supported&quot; is thrown.</span></span> <span data-ttu-id="3acbd-105">在.NET Framework 4.6.2 中已修复此问题。</span><span class="sxs-lookup"><span data-stu-id="3acbd-105">In .NET Framework 4.6.2 this issue has been fixed.</span></span> <span data-ttu-id="3acbd-106">同样，<xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)>和<xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)>现在，使用非标准的密钥大小而不引发<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>s。</span><span class="sxs-lookup"><span data-stu-id="3acbd-106">Similarly, <xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)> and <xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)> now work with non-standard key sizes without throwing <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>s.</span></span>|
|<span data-ttu-id="3acbd-107">建议</span><span class="sxs-lookup"><span data-stu-id="3acbd-107">Suggestion</span></span>|<span data-ttu-id="3acbd-108">如果没有任何异常处理依赖于先前行为的逻辑其中<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>引发时使用非标准的密钥大小，请考虑删除逻辑。</span><span class="sxs-lookup"><span data-stu-id="3acbd-108">If there is any exception handling logic that relies on the previous behavior where a <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> is thrown when non-standard key sizes are used, consider removing the logic.</span></span>|
|<span data-ttu-id="3acbd-109">范围</span><span class="sxs-lookup"><span data-stu-id="3acbd-109">Scope</span></span>|<span data-ttu-id="3acbd-110">边缘</span><span class="sxs-lookup"><span data-stu-id="3acbd-110">Edge</span></span>|
|<span data-ttu-id="3acbd-111">版本</span><span class="sxs-lookup"><span data-stu-id="3acbd-111">Version</span></span>|<span data-ttu-id="3acbd-112">4.6.2</span><span class="sxs-lookup"><span data-stu-id="3acbd-112">4.6.2</span></span>|
|<span data-ttu-id="3acbd-113">类型</span><span class="sxs-lookup"><span data-stu-id="3acbd-113">Type</span></span>|<span data-ttu-id="3acbd-114">重定目标</span><span class="sxs-lookup"><span data-stu-id="3acbd-114">Retargeting</span></span>|
|<span data-ttu-id="3acbd-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="3acbd-115">Affected APIs</span></span>|<ul><li><xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li></ul>|

### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a><span data-ttu-id="32f5d-101">System.Threading.Tasks.Task 释放对象后不再引发 ObjectDisposedException</span><span class="sxs-lookup"><span data-stu-id="32f5d-101">System.Threading.Tasks.Task no longer throw ObjectDisposedException after object is disposed</span></span>

|   |   |
|---|---|
|<span data-ttu-id="32f5d-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="32f5d-102">Details</span></span>|<span data-ttu-id="32f5d-103">除<xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>，<xref:System.Threading.Tasks.Task?displayProperty=name>方法将不再引发<xref:System.ObjectDisposedException?displayProperty=name>异常后释放此对象。此更改支持缓存任务的使用。</span><span class="sxs-lookup"><span data-stu-id="32f5d-103">Except for <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> methods no longer throw an <xref:System.ObjectDisposedException?displayProperty=name> exception after the object is disposed.This change supports the use of cached tasks.</span></span> <span data-ttu-id="32f5d-104">例如，方法会返回一个缓存任务来表示已完成的操作，而不是分配新任务。</span><span class="sxs-lookup"><span data-stu-id="32f5d-104">For example, a method can return a cached task to represent an already completed operation instead of allocating a new task.</span></span> <span data-ttu-id="32f5d-105">在以前的 .NET Framework 版本中无法执行此操作，因为任务的任何使用者都可以处置它（呈现为不可用）。</span><span class="sxs-lookup"><span data-stu-id="32f5d-105">This was impossible in previous .NET Framework versions, because any consumer of the task could dispose of it, which rendered it unusable.</span></span>|
|<span data-ttu-id="32f5d-106">建议</span><span class="sxs-lookup"><span data-stu-id="32f5d-106">Suggestion</span></span>|<span data-ttu-id="32f5d-107">请注意，可能不再引发任务方法<xref:System.ObjectDisposedException?displayProperty=name>在情况下当释放此对象。</span><span class="sxs-lookup"><span data-stu-id="32f5d-107">Be aware that Task methods may no longer throw <xref:System.ObjectDisposedException?displayProperty=name> in cases when the object is disposed.</span></span> <span data-ttu-id="32f5d-108">如果应用程序已根据知道任务已处理此异常，它应更新显式检查任务的状态使用<xref:System.Threading.Tasks.Task.Status>。</span><span class="sxs-lookup"><span data-stu-id="32f5d-108">If an app was depending on this exception to know that a task was disposed, it should be updated to explicitly check the task's status using <xref:System.Threading.Tasks.Task.Status>.</span></span>|
|<span data-ttu-id="32f5d-109">范围</span><span class="sxs-lookup"><span data-stu-id="32f5d-109">Scope</span></span>|<span data-ttu-id="32f5d-110">次要</span><span class="sxs-lookup"><span data-stu-id="32f5d-110">Minor</span></span>|
|<span data-ttu-id="32f5d-111">版本</span><span class="sxs-lookup"><span data-stu-id="32f5d-111">Version</span></span>|<span data-ttu-id="32f5d-112">4.5</span><span class="sxs-lookup"><span data-stu-id="32f5d-112">4.5</span></span>|
|<span data-ttu-id="32f5d-113">类型</span><span class="sxs-lookup"><span data-stu-id="32f5d-113">Type</span></span>|<span data-ttu-id="32f5d-114">运行时</span><span class="sxs-lookup"><span data-stu-id="32f5d-114">Runtime</span></span>|

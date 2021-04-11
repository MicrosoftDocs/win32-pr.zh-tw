---
title: 正在抓取工作頁面範例
description: 若要取出工作頁面，您必須呼叫 ITask QueryInterface 來取出 IProvideTaskPage 介面，然後呼叫 IProvideTaskPage GetPage。 GetPage 方法會傳回頁面的控制碼，然後可用來顯示您所要求的頁面。
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- 正在抓取工作頁面工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023643"
---
# <a name="retrieving-a-task-page-example"></a><span data-ttu-id="1593a-105">正在抓取工作頁面範例</span><span class="sxs-lookup"><span data-stu-id="1593a-105">Retrieving a Task Page Example</span></span>

<span data-ttu-id="1593a-106">若要取出工作頁面，您必須呼叫 **ITask：： QueryInterface** 來取出 [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) 介面，然後呼叫 [**IProvideTaskPage：： GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage)。</span><span class="sxs-lookup"><span data-stu-id="1593a-106">To retrieve a task page you must call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface, then call [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span></span> <span data-ttu-id="1593a-107">**GetPage** 方法會傳回頁面的控制碼，然後可用來顯示您所要求的頁面。</span><span class="sxs-lookup"><span data-stu-id="1593a-107">The **GetPage** method returns a handle to the page, which can then be used to display the page you requested.</span></span>

> [!Note]  
> <span data-ttu-id="1593a-108">在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。</span><span class="sxs-lookup"><span data-stu-id="1593a-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="1593a-109">下列程式說明如何建立新的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="1593a-109">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="1593a-110">**建立新的觸發程式**</span><span class="sxs-lookup"><span data-stu-id="1593a-110">**To create a new trigger**</span></span>

1.  <span data-ttu-id="1593a-111">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="1593a-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="1593a-112"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="1593a-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="1593a-113">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="1593a-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="1593a-114"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="1593a-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="1593a-115">呼叫 **ITask：： QueryInterface** 以抓取 [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) 介面和 [**IProvideTaskPage：： GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) 取得頁面。</span><span class="sxs-lookup"><span data-stu-id="1593a-115">Call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface and [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) to retrieve the page.</span></span>
4.  <span data-ttu-id="1593a-116">使用傳回的頁面控點顯示頁面。</span><span class="sxs-lookup"><span data-stu-id="1593a-116">Using the returned page handle, display the page.</span></span>



| <span data-ttu-id="1593a-117">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="1593a-117">For a code example of</span></span>                                   | <span data-ttu-id="1593a-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="1593a-118">See</span></span>                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1593a-119">取出和顯示已知工作的工作頁面</span><span class="sxs-lookup"><span data-stu-id="1593a-119">Retrieving and displaying the Task page of a known task</span></span> | [<span data-ttu-id="1593a-120">正在抓取工作頁面</span><span class="sxs-lookup"><span data-stu-id="1593a-120">Retrieving a Task Page</span></span>](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a><span data-ttu-id="1593a-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="1593a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1593a-122">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="1593a-122">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 
---
title: 列舉工作範例
description: 若要列舉工作，您必須呼叫 ITaskScheduler Enum 來建立列舉物件。 然後，使用列舉物件的 IEnumWorkItems 介面來列舉 [排定的工作] 資料夾中的工作。
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967277"
---
# <a name="enumerating-tasks-example"></a><span data-ttu-id="dd3bb-104">列舉工作範例</span><span class="sxs-lookup"><span data-stu-id="dd3bb-104">Enumerating Tasks Example</span></span>

<span data-ttu-id="dd3bb-105">若要列舉工作，您必須呼叫 [**ITaskScheduler：： Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) 來建立 [*列舉物件*](e.md)。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-105">To enumerate tasks, you must call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to create an [*enumeration object*](e.md).</span></span> <span data-ttu-id="dd3bb-106">然後，使用列舉物件的 [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) 介面來列舉 [排定的工作] 資料夾中的工作。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-106">Then, use the enumeration object's [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="dd3bb-107">下列程式描述如何列舉 [排定的工作] 資料夾中的工作。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-107">The following procedure describes how to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="dd3bb-108">**列舉 [排定的工作] 資料夾中的工作**</span><span class="sxs-lookup"><span data-stu-id="dd3bb-108">**To enumerate the tasks in the Scheduled Tasks folder**</span></span>

1.  <span data-ttu-id="dd3bb-109">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="dd3bb-110"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="dd3bb-110">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="dd3bb-111">呼叫 [**ITaskScheduler：： Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) 來取得列舉物件。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-111">Call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to get an enumeration object.</span></span>
3.  <span data-ttu-id="dd3bb-112">呼叫 [**IEnumWorkItems：： Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) 以取得工作。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-112">Call [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) to retrieve the tasks.</span></span> <span data-ttu-id="dd3bb-113"> (此範例會嘗試在每次呼叫時取出五個工作。 ) </span><span class="sxs-lookup"><span data-stu-id="dd3bb-113">(This example tries to retrieve five tasks with each call.)</span></span>
4.  <span data-ttu-id="dd3bb-114">處理傳回的工作。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-114">Process the tasks returned.</span></span> <span data-ttu-id="dd3bb-115"> (此範例只會將每個工作的名稱列印到螢幕。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-115">(This example simply prints the name of each task to the screen.</span></span>
5.  <span data-ttu-id="dd3bb-116">釋放資源。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-116">Release resources.</span></span> <span data-ttu-id="dd3bb-117">呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 以釋放用於名稱的記憶體。</span><span class="sxs-lookup"><span data-stu-id="dd3bb-117">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory used for names.</span></span>



| <span data-ttu-id="dd3bb-118">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="dd3bb-118">For a code example of</span></span>                                                         | <span data-ttu-id="dd3bb-119">請參閱</span><span class="sxs-lookup"><span data-stu-id="dd3bb-119">See</span></span>                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="dd3bb-120">列舉本機電腦的 [排程工作] 資料夾中的所有工作</span><span class="sxs-lookup"><span data-stu-id="dd3bb-120">Enumerating all the tasks in the Scheduled Tasks folder of the local computer</span></span> | [<span data-ttu-id="dd3bb-121">C/c + + 程式碼範例：列舉工作</span><span class="sxs-lookup"><span data-stu-id="dd3bb-121">C/C++ Code Example: Enumerating Tasks</span></span>](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a><span data-ttu-id="dd3bb-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd3bb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd3bb-123">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="dd3bb-123">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 
---
title: " (工作排程器) 的程式設計考慮"
description: 開發使用工作排程器1.0 的應用程式時，請記住下列程式設計問題。您的應用程式必須先確認工作排程器服務正在執行，然後再嘗試使用工作排程器 API 進行任何呼叫。在抓取字串時，請確定您在不再需要每個字串之後，呼叫 CoTaskMemFree 來釋放每個字串。 在抓取字串的陣列時，請務必先釋出陣列中的每個字串，然後釋放陣列本身。建立或修改工作專案（包括與工作專案相關聯的觸發程式）時，請務必呼叫 IPersistFile Save，以將工作專案儲存至磁片。使用工作排程器 API 所提供的任何介面之後，請務必呼叫 IUnknown 版本來釋放介面。 每個工作排程器物件都支援 IUnknown。
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- 開始工作排程器
- 程式設計考慮工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965877"
---
# <a name="programming-considerations-task-scheduler"></a><span data-ttu-id="58c27-107"> (工作排程器) 的程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="58c27-107">Programming Considerations (Task Scheduler)</span></span>

<span data-ttu-id="58c27-108">開發使用工作排程器1.0 的應用程式時，請記住下列程式設計問題。</span><span class="sxs-lookup"><span data-stu-id="58c27-108">When developing applications that use the Task Scheduler 1.0, keep the following programming issues in mind.</span></span>

-   <span data-ttu-id="58c27-109">您的應用程式必須先確認工作排程器服務正在執行，然後再嘗試使用工作排程器 API 進行任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="58c27-109">Your application must ensure the Task Scheduler service is running before attempting to make any calls using the Task Scheduler API.</span></span>
-   <span data-ttu-id="58c27-110">在抓取字串時，請確定您在不再需要每個字串之後，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放每個字串。</span><span class="sxs-lookup"><span data-stu-id="58c27-110">When retrieving strings, make sure that you call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release each string after it is no longer needed.</span></span> <span data-ttu-id="58c27-111">在抓取字串的陣列時，請務必先釋出陣列中的每個字串，然後釋放陣列本身。</span><span class="sxs-lookup"><span data-stu-id="58c27-111">When retrieving arrays of strings, make sure you first release each string in the array and then release the array itself.</span></span>
-   <span data-ttu-id="58c27-112">建立或修改工作專案（包括與工作專案相關聯的觸發程式）時，請務必呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) ，以將工作專案儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="58c27-112">When creating or modifying a work item, including triggers associated with a work item, make sure you call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the work item to disk.</span></span>
-   <span data-ttu-id="58c27-113">使用工作排程器 API 所提供的任何介面之後，請務必呼叫 [**IUnknown：： release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 來釋放介面。</span><span class="sxs-lookup"><span data-stu-id="58c27-113">After using any of the interfaces that are provided by the Task Scheduler API, make sure you call [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the interface.</span></span> <span data-ttu-id="58c27-114">每個工作排程器物件都支援 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 。</span><span class="sxs-lookup"><span data-stu-id="58c27-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is supported by each Task Scheduler object.</span></span>

<span data-ttu-id="58c27-115">工作排程器檔的 Using 區段提供許多遵循這些指導方針的範例。</span><span class="sxs-lookup"><span data-stu-id="58c27-115">The Using section of the Task Scheduler documentation provides numerous examples that follow these guidelines.</span></span> <span data-ttu-id="58c27-116">下表提供其中一些範例的跳躍。</span><span class="sxs-lookup"><span data-stu-id="58c27-116">The table below provides jumps to some of these examples.</span></span>

| <span data-ttu-id="58c27-117">如需範例</span><span class="sxs-lookup"><span data-stu-id="58c27-117">For an example of</span></span>         | <span data-ttu-id="58c27-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="58c27-118">See</span></span>                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c27-119">釋放字串</span><span class="sxs-lookup"><span data-stu-id="58c27-119">Releasing strings</span></span>         | [<span data-ttu-id="58c27-120">正在抓取工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="58c27-120">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="58c27-121">將工作專案儲存至磁片</span><span class="sxs-lookup"><span data-stu-id="58c27-121">Saving work items to disk</span></span> | [<span data-ttu-id="58c27-122">設定工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="58c27-122">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |
| <span data-ttu-id="58c27-123">釋放介面</span><span class="sxs-lookup"><span data-stu-id="58c27-123">Releasing interfaces</span></span>      | [<span data-ttu-id="58c27-124">使用 NewWorkItem 範例建立工作</span><span class="sxs-lookup"><span data-stu-id="58c27-124">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |



 

 

 

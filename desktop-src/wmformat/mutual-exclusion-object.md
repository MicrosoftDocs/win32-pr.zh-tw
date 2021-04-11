---
title: 相互排除物件
description: 相互排除物件
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Media Format SDK，相互排除物件
- Advanced Systems Format (ASF) ，相互排除物件
- ASF (Advanced Systems Format) ，相互排除物件
- 物件，相互排除物件
- 相互排除，物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092577"
---
# <a name="mutual-exclusion-object"></a><span data-ttu-id="8f4b8-108">相互排除物件</span><span class="sxs-lookup"><span data-stu-id="8f4b8-108">Mutual Exclusion Object</span></span>

<span data-ttu-id="8f4b8-109">互斥物件是用來指定多個資料流程，一次只能傳遞一個。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-109">A mutual exclusion object is used to specify a number of streams, of which only one can be delivered at a time.</span></span> <span data-ttu-id="8f4b8-110">這可以透過數種方式來使用，例如以數種語言提供音訊串流作為一個影片串流的聲段。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-110">This can be used in several ways, such as providing an audio stream in several languages as the soundtrack for one video stream.</span></span>

<span data-ttu-id="8f4b8-111">相互排除是設定檔的選擇性部分。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-111">Mutual exclusion is an optional part of a profile.</span></span> <span data-ttu-id="8f4b8-112">您可以針對設定檔中現有的相互排除資訊建立相互排除物件，或建立空白，準備接收新資料。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-112">Mutual exclusion objects can be created for existing mutual exclusion information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="8f4b8-113">相互排除物件不能獨立存在於設定檔物件中。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-113">Mutual exclusion objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="8f4b8-114">若要儲存相互排除物件的內容，您必須呼叫 [**IWMProfile：： AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-114">To save the contents of a mutual exclusion object, you must call [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

<span data-ttu-id="8f4b8-115">若要建立相互排除物件，請使用下列其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-115">To create a mutual exclusion object, use one of the following methods.</span></span>



| <span data-ttu-id="8f4b8-116">方法</span><span class="sxs-lookup"><span data-stu-id="8f4b8-116">Method</span></span>                                                                              | <span data-ttu-id="8f4b8-117">描述</span><span class="sxs-lookup"><span data-stu-id="8f4b8-117">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f4b8-118">**IWMProfile::CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-118">**IWMProfile::CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="8f4b8-119">建立相互排除的物件，而不包含任何資料。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-119">Creates a mutual exclusion object without any data.</span></span>                                                                                                         |
| [<span data-ttu-id="8f4b8-120">**IWMProfile::GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-120">**IWMProfile::GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="8f4b8-121">建立從設定檔填入資料的相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-121">Creates a mutual exclusion object populated with data from a profile.</span></span> <span data-ttu-id="8f4b8-122">使用互斥索引來識別所需的相互排除資訊。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-122">Uses the mutual exclusion index to identify the desired mutual exclusion information.</span></span> |



 

<span data-ttu-id="8f4b8-123">上表中的兩個方法都會設定 **IWMMutualExclusion** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-123">Both methods in the preceding table set a pointer to an **IWMMutualExclusion** interface.</span></span> <span data-ttu-id="8f4b8-124">**IWMMutualExclusion** 會繼承 **IWMStreamList** 介面，且永遠不需要直接存取。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-124">The **IWMStreamList** interface is inherited by **IWMMutualExclusion** and never needs to be accessed directly.</span></span> <span data-ttu-id="8f4b8-125">您可以藉由呼叫 **QueryInterface** 方法來取得相互排除物件的另一個介面。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-125">The other interface of the mutual exclusion object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="8f4b8-126">每個相互排除物件都支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-126">The following interfaces are supported by every mutual exclusion object.</span></span>



| <span data-ttu-id="8f4b8-127">介面</span><span class="sxs-lookup"><span data-stu-id="8f4b8-127">Interface</span></span>                                          | <span data-ttu-id="8f4b8-128">描述</span><span class="sxs-lookup"><span data-stu-id="8f4b8-128">Description</span></span>                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f4b8-129">**IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-129">**IWMMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | <span data-ttu-id="8f4b8-130">設定並抓取要使用的互斥類型。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-130">Sets and retrieves the type of mutual exclusion to be used.</span></span>                                                                                            |
| [<span data-ttu-id="8f4b8-131">**IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-131">**IWMMutualExclusion2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | <span data-ttu-id="8f4b8-132">將資料流程組織成記錄，這些記錄可用來建立複雜的互斥案例。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-132">Organizes streams into records, which can be used to create complex mutual exclusion scenarios.</span></span> <span data-ttu-id="8f4b8-133">繼承 **IWMMutualExclusion** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-133">Inherits all of the methods of **IWMMutualExclusion**.</span></span> |
| [<span data-ttu-id="8f4b8-134">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-134">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="8f4b8-135">管理互斥資料流程的清單。</span><span class="sxs-lookup"><span data-stu-id="8f4b8-135">Manages the list of mutually exclusive streams.</span></span>                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="8f4b8-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f4b8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f4b8-137">**互斥**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-137">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="8f4b8-138">**物件**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-138">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="8f4b8-139">**設定檔管理員物件**</span><span class="sxs-lookup"><span data-stu-id="8f4b8-139">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 





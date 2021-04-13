---
title: 頻寬共用物件
description: 頻寬共用物件
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media Format SDK，頻寬共用物件
- Advanced Systems Format (ASF) 、頻寬共用物件
- ASF (Advanced 系統格式) 、頻寬共用物件
- 物件，頻寬共用物件
- 頻寬共用、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374494"
---
# <a name="bandwidth-sharing-object"></a><span data-ttu-id="f2590-108">頻寬共用物件</span><span class="sxs-lookup"><span data-stu-id="f2590-108">Bandwidth Sharing Object</span></span>

<span data-ttu-id="f2590-109">頻寬共用物件是用來指出兩個或多個資料流程（不論其個別的位元速率為何）永遠不會在兩者之間使用超過指定的頻寬量。</span><span class="sxs-lookup"><span data-stu-id="f2590-109">A bandwidth sharing object is used to indicate that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth between them.</span></span> <span data-ttu-id="f2590-110">這是純粹的參考物件;此 SDK 的任何物件不會以程式設計的方式強制執行在其中設定的位速度。</span><span class="sxs-lookup"><span data-stu-id="f2590-110">This is a purely informational object; the bit rates set within it are not enforced programmatically by any object of this SDK.</span></span>

<span data-ttu-id="f2590-111">頻寬共用資訊是設定檔的選擇性部分。</span><span class="sxs-lookup"><span data-stu-id="f2590-111">Bandwidth sharing information is an optional part of a profile.</span></span> <span data-ttu-id="f2590-112">您可以為設定檔中現有的頻寬共用資訊建立頻寬共用物件，也可以建立空的，準備好接收新的資料。</span><span class="sxs-lookup"><span data-stu-id="f2590-112">Bandwidth sharing objects can be created for existing bandwidth sharing information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="f2590-113">設定檔物件不能獨立存在頻寬共用物件。</span><span class="sxs-lookup"><span data-stu-id="f2590-113">Bandwidth sharing objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="f2590-114">若要儲存頻寬共用物件的內容，您必須呼叫 [**IWMProfile3：： AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)。</span><span class="sxs-lookup"><span data-stu-id="f2590-114">To save the contents of a bandwidth sharing object, you must call [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span></span>

<span data-ttu-id="f2590-115">若要建立頻寬共用物件，請呼叫下列其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="f2590-115">To create a bandwidth sharing object, call one of the following methods.</span></span>



| <span data-ttu-id="f2590-116">方法</span><span class="sxs-lookup"><span data-stu-id="f2590-116">Method</span></span>                                                                                  | <span data-ttu-id="f2590-117">描述</span><span class="sxs-lookup"><span data-stu-id="f2590-117">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2590-118">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="f2590-118">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | <span data-ttu-id="f2590-119">建立不含任何資料的頻寬共用物件。</span><span class="sxs-lookup"><span data-stu-id="f2590-119">Creates a bandwidth sharing object without any data.</span></span>                                                                                                           |
| [<span data-ttu-id="f2590-120">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="f2590-120">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | <span data-ttu-id="f2590-121">建立以設定檔中的資料填入的頻寬共用物件。</span><span class="sxs-lookup"><span data-stu-id="f2590-121">Creates a bandwidth sharing object populated with data from a profile.</span></span> <span data-ttu-id="f2590-122">使用頻寬共用索引來識別所需的頻寬共用資訊。</span><span class="sxs-lookup"><span data-stu-id="f2590-122">Uses the bandwidth sharing index to identify the desired bandwidth sharing information.</span></span> |



 

<span data-ttu-id="f2590-123">上表中的兩個方法都會設定 **IWMBandwidthSharing** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f2590-123">Both methods in the preceding table set a pointer to an **IWMBandwidthSharing** interface.</span></span> <span data-ttu-id="f2590-124">**IWMBandwidthSharing** 會繼承 **IWMStreamList** 介面，因此不需要使用這個物件來呼叫 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="f2590-124">The **IWMStreamList** interface is inherited by **IWMBandwidthSharing**, so there is no need to call **QueryInterface** with this object.</span></span>

<span data-ttu-id="f2590-125">每個頻寬共用物件都支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="f2590-125">The following interfaces are supported by every bandwidth sharing object.</span></span>



| <span data-ttu-id="f2590-126">介面</span><span class="sxs-lookup"><span data-stu-id="f2590-126">Interface</span></span>                                          | <span data-ttu-id="f2590-127">描述</span><span class="sxs-lookup"><span data-stu-id="f2590-127">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="f2590-128">**IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="f2590-128">**IWMBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | <span data-ttu-id="f2590-129">管理將共用頻寬之資料流程群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2590-129">Manages the properties of a group of streams that will share bandwidth.</span></span> |
| [<span data-ttu-id="f2590-130">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="f2590-130">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="f2590-131">管理將共用頻寬的資料流程清單。</span><span class="sxs-lookup"><span data-stu-id="f2590-131">Manages the list of streams that will share bandwidth.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="f2590-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2590-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2590-133">**頻寬共用**</span><span class="sxs-lookup"><span data-stu-id="f2590-133">**Bandwidth Sharing**</span></span>](bandwidth-sharing.md)
</dt> <dt>

[<span data-ttu-id="f2590-134">**設定檔管理員物件**</span><span class="sxs-lookup"><span data-stu-id="f2590-134">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="f2590-135">**設定檔物件**</span><span class="sxs-lookup"><span data-stu-id="f2590-135">**Profile Object**</span></span>](profile-object.md)
</dt> </dl>

 

 





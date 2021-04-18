---
title: 串流優先順序物件
description: 串流優先順序物件
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media Format SDK，資料流程優先順序物件
- Advanced Systems Format (ASF) 、串流優先順序物件
- ASF (Advanced 系統格式) 、串流優先順序物件
- 物件，資料流程優先順序物件
- 串流優先權物件
- 資料流程，資料流程優先順序物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965633"
---
# <a name="stream-prioritization-object"></a><span data-ttu-id="7a05d-109">串流優先順序物件</span><span class="sxs-lookup"><span data-stu-id="7a05d-109">Stream Prioritization Object</span></span>

<span data-ttu-id="7a05d-110">資料流程優先權物件是用來指定設定檔中資料流程的重要性順序。</span><span class="sxs-lookup"><span data-stu-id="7a05d-110">A stream prioritization object is used to specify an order of importance for the streams in a profile.</span></span> <span data-ttu-id="7a05d-111">當完全播放因為位元速率限制而無法完成時，最低優先順序的資料流程將會先卸載。</span><span class="sxs-lookup"><span data-stu-id="7a05d-111">When full playback is not possible due to bit-rate limitations, the lowest priority streams will be the first to be dropped.</span></span>

<span data-ttu-id="7a05d-112">您可以為設定檔中現有的資料流程優先順序資料建立資料流程優先權物件，或建立空白的資料流程，準備好接收新的資料。</span><span class="sxs-lookup"><span data-stu-id="7a05d-112">Stream prioritization objects can be created for existing stream prioritization data in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="7a05d-113">資料流程優先權物件不能獨立存在於設定檔物件中。</span><span class="sxs-lookup"><span data-stu-id="7a05d-113">Stream prioritization objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="7a05d-114">若要儲存資料流程優先權物件的內容，您必須呼叫 [**IWMProfile3：： SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)。</span><span class="sxs-lookup"><span data-stu-id="7a05d-114">To save the contents of a stream prioritization object, you must call [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span></span> <span data-ttu-id="7a05d-115">若要建立資料流程優先權物件，請使用下列其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="7a05d-115">To create a stream prioritization object, use one of the following methods.</span></span>



| <span data-ttu-id="7a05d-116">方法</span><span class="sxs-lookup"><span data-stu-id="7a05d-116">Method</span></span>                                                                                          | <span data-ttu-id="7a05d-117">描述</span><span class="sxs-lookup"><span data-stu-id="7a05d-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="7a05d-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="7a05d-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | <span data-ttu-id="7a05d-119">建立不含任何資料的資料流程優先權物件。</span><span class="sxs-lookup"><span data-stu-id="7a05d-119">Creates a stream prioritization object without any data.</span></span>                     |
| [<span data-ttu-id="7a05d-120">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="7a05d-120">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | <span data-ttu-id="7a05d-121">建立以設定檔中的資料填入的資料流程優先權物件。</span><span class="sxs-lookup"><span data-stu-id="7a05d-121">Creates a stream prioritization object populated with data from the profile.</span></span> |



 

<span data-ttu-id="7a05d-122">上表中的兩個方法都會設定 **IWMStreamPrioritization** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7a05d-122">Both methods in the preceding table set a pointer to an **IWMStreamPrioritization** interface.</span></span> <span data-ttu-id="7a05d-123">這是資料流程優先權物件唯一支援的介面。</span><span class="sxs-lookup"><span data-stu-id="7a05d-123">This is the only interface supported by the stream prioritization object.</span></span>



| <span data-ttu-id="7a05d-124">介面</span><span class="sxs-lookup"><span data-stu-id="7a05d-124">Interface</span></span>                                                  | <span data-ttu-id="7a05d-125">描述</span><span class="sxs-lookup"><span data-stu-id="7a05d-125">Description</span></span>                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="7a05d-126">**IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="7a05d-126">**IWMStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | <span data-ttu-id="7a05d-127">管理資料流程優先權物件內資料流程的清單。</span><span class="sxs-lookup"><span data-stu-id="7a05d-127">Manages the list of streams within the stream prioritization object.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7a05d-128">備註</span><span class="sxs-lookup"><span data-stu-id="7a05d-128">Remarks</span></span>

<span data-ttu-id="7a05d-129">指定的設定檔只可有一個資料流程優先順序。</span><span class="sxs-lookup"><span data-stu-id="7a05d-129">Only one stream prioritization can exist for a given profile.</span></span> <span data-ttu-id="7a05d-130">如果您為已包含資料流程優先權的設定檔建立新的資料流程優先順序，則會刪除舊的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7a05d-130">If you create a new stream prioritization for a profile that already contains a stream prioritization, the old one will be deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a05d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a05d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a05d-132">**物件**</span><span class="sxs-lookup"><span data-stu-id="7a05d-132">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="7a05d-133">**設定檔物件**</span><span class="sxs-lookup"><span data-stu-id="7a05d-133">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="7a05d-134">**使用資料流程優先順序**</span><span class="sxs-lookup"><span data-stu-id="7a05d-134">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 





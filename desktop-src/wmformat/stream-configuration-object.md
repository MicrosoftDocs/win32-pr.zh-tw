---
title: 串流設定物件
description: 串流設定物件
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media 格式 SDK、串流設定物件
- Advanced Systems Format (ASF) ，stream configuration 物件
- ASF (Advanced Systems Format) ，stream configuration objects
- 物件，資料流程設定物件
- 串流設定物件
- 串流，串流設定物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092585"
---
# <a name="stream-configuration-object"></a><span data-ttu-id="c2b55-109">串流設定物件</span><span class="sxs-lookup"><span data-stu-id="c2b55-109">Stream Configuration Object</span></span>

<span data-ttu-id="c2b55-110">資料流程設定物件是用來在 ASF 檔案中指定媒體資料流程的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2b55-110">A stream configuration object is used to specify the properties of a media stream in an ASF file.</span></span> <span data-ttu-id="c2b55-111">您可以為設定檔中的現有資料流程建立串流設定物件，也可以建立空的串流設定物件，準備好接收新的資料。</span><span class="sxs-lookup"><span data-stu-id="c2b55-111">Stream configuration objects can be created for existing streams in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="c2b55-112">資料流程設定物件不能獨立存在於設定檔物件中。</span><span class="sxs-lookup"><span data-stu-id="c2b55-112">Stream configuration objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="c2b55-113">若要儲存資料流程設定物件的內容，您必須呼叫 [**IWMProfile：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) 來加入新的資料流程或 [**IWMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) ，以儲存對現有資料流程所做的變更。</span><span class="sxs-lookup"><span data-stu-id="c2b55-113">To save the contents of a stream configuration object, you must call either [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add a new stream or [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to save changes made to an existing stream.</span></span>

<span data-ttu-id="c2b55-114">若要建立串流設定物件，請使用下列其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="c2b55-114">To create a stream configuration object, use one of the following methods.</span></span>



| <span data-ttu-id="c2b55-115">方法</span><span class="sxs-lookup"><span data-stu-id="c2b55-115">Method</span></span>                                                                | <span data-ttu-id="c2b55-116">描述</span><span class="sxs-lookup"><span data-stu-id="c2b55-116">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2b55-117">**IWMProfile::CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="c2b55-117">**IWMProfile::CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | <span data-ttu-id="c2b55-118">建立不含任何資料的資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="c2b55-118">Creates a stream configuration object without any data.</span></span>                                                                          |
| [<span data-ttu-id="c2b55-119">**IWMProfile：： GetStream**</span><span class="sxs-lookup"><span data-stu-id="c2b55-119">**IWMProfile::GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | <span data-ttu-id="c2b55-120">建立以設定檔中的資料填入的資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="c2b55-120">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="c2b55-121">使用資料流程索引來識別所需的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c2b55-121">Uses the stream index to identify the desired stream.</span></span>  |
| [<span data-ttu-id="c2b55-122">**IWMProfile::GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="c2b55-122">**IWMProfile::GetStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | <span data-ttu-id="c2b55-123">建立以設定檔中的資料填入的資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="c2b55-123">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="c2b55-124">使用資料流程號碼來識別所需的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c2b55-124">Uses the stream number to identify the desired stream.</span></span> |



 

<span data-ttu-id="c2b55-125">上表中的所有方法都會設定 **IWMStreamConfig** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c2b55-125">All of the methods in the preceding table set a pointer to an **IWMStreamConfig** interface.</span></span> <span data-ttu-id="c2b55-126">您可以藉由呼叫 **QueryInterface** 方法來取得資料流程設定物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="c2b55-126">The other interfaces of the stream configuration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="c2b55-127">Stream configuration 物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="c2b55-127">The following interfaces are supported by the stream configuration object.</span></span>



| <span data-ttu-id="c2b55-128">介面</span><span class="sxs-lookup"><span data-stu-id="c2b55-128">Interface</span></span>                                        | <span data-ttu-id="c2b55-129">描述</span><span class="sxs-lookup"><span data-stu-id="c2b55-129">Description</span></span>                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2b55-130">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="c2b55-130">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="c2b55-131">設定和抓取資料流程的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="c2b55-131">Sets and retrieves the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream.</span></span>                                    |
| [<span data-ttu-id="c2b55-132">**IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="c2b55-132">**IWMPropertyVault**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | <span data-ttu-id="c2b55-133">設定及抓取所有資料流程都不需要的屬性，例如變數位元速率 (VBR) 設定。</span><span class="sxs-lookup"><span data-stu-id="c2b55-133">Sets and retrieves properties that are not required for all streams, like variable bit rate (VBR) settings.</span></span>                  |
| [<span data-ttu-id="c2b55-134">**IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="c2b55-134">**IWMStreamConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | <span data-ttu-id="c2b55-135">設定和抓取資料流程的所有基本資訊。</span><span class="sxs-lookup"><span data-stu-id="c2b55-135">Sets and retrieves all of the basic information about a stream.</span></span>                                                              |
| [<span data-ttu-id="c2b55-136">**IWMStreamConfig2**</span><span class="sxs-lookup"><span data-stu-id="c2b55-136">**IWMStreamConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | <span data-ttu-id="c2b55-137">設定與資料流程相關聯的資料單位延伸模組類型。</span><span class="sxs-lookup"><span data-stu-id="c2b55-137">Configures the types of data unit extensions associated with the stream.</span></span> <span data-ttu-id="c2b55-138">繼承 **IWMStreamConfig** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="c2b55-138">Inherits all of the methods of **IWMStreamConfig**.</span></span> |
| [<span data-ttu-id="c2b55-139">**IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="c2b55-139">**IWMStreamConfig3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | <span data-ttu-id="c2b55-140">設定和捕獲資料流程的語言。</span><span class="sxs-lookup"><span data-stu-id="c2b55-140">Sets and retrieves the language for the stream.</span></span> <span data-ttu-id="c2b55-141">繼承 **IWMStreamConfig** 和 **IWMStreamConfig2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="c2b55-141">Inherits all of the methods of **IWMStreamConfig** and **IWMStreamConfig2**.</span></span> |
| [<span data-ttu-id="c2b55-142">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="c2b55-142">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="c2b55-143">管理影片資料流程的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2b55-143">Manages the properties of a video stream.</span></span> <span data-ttu-id="c2b55-144">這是選擇性的介面，只適用于影片串流。</span><span class="sxs-lookup"><span data-stu-id="c2b55-144">This is an optional interface, and is available only for video streams.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="c2b55-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2b55-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2b55-146">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="c2b55-146">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="c2b55-147">**物件**</span><span class="sxs-lookup"><span data-stu-id="c2b55-147">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="c2b55-148">**設定檔管理員物件**</span><span class="sxs-lookup"><span data-stu-id="c2b55-148">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 





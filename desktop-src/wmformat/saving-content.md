---
title: 儲存內容
description: 儲存內容
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK，儲存內容
- Windows Media Format SDK，快速快取串流
- Advanced Systems Format (ASF) ，儲存內容
- ASF (Advanced Systems Format) ，儲存內容
- Advanced Systems Format (ASF) 、Fast Cache 串流
- ASF (Advanced Systems Format) 、Fast Cache 串流
- 串流，儲存內容
- 快取記憶體串流，儲存內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681553"
---
# <a name="saving-content"></a><span data-ttu-id="930e5-111">儲存內容</span><span class="sxs-lookup"><span data-stu-id="930e5-111">Saving Content</span></span>

<span data-ttu-id="930e5-112">藉由使用此 SDK，應用程式可以在讀取器物件上呼叫 [**IWMReaderAdvanced2：： savefileas 並**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) 方法，將下載或串流處理的內容儲存至使用者的本機電腦。</span><span class="sxs-lookup"><span data-stu-id="930e5-112">By using this SDK, an application can save downloaded or streamed content to the user's local computer, by calling the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) method on the reader object.</span></span> <span data-ttu-id="930e5-113">針對已串流處理的內容，伺服器必須使用快速快取串流，如 [從用戶端啟用快速快取串流](enabling-fast-cache-streaming-from-the-client.md)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="930e5-113">For streamed content, the server must be using Fast Cache streaming, which is described in the section [Enabling Fast Cache Streaming from the Client](enabling-fast-cache-streaming-from-the-client.md).</span></span> <span data-ttu-id="930e5-114">針對串流的內容， **savefileas 並** 方法會建立一個 ASX 檔案，指向包含已儲存內容的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="930e5-114">For streamed content, the **SaveFileAs** method creates an ASX file that points to an ASF file containing the saved content.</span></span> <span data-ttu-id="930e5-115">如果讀取器物件正在串流處理伺服器端播放清單，則每個專案都會儲存為個別的 ASF 檔案，而 ASX 檔案會指向每個 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="930e5-115">If the reader object is streaming a server-side playlist, each entry is saved as a separate ASF file, and the ASX file points to each of the ASF files.</span></span> <span data-ttu-id="930e5-116">針對下載的內容， **savefileas 並** 方法只會建立一個 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="930e5-116">For downloaded content, the **SaveFileAs** method simply creates an ASF file.</span></span>

<span data-ttu-id="930e5-117">若要將內容儲存到本機檔案，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="930e5-117">To save content to a local file, do the following:</span></span>

1.  <span data-ttu-id="930e5-118">使用 URL 呼叫 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 。</span><span class="sxs-lookup"><span data-stu-id="930e5-118">Call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) with the URL.</span></span> <span data-ttu-id="930e5-119">**Open** 是非同步呼叫，並會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="930e5-119">**Open** is an asynchronous call, and returns immediately.</span></span> <span data-ttu-id="930e5-120">等候作業完成，如中所述， [建立讀取器並開啟](to-create-a-reader-and-open-a-file.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="930e5-120">Wait for the operation to complete, as described in [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md).</span></span>
2.  <span data-ttu-id="930e5-121">查詢 [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) 介面的 reader 物件。</span><span class="sxs-lookup"><span data-stu-id="930e5-121">Query the reader object for the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface.</span></span>
3.  <span data-ttu-id="930e5-122">藉由呼叫 [**IWMReaderAdvanced4：： CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) 方法來檢查內容是否可以儲存。</span><span class="sxs-lookup"><span data-stu-id="930e5-122">Check whether the content can be saved by calling the [**IWMReaderAdvanced4::CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) method.</span></span> <span data-ttu-id="930e5-123">如果此方法傳回 False，則無法在本機儲存內容。</span><span class="sxs-lookup"><span data-stu-id="930e5-123">If the method returns False, the content cannot be saved locally.</span></span> <span data-ttu-id="930e5-124">否則，請繼續進行步驟4。</span><span class="sxs-lookup"><span data-stu-id="930e5-124">Otherwise, proceed to step 4.</span></span>
4.  <span data-ttu-id="930e5-125">呼叫 [**IWMReaderAdvanced4：： IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) 方法，以判斷伺服器是否使用快速快取串流。</span><span class="sxs-lookup"><span data-stu-id="930e5-125">Call the [**IWMReaderAdvanced4::IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) method to determine whether the server is using Fast Cache streaming.</span></span>
5.  <span data-ttu-id="930e5-126">使用本機檔案的檔案名來呼叫 [**IWMReaderAdvanced2：： savefileas 並**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) 。</span><span class="sxs-lookup"><span data-stu-id="930e5-126">Call the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) with a file name for the local file.</span></span> <span data-ttu-id="930e5-127">如果 **IsUsingFastCache** 方法傳回 True，請提供檔案名為 .asx 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="930e5-127">If the **IsUsingFastCache** method returned True, give the file name an .asx extension.</span></span> <span data-ttu-id="930e5-128">否則，請將檔案名命名為 .asf、.wma 或 .wmv 副檔名。</span><span class="sxs-lookup"><span data-stu-id="930e5-128">Otherwise, give the file name an .asf, .wma, or .wmv extension.</span></span>

<span data-ttu-id="930e5-129">應用程式可以藉由呼叫 [**IWMReaderAdvanced4：： CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) 方法，在進行中時取消儲存作業。</span><span class="sxs-lookup"><span data-stu-id="930e5-129">The application can cancel the save operation while it is in progress, by calling the [**IWMReaderAdvanced4::CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) method.</span></span>

<span data-ttu-id="930e5-130">儲存的內容可能會受到 DRM 保護，因此可能無法在另一部電腦上播放該檔案。</span><span class="sxs-lookup"><span data-stu-id="930e5-130">The saved content might be protected with DRM, so it may not be possible to play the file on another computer.</span></span> <span data-ttu-id="930e5-131">如需有關內容保護的詳細資訊，請參閱 [數位 Rights Management 功能](digital-rights-management-features.md)。</span><span class="sxs-lookup"><span data-stu-id="930e5-131">For more information on content protection, see [Digital Rights Management Features](digital-rights-management-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="930e5-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="930e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="930e5-133">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="930e5-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="930e5-134">**IWMReaderAdvanced2 介面**</span><span class="sxs-lookup"><span data-stu-id="930e5-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 





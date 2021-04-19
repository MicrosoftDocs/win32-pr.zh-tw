---
title: 燒錄包含安全檔案的播放清單
description: 燒錄包含安全檔案的播放清單
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK，以安全檔案燒錄播放清單
- Windows Media Format SDK，包含安全檔案的播放清單
- Advanced Systems Format (ASF) ，以安全檔案燒錄播放清單
- ASF (Advanced Systems Format) ，以安全檔案燒錄播放清單
- Advanced Systems Format (ASF) 、具有安全檔案的播放清單
- ASF (Advanced Systems Format) ，包含安全檔案的播放清單
- 數位版權管理 (DRM) ，以安全檔案燒錄播放清單
- DRM (數位版權管理) ，以安全檔案燒錄播放清單
- 數位版權管理 (DRM) ，包含安全檔案的播放清單
- DRM (數位版權管理) ，包含安全檔案的播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106968085"
---
# <a name="burning-playlists-that-contain-secure-files"></a><span data-ttu-id="e21c0-113">燒錄包含安全檔案的播放清單</span><span class="sxs-lookup"><span data-stu-id="e21c0-113">Burning Playlists That Contain Secure Files</span></span>

<span data-ttu-id="e21c0-114">使用 Windows Media Rights Manager 10 SDK 的物件建立的授權可以指定將檔案複製到光碟作為播放清單一部分的許可權。</span><span class="sxs-lookup"><span data-stu-id="e21c0-114">Licenses created by using the objects of the Windows Media Rights Manager 10 SDK can specify the right to copy a file to compact disc as part of a playlist.</span></span> <span data-ttu-id="e21c0-115">這項功能稱為播放清單燒錄，需要您先確認播放清單中所有檔案的授權，再開始複製資料。</span><span class="sxs-lookup"><span data-stu-id="e21c0-115">This feature, called playlist burning, requires that you verify the licenses of all of the files in the playlist before starting to copy data.</span></span> <span data-ttu-id="e21c0-116">Windows Media Format SDK 提供 [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) 介面，可為您執行檔案驗證。</span><span class="sxs-lookup"><span data-stu-id="e21c0-116">The Windows Media Format SDK provides the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface to perform file verification for you.</span></span>

<span data-ttu-id="e21c0-117">若要執行播放清單燒錄，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="e21c0-117">To implement playlist burning, perform the following steps:</span></span>

1.  <span data-ttu-id="e21c0-118">建立 reader 物件的實例，或同步讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="e21c0-118">Create an instance of the reader object, or the synchronous reader object.</span></span> <span data-ttu-id="e21c0-119">如需詳細資訊，請參閱 [讀取 ASF](reading-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="e21c0-119">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="e21c0-120">呼叫讀取器介面的 **QueryInterface** 方法 ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) 或 [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) ，以取得 [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e21c0-120">Call the **QueryInterface** method of the reader interface ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) or [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) to obtain a pointer to the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface.</span></span>
3.  <span data-ttu-id="e21c0-121">將檔案名從播放清單複製到寬字元字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="e21c0-121">Copy the file names from the playlist into an array of wide-character strings.</span></span> <span data-ttu-id="e21c0-122">陣列中的檔案名必須與播放清單中出現的順序相同。</span><span class="sxs-lookup"><span data-stu-id="e21c0-122">The file names in the array must be in the same order as they appear in the playlist.</span></span>
4.  <span data-ttu-id="e21c0-123">呼叫 [**IWMReaderPlaylistBurn：： InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) 方法，將指標傳入步驟3所建立的陣列，以初始化檔案的授權驗證。</span><span class="sxs-lookup"><span data-stu-id="e21c0-123">Call the [**IWMReaderPlaylistBurn::InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) method, passing in a pointer to the array created in step 3, to initialize the license verification for the files.</span></span>
5.  <span data-ttu-id="e21c0-124">當授權驗證完成時，讀取器物件會將 WMT \_ INIT \_ 播放清單 \_ 燒錄訊息傳送至您的 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法的執行。</span><span class="sxs-lookup"><span data-stu-id="e21c0-124">When the license verification is completed, the reader object sends a WMT\_INIT\_PLAYLIST\_BURN message to your implementation of the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="e21c0-125">當您的回呼收到此訊息時，請呼叫 [**IWMReaderPlaylistBurn：： GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) 方法以取得授權檢查的結果。</span><span class="sxs-lookup"><span data-stu-id="e21c0-125">When your callback receives this message, call the [**IWMReaderPlaylistBurn::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) method to get the results of the license check.</span></span> <span data-ttu-id="e21c0-126">這個方法會採用 **HRESULT** 變數陣列，這些變數會對應至傳遞給 **InitPlaylistBurn** 的陣列中的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e21c0-126">This method takes an array of **HRESULT** variables that correspond to the file names in the array passed to **InitPlaylistBurn**.</span></span> <span data-ttu-id="e21c0-127">如果結果陣列中的所有值都等於 S \_ ，您可以繼續。</span><span class="sxs-lookup"><span data-stu-id="e21c0-127">If all of the values in the result array are equal to S\_OK, you can continue.</span></span> <span data-ttu-id="e21c0-128">如果有任何結果是錯誤碼，則不能複製播放清單。</span><span class="sxs-lookup"><span data-stu-id="e21c0-128">If any result is an error code, the playlist must not be copied.</span></span>
6.  <span data-ttu-id="e21c0-129">使用相同的讀取器實例，開啟並讀取每個檔案。</span><span class="sxs-lookup"><span data-stu-id="e21c0-129">Using the same instance of the reader, open and read each file.</span></span> <span data-ttu-id="e21c0-130">您必須依檔案名在傳遞至 **InitPlaylistBurn** 的檔案名陣列中出現的順序開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="e21c0-130">You must open the files in the order in which the file names appeared in the file name array passed to **InitPlaylistBurn**.</span></span>
7.  <span data-ttu-id="e21c0-131">當您複製播放清單中的所有檔案時，請呼叫 [**IWMReaderPlaylistBurn：： EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) 完成播放清單燒錄程式，並釋放讀取器所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="e21c0-131">When you have copied all of the files in the playlist, call the [**IWMReaderPlaylistBurn::EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) to complete the playlist burn process and free the resources used by the reader.</span></span>

> [!Note]  
> <span data-ttu-id="e21c0-132">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="e21c0-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e21c0-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="e21c0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e21c0-134">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="e21c0-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 





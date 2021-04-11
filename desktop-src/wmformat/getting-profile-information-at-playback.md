---
title: 在播放時取得設定檔資訊
description: 在播放時取得設定檔資訊
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK，設定檔
- Advanced Systems Format (ASF) ，設定檔
- ASF (Advanced Systems Format) ，設定檔
- Advanced Systems Format (ASF) ，相互排除
- ASF (Advanced Systems Format) ，相互排除
- Advanced Systems Format (ASF) 、頻寬共用
- ASF (Advanced 系統格式) 、頻寬共用
- 串流，在播放時取得設定檔資訊
- 設定檔，在播放時取得資訊
- 相互排除，在播放時取得設定檔資訊
- 頻寬共用，在播放時取得設定檔資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092550"
---
# <a name="getting-profile-information-at-playback"></a><span data-ttu-id="3e87d-114">在播放時取得設定檔資訊</span><span class="sxs-lookup"><span data-stu-id="3e87d-114">Getting Profile Information at Playback</span></span>

<span data-ttu-id="3e87d-115">用來建立檔案之設定檔中的資訊會儲存在檔案的標頭區段中。</span><span class="sxs-lookup"><span data-stu-id="3e87d-115">Information from the profile used to create a file is stored in the header section of the file.</span></span> <span data-ttu-id="3e87d-116">這兩個讀取器物件都可以從檔案標頭存取設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="3e87d-116">Both reader objects can access the profile information from the file header.</span></span> <span data-ttu-id="3e87d-117">有幾個原因可能會讓您想要從讀取器存取設定檔資料。</span><span class="sxs-lookup"><span data-stu-id="3e87d-117">There are several reasons why you might want to access profile data from the reader.</span></span> <span data-ttu-id="3e87d-118">最常見的情況是，您需要捕獲資料流程、互斥物件和頻寬共用物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e87d-118">Most commonly, you will need to retrieve information about streams, mutual exclusion objects, and bandwidth sharing objects.</span></span>

<span data-ttu-id="3e87d-119">您可以針對 [**IWMProfile**](iwmprofile.md) 介面查詢非同步讀取器物件和同步讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="3e87d-119">Both the asynchronous reader object and the synchronous reader object can be queried for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="3e87d-120">對設定檔資訊進行的任何變更，對讀取器中的檔案都不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="3e87d-120">No changes made to the profile information can have any affect on the file in the reader.</span></span> <span data-ttu-id="3e87d-121">如需存取設定檔資訊的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="3e87d-121">For more information about accessing profile information, see [Working with Profiles](working-with-profiles.md).</span></span>

## <a name="stream-information"></a><span data-ttu-id="3e87d-122">串流資訊</span><span class="sxs-lookup"><span data-stu-id="3e87d-122">Stream Information</span></span>

<span data-ttu-id="3e87d-123">有時候必須知道串流的設定方式。</span><span class="sxs-lookup"><span data-stu-id="3e87d-123">It is sometimes important to know how a stream is configured.</span></span> <span data-ttu-id="3e87d-124">當您從讀取器物件的任一個取得媒體屬性時，您會取得輸出的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e87d-124">When you retrieve media properties from the either of the reader objects, you get the properties of the outputs.</span></span> <span data-ttu-id="3e87d-125">輸出屬性會描述讀取器如何傳遞來自資料流程的未壓縮資料，而不是在 ASF 檔案內設定資料流程的方式。</span><span class="sxs-lookup"><span data-stu-id="3e87d-125">Output properties describe how the uncompressed data from a stream is going to be delivered by the reader, not how the stream is configured within the ASF file.</span></span>

<span data-ttu-id="3e87d-126">從任一個 reader 物件接收未壓縮的資料流程範例時，您必須使用設定檔資訊來識別壓縮資料的格式。</span><span class="sxs-lookup"><span data-stu-id="3e87d-126">When receiving uncompressed stream samples from either reader object, you must use the profile information to identify the format of the compressed data.</span></span> <span data-ttu-id="3e87d-127">如果您要將壓縮的串流寫入另一個 ASF 檔，這點特別重要。</span><span class="sxs-lookup"><span data-stu-id="3e87d-127">This is particularly important if you are going to write the compressed stream to another ASF file.</span></span>

<span data-ttu-id="3e87d-128">使用智慧型 recompression 將音訊串流轉碼至較低的位元速率時，您也需要存取資料流程資訊。</span><span class="sxs-lookup"><span data-stu-id="3e87d-128">You also need to access stream information when using smart recompression to transcode an audio stream to a lower bit rate.</span></span>

<span data-ttu-id="3e87d-129">您可能會想要判斷資料流程是否使用變數位元速率來撰寫 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="3e87d-129">You may want to determine whether a stream was written using variable bit rate (VBR) encoding.</span></span> <span data-ttu-id="3e87d-130">您無法從任一個 reader 物件的 **IWMProfile** 介面存取任何 VBR 資訊。</span><span class="sxs-lookup"><span data-stu-id="3e87d-130">You cannot access any VBR information from the **IWMProfile** interface of either reader object.</span></span> <span data-ttu-id="3e87d-131">這是因為在編碼之後，不會將 VBR 資訊儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="3e87d-131">This is because the VBR information is not stored in the file after encoding.</span></span> <span data-ttu-id="3e87d-132">您可以藉由取得讀取器物件的 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面指標並呼叫 [**IWMHeaderInfo：： GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)，來判斷資料流程是否使用 VBR 編碼來建立。</span><span class="sxs-lookup"><span data-stu-id="3e87d-132">You can determine whether a stream was created using VBR encoding by obtaining a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface of the reader object and calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span> <span data-ttu-id="3e87d-133">您必須指定串流號碼，並傳遞 g \_ wszIsVBR 做為屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="3e87d-133">You must specify the stream number and pass g\_wszIsVBR as the attribute name.</span></span>

## <a name="mutual-exclusion-information"></a><span data-ttu-id="3e87d-134">相互排除資訊</span><span class="sxs-lookup"><span data-stu-id="3e87d-134">Mutual Exclusion Information</span></span>

<span data-ttu-id="3e87d-135">如果您想要建立使用相互排除的讀取應用程式，您會想要存取設定檔中所包含之任何互斥物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e87d-135">If you want to create a reading application that uses mutual exclusion, you will want to access the information about any mutual exclusion objects included in the profile.</span></span> <span data-ttu-id="3e87d-136">若為所有相互排斥類型（位元速率不同），讀取應用程式會負責任何需要的資料流程切換。</span><span class="sxs-lookup"><span data-stu-id="3e87d-136">For all mutual exclusion types except bit rate, the reading application is responsible for any stream switching that is required.</span></span> <span data-ttu-id="3e87d-137">若要切換資料流程，您需要知道哪些資料流程是哪些。</span><span class="sxs-lookup"><span data-stu-id="3e87d-137">To switch streams, you need to know which streams are which.</span></span>

## <a name="bandwidth-sharing-information"></a><span data-ttu-id="3e87d-138">頻寬共用資訊</span><span class="sxs-lookup"><span data-stu-id="3e87d-138">Bandwidth Sharing Information</span></span>

<span data-ttu-id="3e87d-139">設定檔中包含的頻寬共用物件僅供資訊參考之用。</span><span class="sxs-lookup"><span data-stu-id="3e87d-139">Bandwidth sharing objects that are included in a profile are included only for informational purposes.</span></span> <span data-ttu-id="3e87d-140">寫入器物件或其中一個讀取器物件都不會因為頻寬共用資料而採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="3e87d-140">Neither the writer object nor either of the reader objects takes any action as a result of bandwidth sharing data.</span></span> <span data-ttu-id="3e87d-141">如果您想要在讀取應用程式中使用頻寬共用，您必須從設定檔資料存取頻寬共用資訊。</span><span class="sxs-lookup"><span data-stu-id="3e87d-141">If you want to use bandwidth sharing in your reading application, you must access the bandwidth sharing information from the profile data.</span></span>

> [!Note]  
> <span data-ttu-id="3e87d-142">並非所有用來建立檔案的設定檔資訊都出現在檔案標頭中。</span><span class="sxs-lookup"><span data-stu-id="3e87d-142">Not all of the information from the profile used to create a file is present in the file header.</span></span> <span data-ttu-id="3e87d-143">一般來說，只有在編碼時使用的資料不會保存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="3e87d-143">As a general rule, data that is used only at the time of encoding is not persisted in the file.</span></span> <span data-ttu-id="3e87d-144">這包括使用 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) 方法設定的輸入設定，以及使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e87d-144">This includes input settings that were set using the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method, as well as properties set using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3e87d-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e87d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e87d-146">**IWMProfile 介面**</span><span class="sxs-lookup"><span data-stu-id="3e87d-146">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="3e87d-147">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="3e87d-147">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 





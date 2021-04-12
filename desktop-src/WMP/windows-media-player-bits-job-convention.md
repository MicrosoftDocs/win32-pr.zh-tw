---
title: Windows Media Player BITS 作業慣例
description: 如果您使用背景智慧型傳送服務 (BITS) ，Windows Media Player 可以自動下載數位媒體專案，並將其新增至程式庫。
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- 'Windows Media Player 線上商店，背景智慧型傳送服務 (個位) '
- '線上商店、背景智慧型傳送服務 (位) '
- '輸入2個線上商店，背景智慧型傳送服務 (位) '
- 背景智慧型傳送服務 (BITS)
- 'BITS (背景智慧型傳送服務) '
- Windows Media Player 線上商店，BITS 作業慣例
- 線上商店，BITS 作業慣例
- 類型2線上商店，BITS 作業慣例
- BITS 作業慣例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186067"
---
# <a name="windows-media-player-bits-job-convention"></a><span data-ttu-id="1108b-112">Windows Media Player BITS 作業慣例</span><span class="sxs-lookup"><span data-stu-id="1108b-112">Windows Media Player BITS Job Convention</span></span>

<span data-ttu-id="1108b-113">如果您使用 [背景智慧型傳送服務 (BITS) ](/windows/desktop/Bits/background-intelligent-transfer-service-portal)，Windows Media Player 可以自動下載數位媒體專案，並將其新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="1108b-113">Windows Media Player can automatically download and add digital media items to the library if you use [Background Intelligent Transfer Service (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span></span> <span data-ttu-id="1108b-114">若要利用這項功能，您必須將作業新增至 BITS 傳送佇列，並呼叫 **IBackgroundCopyJob：： SetDescription**，並提供使用正確格式的描述字串。</span><span class="sxs-lookup"><span data-stu-id="1108b-114">To take advantage of this feature, you must add your job to the BITS transfer queue and call **IBackgroundCopyJob::SetDescription**, providing a description string that uses the correct format.</span></span>

> [!Note]  
> <span data-ttu-id="1108b-115">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="1108b-115">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1108b-116">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="1108b-116">Use of this functionality outside the context of an online store is not supported.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1108b-117">語法</span><span class="sxs-lookup"><span data-stu-id="1108b-117">Syntax</span></span>

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a><span data-ttu-id="1108b-118">參數</span><span class="sxs-lookup"><span data-stu-id="1108b-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1108b-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span><span class="sxs-lookup"><span data-stu-id="1108b-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-120">Windows Media Player 用來識別服務的隨機產生32位值。</span><span class="sxs-lookup"><span data-stu-id="1108b-120">A randomly generated 32-bit value that Windows Media Player uses to identify the service.</span></span>

</dd> <dt>

<span data-ttu-id="1108b-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*供應商*</span><span class="sxs-lookup"><span data-stu-id="1108b-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-122">提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="1108b-122">The provider name.</span></span> <span data-ttu-id="1108b-123">此值必須符合有效的線上商店金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="1108b-123">This value must match a valid online store key name.</span></span>

</dd> <dt>

<span data-ttu-id="1108b-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span><span class="sxs-lookup"><span data-stu-id="1108b-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-125">專輯的主要演出者名稱。</span><span class="sxs-lookup"><span data-stu-id="1108b-125">The name of the primary artist for the album.</span></span>

</dd> <dt>

<span data-ttu-id="1108b-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span><span class="sxs-lookup"><span data-stu-id="1108b-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-127">專輯的標題。</span><span class="sxs-lookup"><span data-stu-id="1108b-127">The title of the album.</span></span>

</dd> <dt>

<span data-ttu-id="1108b-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span><span class="sxs-lookup"><span data-stu-id="1108b-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-129">CD 曲目編號。</span><span class="sxs-lookup"><span data-stu-id="1108b-129">The CD track number.</span></span>

</dd> <dt>

<span data-ttu-id="1108b-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*標題*</span><span class="sxs-lookup"><span data-stu-id="1108b-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Title*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-131">內容的標題。</span><span class="sxs-lookup"><span data-stu-id="1108b-131">The title of the content.</span></span>

</dd> <dt>

<span data-ttu-id="1108b-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*時間*</span><span class="sxs-lookup"><span data-stu-id="1108b-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-133">內容的持續時間。</span><span class="sxs-lookup"><span data-stu-id="1108b-133">The duration of the content.</span></span>

</dd> <dt>

<span data-ttu-id="1108b-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*評級*</span><span class="sxs-lookup"><span data-stu-id="1108b-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Rating*</span></span>
</dt> <dd>

<span data-ttu-id="1108b-135">內容的評等。</span><span class="sxs-lookup"><span data-stu-id="1108b-135">The rating for the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1108b-136">備註</span><span class="sxs-lookup"><span data-stu-id="1108b-136">Remarks</span></span>

<span data-ttu-id="1108b-137">當 Windows Media Player 10 或更新版本使用 BITS 來下載內容時，它會列舉傳送佇列中的作業，並檢查每項作業的描述字串。</span><span class="sxs-lookup"><span data-stu-id="1108b-137">When Windows Media Player 10 or later uses BITS to download content, it enumerates the jobs in the transfer queue and inspects the description string for each job.</span></span> <span data-ttu-id="1108b-138">如果描述字串符合預期慣例，Windows Media Player 下載內容。</span><span class="sxs-lookup"><span data-stu-id="1108b-138">If the description string matches the expected convention, Windows Media Player downloads the content.</span></span>

<span data-ttu-id="1108b-139">您只需新增一個數位媒體檔案，即可下載至每個 BITS 作業。</span><span class="sxs-lookup"><span data-stu-id="1108b-139">You must add only one digital media file for download to each BITS job.</span></span>

<span data-ttu-id="1108b-140">使用此慣例啟動 BITS 作業之後，您必須讓 Windows Media Player 完成工作。</span><span class="sxs-lookup"><span data-stu-id="1108b-140">After you start a BITS job using this convention, you must let Windows Media Player complete the job.</span></span> <span data-ttu-id="1108b-141">Windows Media Player 也會從 BITS 佇列中移除工作、將下載的檔案移至儲存已翻錄音樂的位置，然後將下載的檔案新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="1108b-141">Windows Media Player will also remove the job from the BITS queue, move the downloaded file to the location where ripped music is saved, and add the downloaded file to the library.</span></span>

<span data-ttu-id="1108b-142">*ServiceId* 參數必須包含非零的32位值。</span><span class="sxs-lookup"><span data-stu-id="1108b-142">The *serviceId* parameter must contain a nonzero 32-bit value.</span></span> <span data-ttu-id="1108b-143">建議您使用函數 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 來建立這個值。</span><span class="sxs-lookup"><span data-stu-id="1108b-143">We recommend that you use the function [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) to create this value.</span></span>

<span data-ttu-id="1108b-144">您使用 **IBackgroundCopyJob：： AddFile** 的 *localName* 參數指定的檔案名必須具有 .wma、.wmv、mp3 或 .asf 副檔名。</span><span class="sxs-lookup"><span data-stu-id="1108b-144">The file name you specify using the *localName* parameter of **IBackgroundCopyJob::AddFile** must have a .wma, .wmv, .mp3, or .asf file name extension.</span></span>

<span data-ttu-id="1108b-145">其餘的參數是設計來包含與內容相關的中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="1108b-145">The remaining parameters are designed to contain metadata values related to the content.</span></span> <span data-ttu-id="1108b-146">您可以使用 **DownloadItem getItemInfo**，從線上商店網頁取得這些值。</span><span class="sxs-lookup"><span data-stu-id="1108b-146">You can retrieve these values from your online store webpage by using **DownloadItem.getItemInfo**.</span></span> <span data-ttu-id="1108b-147">您可以藉由呼叫 **DownloadManager getDownloadCollection** ，並提供 *serviceId* 作為 *collectionId* 參數，來取得正確的下載集合。</span><span class="sxs-lookup"><span data-stu-id="1108b-147">You can retrieve the correct download collection by calling **DownloadManager.getDownloadCollection** and providing *serviceId* as the *collectionId* parameter.</span></span>

<span data-ttu-id="1108b-148">Windows Media Player 會在播放程式執行時定期檢查 BITS 佇列。</span><span class="sxs-lookup"><span data-stu-id="1108b-148">Windows Media Player inspects the BITS queue periodically while the Player is running.</span></span> <span data-ttu-id="1108b-149">為確保 Windows Media Player 檢查 BITS 佇列中的下載工作，您應該在下列登錄子機碼中建立一個值：</span><span class="sxs-lookup"><span data-stu-id="1108b-149">To ensure that Windows Media Player checks the BITS queue for download jobs, you should create a value in the following registry subkey:</span></span>

<span data-ttu-id="1108b-150">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ 服務**</span><span class="sxs-lookup"><span data-stu-id="1108b-150">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Services**</span></span>

<span data-ttu-id="1108b-151">此值應如下所示建立。</span><span class="sxs-lookup"><span data-stu-id="1108b-151">The value should be created as follows.</span></span>



| <span data-ttu-id="1108b-152">名稱</span><span class="sxs-lookup"><span data-stu-id="1108b-152">Name</span></span>                | <span data-ttu-id="1108b-153">類型</span><span class="sxs-lookup"><span data-stu-id="1108b-153">Type</span></span>      | <span data-ttu-id="1108b-154">Description</span><span class="sxs-lookup"><span data-stu-id="1108b-154">Description</span></span>                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1108b-155">**RefreshDownload**</span><span class="sxs-lookup"><span data-stu-id="1108b-155">**RefreshDownload**</span></span> | <span data-ttu-id="1108b-156">**Dword**</span><span class="sxs-lookup"><span data-stu-id="1108b-156">**DWORD**</span></span> | <span data-ttu-id="1108b-157">指定 Windows Media Player 是否應該檢查 BITS 佇列中的下載作業。</span><span class="sxs-lookup"><span data-stu-id="1108b-157">Specifies whether Windows Media Player should inspect the BITS queue for download jobs.</span></span> <span data-ttu-id="1108b-158">如果值為零，播放程式將不會檢查 BITS 佇列。</span><span class="sxs-lookup"><span data-stu-id="1108b-158">If the value is zero, the Player will not inspect the BITS queue.</span></span> <span data-ttu-id="1108b-159">如果此值為非零值，則播放程式必須檢查佇列。</span><span class="sxs-lookup"><span data-stu-id="1108b-159">The Player must inspect the queue if the value is nonzero.</span></span> |



 

<span data-ttu-id="1108b-160">您可以使用下列替代語法來新增 Windows Media Player 未完成的 BITS 作業，但它只會顯示狀態資訊：</span><span class="sxs-lookup"><span data-stu-id="1108b-160">You can use the following alternate syntax to add BITS jobs that Windows Media Player does not complete, but for which it simply shows status information:</span></span>

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

<span data-ttu-id="1108b-161">使用上述語法時，您必須撰寫程式碼來完成 BITS 下載、在使用者的電腦上組織內容，並視需要將內容新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="1108b-161">When you use the preceding syntax, you must write code to complete the BITS download, organize the content on the user's computer, and add the content to the library, if desired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1108b-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="1108b-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1108b-163">CryptGenRandom</span><span class="sxs-lookup"><span data-stu-id="1108b-163">CryptGenRandom</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[<span data-ttu-id="1108b-164">**DownloadItem. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1108b-164">**DownloadItem.getItemInfo**</span></span>](downloaditem-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1108b-165">**DownloadManager.getDownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="1108b-165">**DownloadManager.getDownloadCollection**</span></span>](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="1108b-166">**類型 2 線上商店的參考**</span><span class="sxs-lookup"><span data-stu-id="1108b-166">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 
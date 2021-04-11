---
title: '新功能 (Windows Media Format 11 SDK) '
description: 新功能
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK，新功能
- Windows Media Format SDK，功能
- Windows Media Format SDK，新功能
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，DRM 更新
- Windows Media Format SDK，編解碼器更新
- Windows Media Format SDK，縮圖影像
- 數位版權管理 (DRM) 、新功能
- DRM (數位版權管理) 、新功能
- 縮圖影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685408"
---
# <a name="whats-new-windows-media-format-11-sdk"></a><span data-ttu-id="47664-113">新功能 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="47664-113">What's New (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="47664-114">Windows Media Format 11 SDK 引進新的數位版權管理 (DRM) 功能。</span><span class="sxs-lookup"><span data-stu-id="47664-114">The Windows Media Format 11 SDK introduces new digital rights management (DRM) features.</span></span> <span data-ttu-id="47664-115">自9.5 版開始，已對 SDK 進行下列變更。</span><span class="sxs-lookup"><span data-stu-id="47664-115">The following changes have been made to the SDK since the 9.5 release.</span></span>

## <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="47664-116">Windows Media DRM 用戶端擴充 Api</span><span class="sxs-lookup"><span data-stu-id="47664-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="47664-117">Windows Media Format 11 SDK 隨附一組新的 DRM Api。</span><span class="sxs-lookup"><span data-stu-id="47664-117">The Windows Media Format 11 SDK ships with a new set of DRM APIs.</span></span> <span data-ttu-id="47664-118">這些 Api 會在自己的程式庫中執行。</span><span class="sxs-lookup"><span data-stu-id="47664-118">These APIs are implemented in their own library.</span></span> <span data-ttu-id="47664-119">Windows Media DRM 用戶端擴充 Api 也支援 Windows Media 格式 SDK 的物件所支援的許多 DRM 功能。</span><span class="sxs-lookup"><span data-stu-id="47664-119">Many of the DRM features supported by the objects of the Windows Media Format SDK are also supported by the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="47664-120">新 Api 的主要差異在於它們不會依賴有 ASF 檔案可運作。</span><span class="sxs-lookup"><span data-stu-id="47664-120">The primary difference in the new APIs is that they do not rely on having an ASF file to work.</span></span> <span data-ttu-id="47664-121">相反地，新的 Api 會直接處理本機授權存放區，通常會使用金鑰識別碼來識別授權。</span><span class="sxs-lookup"><span data-stu-id="47664-121">Instead, the new APIs deal with the local license store directly, often using the key ID to identify licenses.</span></span>

<span data-ttu-id="47664-122">如需詳細資訊，請參閱 [Windows MEDIA DRM 用戶端擴充 api](windows-media-drm-client-extended-apis.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="47664-122">For more information, see the [Windows Media DRM Client Extended APIs](windows-media-drm-client-extended-apis.md) documentation.</span></span>

## <a name="updated-codecs"></a><span data-ttu-id="47664-123">已更新編解碼器</span><span class="sxs-lookup"><span data-stu-id="47664-123">Updated Codecs</span></span>

<span data-ttu-id="47664-124">已更新 Windows Media 視訊 9 Advanced Profile 編解碼器，以產生符合已發行之 SMPTE VC-1 標準的壓縮位資料流程。</span><span class="sxs-lookup"><span data-stu-id="47664-124">The Windows Media Video 9 Advanced Profile codec has been updated to produce a compressed bit stream that is compliant with the published SMPTE VC-1 standard.</span></span>

<span data-ttu-id="47664-125">這一版的 SDK 也包含 Windows Media 音訊 10 Professional 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="47664-125">The Windows Media Audio 10 Professional codec is also included in this release of the SDK.</span></span> <span data-ttu-id="47664-126">新的音訊編解碼器功能以較低的位元速率提高品質。</span><span class="sxs-lookup"><span data-stu-id="47664-126">The new audio codec features improved quality at lower bit rates.</span></span>

## <a name="thumbnail-right"></a><span data-ttu-id="47664-127">縮圖右邊</span><span class="sxs-lookup"><span data-stu-id="47664-127">Thumbnail Right</span></span>

<span data-ttu-id="47664-128">應用程式可以要求新的 DRM 動作以從影片讀取，以建立縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="47664-128">Applications can request a new DRM action to read from video to create a thumbnail image.</span></span> <span data-ttu-id="47664-129">這可讓應用程式建立及顯示影片檔案的縮圖影像，而不需要開啟檔案以供播放。</span><span class="sxs-lookup"><span data-stu-id="47664-129">This enables applications to create and display thumbnail images for video files without opening the file for playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47664-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="47664-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47664-131">**關於 Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="47664-131">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 





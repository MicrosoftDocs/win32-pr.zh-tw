---
title: 音樂檔案的屬性
description: 音樂檔案的屬性
ms.assetid: 098d9241-c8b0-4b0c-b9c1-668497f91e8c
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性、音訊檔
- 屬性、音樂檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5956296da5ef43ed3a8d35ecc2d7e6d0a4c97e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672044"
---
# <a name="attributes-for-music-files"></a><span data-ttu-id="e2d63-108">音樂檔案的屬性</span><span class="sxs-lookup"><span data-stu-id="e2d63-108">Attributes for Music Files</span></span>

<span data-ttu-id="e2d63-109">本節列出常用於包含音樂之音訊檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2d63-109">This section lists the attributes commonly used for audio files containing music.</span></span> <span data-ttu-id="e2d63-110">建議您根據這些清單設定檔案的屬性，以確保您的檔案與各種不同的播放應用程式完全相容。</span><span class="sxs-lookup"><span data-stu-id="e2d63-110">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="e2d63-111">此區段中的屬性會以三種類別列出：主要、次要和第三個類別。</span><span class="sxs-lookup"><span data-stu-id="e2d63-111">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="e2d63-112">主要屬性會傳達最基本的檔案相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e2d63-112">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="e2d63-113">如果您要建立用於散發的音訊檔案，這是您應該使用的最小屬性集。</span><span class="sxs-lookup"><span data-stu-id="e2d63-113">If you are creating audio files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="e2d63-114">次要屬性包含對所有音訊檔案而言很重要，但不是通用的通用中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e2d63-114">Secondary attributes contain common metadata that is important but not universal to all audio files.</span></span>

<span data-ttu-id="e2d63-115">第三個屬性應該包含在必要的情況下，但不是描述檔案的必要條件。</span><span class="sxs-lookup"><span data-stu-id="e2d63-115">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-music"></a><span data-ttu-id="e2d63-116">音樂的主要屬性</span><span class="sxs-lookup"><span data-stu-id="e2d63-116">Primary Attributes for Music</span></span>

-   [<span data-ttu-id="e2d63-117">**作者**</span><span class="sxs-lookup"><span data-stu-id="e2d63-117">**Author**</span></span>](author.md)
-   [<span data-ttu-id="e2d63-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="e2d63-118">**Title**</span></span>](title.md)
-   [<span data-ttu-id="e2d63-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="e2d63-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)
-   [<span data-ttu-id="e2d63-120">**WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="e2d63-120">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   [<span data-ttu-id="e2d63-121">**WM/內容類型**</span><span class="sxs-lookup"><span data-stu-id="e2d63-121">**WM/Genre**</span></span>](wm-genre.md)
-   <span data-ttu-id="e2d63-122">如果有 (，則為 [**WM/MCDI**](wm-mcdi.md)否則，請使用 [**wm/WMCollectionID**](wm-wmcollectionid.md)、 [**wm/WMCollectionGroupID**](wm-wmcollectiongroupid.md)或 [**wm/WMContentID**](wm-wmcontentid.md)) </span><span class="sxs-lookup"><span data-stu-id="e2d63-122">[**WM/MCDI**](wm-mcdi.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), or [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="e2d63-123">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="e2d63-123">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="e2d63-124">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="e2d63-124">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="e2d63-125">**WM/提供者**</span><span class="sxs-lookup"><span data-stu-id="e2d63-125">**WM/Provider**</span></span>](wm-provider.md)
-   [<span data-ttu-id="e2d63-126">**WM/TrackNumber**</span><span class="sxs-lookup"><span data-stu-id="e2d63-126">**WM/TrackNumber**</span></span>](wm-tracknumber.md)

## <a name="secondary-attributes-for-music"></a><span data-ttu-id="e2d63-127">音樂的次要屬性</span><span class="sxs-lookup"><span data-stu-id="e2d63-127">Secondary Attributes for Music</span></span>

-   [<span data-ttu-id="e2d63-128">**著作權**</span><span class="sxs-lookup"><span data-stu-id="e2d63-128">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="e2d63-129">**WM/編輯器**</span><span class="sxs-lookup"><span data-stu-id="e2d63-129">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="e2d63-130">**WM/EncodingTime**</span><span class="sxs-lookup"><span data-stu-id="e2d63-130">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="e2d63-131">**WM/語言**</span><span class="sxs-lookup"><span data-stu-id="e2d63-131">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="e2d63-132">**WM/ParentalRating**</span><span class="sxs-lookup"><span data-stu-id="e2d63-132">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="e2d63-133">**WM/生產者**</span><span class="sxs-lookup"><span data-stu-id="e2d63-133">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="e2d63-134">**WM/工具**</span><span class="sxs-lookup"><span data-stu-id="e2d63-134">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="e2d63-135">**WM/ToolVersion**</span><span class="sxs-lookup"><span data-stu-id="e2d63-135">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="e2d63-136">**WM/WMCollectionGroupID**</span><span class="sxs-lookup"><span data-stu-id="e2d63-136">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="e2d63-137">**WM/WMCollectionID**</span><span class="sxs-lookup"><span data-stu-id="e2d63-137">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="e2d63-138">**WM/WMContentID**</span><span class="sxs-lookup"><span data-stu-id="e2d63-138">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="e2d63-139">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="e2d63-139">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-music"></a><span data-ttu-id="e2d63-140">音樂的第三個屬性</span><span class="sxs-lookup"><span data-stu-id="e2d63-140">Tertiary Attributes for Music</span></span>

-   [<span data-ttu-id="e2d63-141">**描述**</span><span class="sxs-lookup"><span data-stu-id="e2d63-141">**Description**</span></span>](description.md)
-   [<span data-ttu-id="e2d63-142">**WM/AuthorURL**</span><span class="sxs-lookup"><span data-stu-id="e2d63-142">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="e2d63-143">**WM/BeatsPerMinute**</span><span class="sxs-lookup"><span data-stu-id="e2d63-143">**WM/BeatsPerMinute**</span></span>](wm-beatsperminute.md)
-   [<span data-ttu-id="e2d63-144">**WM/導體**</span><span class="sxs-lookup"><span data-stu-id="e2d63-144">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="e2d63-145">**WM/ContentGroupDescription**</span><span class="sxs-lookup"><span data-stu-id="e2d63-145">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="e2d63-146">**WM/EncodedBy**</span><span class="sxs-lookup"><span data-stu-id="e2d63-146">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="e2d63-147">**WM/EncodingSettings**</span><span class="sxs-lookup"><span data-stu-id="e2d63-147">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="e2d63-148">**WM/InitialKey**</span><span class="sxs-lookup"><span data-stu-id="e2d63-148">**WM/InitialKey**</span></span>](wm-initialkey.md)
-   [<span data-ttu-id="e2d63-149">**WM/歌詞**</span><span class="sxs-lookup"><span data-stu-id="e2d63-149">**WM/Lyrics**</span></span>](wm-lyrics.md)
-   [<span data-ttu-id="e2d63-150">**WM/歌詞 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="e2d63-150">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md)
-   [<span data-ttu-id="e2d63-151">**WM/情緒**</span><span class="sxs-lookup"><span data-stu-id="e2d63-151">**WM/Mood**</span></span>](wm-mood.md)
-   [<span data-ttu-id="e2d63-152">**WM/PartOfSet**</span><span class="sxs-lookup"><span data-stu-id="e2d63-152">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="e2d63-153">**WM/句號**</span><span class="sxs-lookup"><span data-stu-id="e2d63-153">**WM/Period**</span></span>](wm-period.md)
-   [<span data-ttu-id="e2d63-154">**WM/圖片**</span><span class="sxs-lookup"><span data-stu-id="e2d63-154">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="e2d63-155">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="e2d63-155">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="e2d63-156">**WM/發行者**</span><span class="sxs-lookup"><span data-stu-id="e2d63-156">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="e2d63-157">**WM/子標題**</span><span class="sxs-lookup"><span data-stu-id="e2d63-157">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="e2d63-158">**WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="e2d63-158">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="e2d63-159">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="e2d63-159">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="e2d63-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2d63-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2d63-161">**依類型的屬性**</span><span class="sxs-lookup"><span data-stu-id="e2d63-161">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="e2d63-162">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="e2d63-162">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





---
title: 影片檔案的屬性
description: 影片檔案的屬性
ms.assetid: 4250ad27-075e-4daa-bc04-d24ddd2e8252
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性、影片檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd19791857d55be8017d291698a3297b395af550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371973"
---
# <a name="attributes-for-video-files"></a><span data-ttu-id="047cd-107">影片檔案的屬性</span><span class="sxs-lookup"><span data-stu-id="047cd-107">Attributes for Video Files</span></span>

<span data-ttu-id="047cd-108">此區段會列出常用於影片檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="047cd-108">This section lists the attributes commonly used for video files.</span></span> <span data-ttu-id="047cd-109">建議您根據這些清單設定檔案的屬性，以確保您的檔案與各種不同的播放應用程式完全相容。</span><span class="sxs-lookup"><span data-stu-id="047cd-109">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="047cd-110">此區段中的屬性會以三種類別列出：主要、次要和第三個類別。</span><span class="sxs-lookup"><span data-stu-id="047cd-110">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="047cd-111">主要屬性會傳達最基本的檔案相關資訊。</span><span class="sxs-lookup"><span data-stu-id="047cd-111">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="047cd-112">如果您要建立用於散發的影片檔案，這是您應該使用的最小屬性集。</span><span class="sxs-lookup"><span data-stu-id="047cd-112">If you are creating video files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="047cd-113">次要屬性包含對所有影片檔案而言很重要，但不是通用的通用中繼資料。</span><span class="sxs-lookup"><span data-stu-id="047cd-113">Secondary attributes contain common metadata that is important but not universal to all video files.</span></span>

<span data-ttu-id="047cd-114">第三個屬性應該包含在必要的情況下，但不是描述檔案的必要條件。</span><span class="sxs-lookup"><span data-stu-id="047cd-114">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-video"></a><span data-ttu-id="047cd-115">影片的主要屬性</span><span class="sxs-lookup"><span data-stu-id="047cd-115">Primary Attributes for Video</span></span>

-   [<span data-ttu-id="047cd-116">**作者**</span><span class="sxs-lookup"><span data-stu-id="047cd-116">**Author**</span></span>](author.md)
-   [<span data-ttu-id="047cd-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="047cd-117">**Title**</span></span>](title.md)
-   [<span data-ttu-id="047cd-118">**WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="047cd-118">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   <span data-ttu-id="047cd-119">如果有 (，則為 [**WM/DVDID**](wm-dvdid.md)否則，請使用 [**wm/WMCollectionID**](wm-wmcollectionid.md)、 [**wm/WMCollectionGroupID**](wm-wmcollectiongroupid.md)和 [**wm/WMContentID**](wm-wmcontentid.md)) </span><span class="sxs-lookup"><span data-stu-id="047cd-119">[**WM/DVDID**](wm-dvdid.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), and [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="047cd-120">**WM/內容類型**</span><span class="sxs-lookup"><span data-stu-id="047cd-120">**WM/Genre**</span></span>](wm-genre.md)
-   [<span data-ttu-id="047cd-121">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="047cd-121">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="047cd-122">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="047cd-122">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="047cd-123">**WM/提供者**</span><span class="sxs-lookup"><span data-stu-id="047cd-123">**WM/Provider**</span></span>](wm-provider.md)

## <a name="secondary-attributes-for-video"></a><span data-ttu-id="047cd-124">影片的次要屬性</span><span class="sxs-lookup"><span data-stu-id="047cd-124">Secondary Attributes for Video</span></span>

-   [<span data-ttu-id="047cd-125">**著作權**</span><span class="sxs-lookup"><span data-stu-id="047cd-125">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="047cd-126">**WM/編輯器**</span><span class="sxs-lookup"><span data-stu-id="047cd-126">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="047cd-127">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="047cd-127">**WM/Director**</span></span>](wm-director.md)
-   [<span data-ttu-id="047cd-128">**WM/EncodingTime**</span><span class="sxs-lookup"><span data-stu-id="047cd-128">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="047cd-129">**WM/語言**</span><span class="sxs-lookup"><span data-stu-id="047cd-129">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="047cd-130">**WM/ParentalRating**</span><span class="sxs-lookup"><span data-stu-id="047cd-130">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="047cd-131">**WM/生產者**</span><span class="sxs-lookup"><span data-stu-id="047cd-131">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="047cd-132">**WM/工具**</span><span class="sxs-lookup"><span data-stu-id="047cd-132">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="047cd-133">**WM/ToolVersion**</span><span class="sxs-lookup"><span data-stu-id="047cd-133">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="047cd-134">**WM/WMCollectionGroupID**</span><span class="sxs-lookup"><span data-stu-id="047cd-134">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="047cd-135">**WM/WMCollectionID**</span><span class="sxs-lookup"><span data-stu-id="047cd-135">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="047cd-136">**WM/WMContentID**</span><span class="sxs-lookup"><span data-stu-id="047cd-136">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="047cd-137">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="047cd-137">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-video"></a><span data-ttu-id="047cd-138">影片的第三個屬性</span><span class="sxs-lookup"><span data-stu-id="047cd-138">Tertiary Attributes for Video</span></span>

-   [<span data-ttu-id="047cd-139">**描述**</span><span class="sxs-lookup"><span data-stu-id="047cd-139">**Description**</span></span>](description.md)
-   [<span data-ttu-id="047cd-140">**WM/AuthorURL**</span><span class="sxs-lookup"><span data-stu-id="047cd-140">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="047cd-141">**WM/導體**</span><span class="sxs-lookup"><span data-stu-id="047cd-141">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="047cd-142">**WM/ContentGroupDescription**</span><span class="sxs-lookup"><span data-stu-id="047cd-142">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="047cd-143">**WM/EncodedBy**</span><span class="sxs-lookup"><span data-stu-id="047cd-143">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="047cd-144">**WM/EncodingSettings**</span><span class="sxs-lookup"><span data-stu-id="047cd-144">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="047cd-145">**WM/PartOfSet**</span><span class="sxs-lookup"><span data-stu-id="047cd-145">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="047cd-146">**WM/圖片**</span><span class="sxs-lookup"><span data-stu-id="047cd-146">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="047cd-147">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="047cd-147">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="047cd-148">**WM/發行者**</span><span class="sxs-lookup"><span data-stu-id="047cd-148">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="047cd-149">**WM/子標題**</span><span class="sxs-lookup"><span data-stu-id="047cd-149">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="047cd-150">**WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="047cd-150">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="047cd-151">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="047cd-151">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="047cd-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="047cd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="047cd-153">**依類型的屬性**</span><span class="sxs-lookup"><span data-stu-id="047cd-153">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="047cd-154">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="047cd-154">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





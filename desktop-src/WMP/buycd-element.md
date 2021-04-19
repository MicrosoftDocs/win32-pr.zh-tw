---
title: BuyCD 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |BuyCD 元素
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- BuyCD 元素 Windows Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994681"
---
# <a name="buycd-element"></a><span data-ttu-id="79235-105">BuyCD 元素</span><span class="sxs-lookup"><span data-stu-id="79235-105">BuyCD Element</span></span>

> [!Note]  
> <span data-ttu-id="79235-106">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="79235-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="79235-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="79235-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="79235-108">**BuyCD** 元素會指定當使用者選擇進行購買時，Windows Media Player 顯示的網頁 url。</span><span class="sxs-lookup"><span data-stu-id="79235-108">The **BuyCD** element specifies the URLs for webpages that Windows Media Player displays when the user chooses to make a purchase.</span></span>

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="79235-109">屬性</span><span class="sxs-lookup"><span data-stu-id="79235-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="79235-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (必要) </span><span class="sxs-lookup"><span data-stu-id="79235-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="79235-111">線上商店所顯示的網頁 URL，以提供 CD 或 DVD 供 Windows Media Player 購買。</span><span class="sxs-lookup"><span data-stu-id="79235-111">URL for the webpage that the online store displays to offer a CD or DVD for purchase in Windows Media Player.</span></span>

</dd> <dt>

<span data-ttu-id="79235-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span><span class="sxs-lookup"><span data-stu-id="79235-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span></span>
</dt> <dd>

<span data-ttu-id="79235-113">線上商店顯示的網頁 URL，可提供在 Windows XP Media Center Edition 2004 更新中購買的 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="79235-113">URL for the webpage the online store displays to offer a CD or DVD for purchase in Windows XP Media Center Edition 2004 Update.</span></span>

</dd> <dt>

<span data-ttu-id="79235-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span><span class="sxs-lookup"><span data-stu-id="79235-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span></span>
</dt> <dd>

<span data-ttu-id="79235-115">線上商店顯示的網頁 URL，可在另一個瀏覽器視窗中提供要購買的 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="79235-115">URL for the webpage that the online store displays to offer a CD or DVD for purchase in a separate browser window.</span></span> <span data-ttu-id="79235-116">Windows XP Service Pack 2 或更新版本也會使用此 URL 來取得「 **線上購物音樂** 」功能。</span><span class="sxs-lookup"><span data-stu-id="79235-116">This URL is also used by Windows XP Service Pack 2 or later for the **Shop for music online** feature.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="79235-117">父/子項目</span><span class="sxs-lookup"><span data-stu-id="79235-117">Parent/Child Elements</span></span>



| <span data-ttu-id="79235-118">階層</span><span class="sxs-lookup"><span data-stu-id="79235-118">Hierarchy</span></span>       | <span data-ttu-id="79235-119">元素</span><span class="sxs-lookup"><span data-stu-id="79235-119">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="79235-120">父元素</span><span class="sxs-lookup"><span data-stu-id="79235-120">Parent elements</span></span> | <span data-ttu-id="79235-121">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="79235-121">**ServiceInfo**</span></span> |
| <span data-ttu-id="79235-122">子元素</span><span class="sxs-lookup"><span data-stu-id="79235-122">Child elements</span></span>  | <span data-ttu-id="79235-123">無</span><span class="sxs-lookup"><span data-stu-id="79235-123">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="79235-124">備註</span><span class="sxs-lookup"><span data-stu-id="79235-124">Remarks</span></span>

<span data-ttu-id="79235-125">當使用者按一下 Windows Media Player 中的按鈕或連結來購買 CD 或 DVD 時，播放 ServiceTask1 會將 URL 要求傳送給使用問號 (？ ) 查詢字串分隔符號所附加的參數。</span><span class="sxs-lookup"><span data-stu-id="79235-125">When the user clicks a button or link in Windows Media Player to purchase a CD or DVD, the Player sends the URL request to ServiceTask1 with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="79235-126">下表詳細說明以 URL 要求傳送的參數。</span><span class="sxs-lookup"><span data-stu-id="79235-126">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="79235-127">其他可能存在於舊版相容性的用途。</span><span class="sxs-lookup"><span data-stu-id="79235-127">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="79235-128">Name</span><span class="sxs-lookup"><span data-stu-id="79235-128">Name</span></span>         | <span data-ttu-id="79235-129">值</span><span class="sxs-lookup"><span data-stu-id="79235-129">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79235-130">*專輯*</span><span class="sxs-lookup"><span data-stu-id="79235-130">*Album*</span></span>      | <span data-ttu-id="79235-131">媒體專案之 **WM/AlbumTitle** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="79235-131">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="79235-132">*演出者*</span><span class="sxs-lookup"><span data-stu-id="79235-132">*Artist*</span></span>     | <span data-ttu-id="79235-133">**WM/AlbumArtist** 屬性的值（如果有的話），否則為媒體專案的 **Author** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="79235-133">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="79235-134">*大地 水準面*</span><span class="sxs-lookup"><span data-stu-id="79235-134">*geoid*</span></span>      | <span data-ttu-id="79235-135">Windows 地理位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="79235-135">Windows geographical location ID.</span></span> <span data-ttu-id="79235-136">在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="79235-136">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="79235-137">*locale*</span><span class="sxs-lookup"><span data-stu-id="79235-137">*locale*</span></span>     | <span data-ttu-id="79235-138">Windows Media Player 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="79235-138">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="79235-139">*標題*</span><span class="sxs-lookup"><span data-stu-id="79235-139">*Title*</span></span>      | <span data-ttu-id="79235-140">媒體專案的 **標題** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="79235-140">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="79235-141">*UFID*</span><span class="sxs-lookup"><span data-stu-id="79235-141">*UFID*</span></span>       | <span data-ttu-id="79235-142">媒體專案之 **WM/UniqueFileIdentifier** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="79235-142">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="79235-143">*userlocale*</span><span class="sxs-lookup"><span data-stu-id="79235-143">*userlocale*</span></span> | <span data-ttu-id="79235-144">Windows 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="79235-144">Windows locale ID.</span></span> <span data-ttu-id="79235-145">地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。</span><span class="sxs-lookup"><span data-stu-id="79235-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="79235-146">*version*</span><span class="sxs-lookup"><span data-stu-id="79235-146">*version*</span></span>    | <span data-ttu-id="79235-147">使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。</span><span class="sxs-lookup"><span data-stu-id="79235-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

<span data-ttu-id="79235-148">Windows XP Media Center Edition 2004 提供使用者介面，其設計目的是要在某個距離觀看。</span><span class="sxs-lookup"><span data-stu-id="79235-148">Windows XP Media Center Edition 2004 provides users with a user interface designed to be viewed at a distance.</span></span> <span data-ttu-id="79235-149">您應該針對要在大型顯示器上查看的 *MediaCenterURL* 參數建立網頁。</span><span class="sxs-lookup"><span data-stu-id="79235-149">You should create webpages for the *MediaCenterURL* parameter to be viewed on large displays.</span></span>

## <a name="requirements"></a><span data-ttu-id="79235-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="79235-150">Requirements</span></span>



| <span data-ttu-id="79235-151">需求</span><span class="sxs-lookup"><span data-stu-id="79235-151">Requirement</span></span> | <span data-ttu-id="79235-152">值</span><span class="sxs-lookup"><span data-stu-id="79235-152">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="79235-153">版本</span><span class="sxs-lookup"><span data-stu-id="79235-153">Version</span></span><br/> | <span data-ttu-id="79235-154">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="79235-154">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79235-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79235-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79235-156">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="79235-156">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="79235-157">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="79235-157">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="79235-158">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="79235-158">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






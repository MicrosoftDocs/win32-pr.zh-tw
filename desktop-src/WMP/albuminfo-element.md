---
title: AlbumInfo 元素
description: AlbumInfo 元素會指定當使用者選擇要查看特定媒體專案的詳細資訊時，Windows Media Player 顯示之網頁的 URL。
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- AlbumInfo 元素 Windows Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987147"
---
# <a name="albuminfo-element"></a><span data-ttu-id="2378f-104">AlbumInfo 元素</span><span class="sxs-lookup"><span data-stu-id="2378f-104">AlbumInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="2378f-105">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="2378f-105">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2378f-106">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="2378f-106">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2378f-107">**AlbumInfo** 元素會指定當使用者選擇要查看特定媒體專案的詳細資訊時，Windows Media Player 顯示之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="2378f-107">The **AlbumInfo** element specifies the URL for the webpage that Windows Media Player displays when the user chooses to view more information about a particular media item.</span></span>

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a><span data-ttu-id="2378f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="2378f-108">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="2378f-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>需要 (**URL**) </span><span class="sxs-lookup"><span data-stu-id="2378f-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="2378f-110">Windows Media Player 顯示之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="2378f-110">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="2378f-111">父/子項目</span><span class="sxs-lookup"><span data-stu-id="2378f-111">Parent/Child Elements</span></span>



| <span data-ttu-id="2378f-112">階層</span><span class="sxs-lookup"><span data-stu-id="2378f-112">Hierarchy</span></span>       | <span data-ttu-id="2378f-113">元素</span><span class="sxs-lookup"><span data-stu-id="2378f-113">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="2378f-114">父元素</span><span class="sxs-lookup"><span data-stu-id="2378f-114">Parent elements</span></span> | <span data-ttu-id="2378f-115">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="2378f-115">**ServiceInfo**</span></span> |
| <span data-ttu-id="2378f-116">子元素</span><span class="sxs-lookup"><span data-stu-id="2378f-116">Child elements</span></span>  | <span data-ttu-id="2378f-117">無</span><span class="sxs-lookup"><span data-stu-id="2378f-117">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="2378f-118">備註</span><span class="sxs-lookup"><span data-stu-id="2378f-118">Remarks</span></span>

<span data-ttu-id="2378f-119">當使用者按一下 Windows Media Player 中的按鈕來查看特定媒體專案的其他資訊時，播放玩家會使用問號 (？ ) 查詢字串分隔符號，以附加的參數來傳送 URL 要求。</span><span class="sxs-lookup"><span data-stu-id="2378f-119">When the user clicks a button in Windows Media Player to view additional information about a particular media item, the Player sends the URL request with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="2378f-120">下表詳細說明以 URL 要求傳送的參數。</span><span class="sxs-lookup"><span data-stu-id="2378f-120">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="2378f-121">其他可能存在於舊版相容性的用途。</span><span class="sxs-lookup"><span data-stu-id="2378f-121">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="2378f-122">Name</span><span class="sxs-lookup"><span data-stu-id="2378f-122">Name</span></span>         | <span data-ttu-id="2378f-123">值</span><span class="sxs-lookup"><span data-stu-id="2378f-123">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2378f-124">*專輯*</span><span class="sxs-lookup"><span data-stu-id="2378f-124">*Album*</span></span>      | <span data-ttu-id="2378f-125">媒體專案之 **WM/AlbumTitle** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2378f-125">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="2378f-126">*演出者*</span><span class="sxs-lookup"><span data-stu-id="2378f-126">*Artist*</span></span>     | <span data-ttu-id="2378f-127">**WM/AlbumArtist** 屬性的值（如果有的話），否則為媒體專案的 **Author** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="2378f-127">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="2378f-128">*大地 水準面*</span><span class="sxs-lookup"><span data-stu-id="2378f-128">*geoid*</span></span>      | <span data-ttu-id="2378f-129">Windows 地理位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2378f-129">Windows geographical location ID.</span></span> <span data-ttu-id="2378f-130">在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2378f-130">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="2378f-131">*locale*</span><span class="sxs-lookup"><span data-stu-id="2378f-131">*locale*</span></span>     | <span data-ttu-id="2378f-132">Windows Media Player 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="2378f-132">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="2378f-133">*標題*</span><span class="sxs-lookup"><span data-stu-id="2378f-133">*Title*</span></span>      | <span data-ttu-id="2378f-134">媒體專案的 **標題** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="2378f-134">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="2378f-135">*UFID*</span><span class="sxs-lookup"><span data-stu-id="2378f-135">*UFID*</span></span>       | <span data-ttu-id="2378f-136">媒體專案之 **WM/UniqueFileIdentifier** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2378f-136">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="2378f-137">*userlocale*</span><span class="sxs-lookup"><span data-stu-id="2378f-137">*userlocale*</span></span> | <span data-ttu-id="2378f-138">Windows 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="2378f-138">Windows locale ID.</span></span> <span data-ttu-id="2378f-139">地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。</span><span class="sxs-lookup"><span data-stu-id="2378f-139">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="2378f-140">*version*</span><span class="sxs-lookup"><span data-stu-id="2378f-140">*version*</span></span>    | <span data-ttu-id="2378f-141">使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。</span><span class="sxs-lookup"><span data-stu-id="2378f-141">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="2378f-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="2378f-142">Requirements</span></span>



| <span data-ttu-id="2378f-143">需求</span><span class="sxs-lookup"><span data-stu-id="2378f-143">Requirement</span></span> | <span data-ttu-id="2378f-144">值</span><span class="sxs-lookup"><span data-stu-id="2378f-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="2378f-145">版本</span><span class="sxs-lookup"><span data-stu-id="2378f-145">Version</span></span><br/> | <span data-ttu-id="2378f-146">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2378f-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2378f-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2378f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2378f-148">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="2378f-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="2378f-149">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="2378f-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="2378f-150">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="2378f-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






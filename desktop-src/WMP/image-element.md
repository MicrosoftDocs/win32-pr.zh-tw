---
title: " (WMP SDK) 的 Image 元素"
description: 請注意，本節將說明針對線上商店使用而設計的功能。 | (WMP SDK) 的 Image 元素
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- 影像元素 Windows Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976180"
---
# <a name="image-element-wmp-sdk"></a><span data-ttu-id="e4888-105"> (WMP SDK) 的 Image 元素</span><span class="sxs-lookup"><span data-stu-id="e4888-105">Image Element (WMP SDK)</span></span>

> [!Note]  
> <span data-ttu-id="e4888-106">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="e4888-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e4888-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="e4888-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e4888-108">**Image** 元素會指定 Windows Media Player 顯示給使用者以代表線上商店的影像。</span><span class="sxs-lookup"><span data-stu-id="e4888-108">The **Image** element specifies the images that Windows Media Player displays to the user to represent the online store.</span></span>

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="e4888-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e4888-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="e4888-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>類型1存放區所需的 **EulaURL** (，已忽略類型 2) </span><span class="sxs-lookup"><span data-stu-id="e4888-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (required for type 1 stores, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="e4888-111">Windows Media Player 在 [使用者授權合約] ([EULA) ] 對話方塊中顯示之標誌的 URL。</span><span class="sxs-lookup"><span data-stu-id="e4888-111">URL for the logo that Windows Media Player displays in the end user license agreement (EULA) dialog box.</span></span> <span data-ttu-id="e4888-112">這必須是 80 x 80 圖元的 PNG 影像。</span><span class="sxs-lookup"><span data-stu-id="e4888-112">This must be a PNG image that is 80 x 80 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e4888-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (選用) </span><span class="sxs-lookup"><span data-stu-id="e4888-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="e4888-114">Windows Media Player 在 [服務] 功能表上顯示之影像的 URL。</span><span class="sxs-lookup"><span data-stu-id="e4888-114">URL for the image that Windows Media Player displays on the services menu.</span></span> <span data-ttu-id="e4888-115">此映射必須是 15 x 15 圖元。</span><span class="sxs-lookup"><span data-stu-id="e4888-115">This image must be 15 x 15 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e4888-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (選用) </span><span class="sxs-lookup"><span data-stu-id="e4888-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="e4888-117">針對類型1線上商店，這是 Windows Media Player 在 [ **線上商店** ] 索引標籤中顯示之影像的 URL。針對 Windows Media Player 11，此映射的寬度必須為45圖元，且高度為13圖元。</span><span class="sxs-lookup"><span data-stu-id="e4888-117">For a type 1 online store, this is the URL for the image that Windows Media Player displays on the **Online Stores** tab. For Windows Media Player 11, this image must be 45 pixels wide by 13 pixels high.</span></span> <span data-ttu-id="e4888-118">針對 Windows Media Player 12，此映射的寬度必須為45圖元，高達30圖元。</span><span class="sxs-lookup"><span data-stu-id="e4888-118">For Windows Media Player 12, this image must be 45 pixels wide by 30 pixels high.</span></span> <span data-ttu-id="e4888-119">若要支援 Windows Media Player 的11和12版，您必須提供兩個不同的 ServiceInfo.xml 檔，其中每個檔都指向適當大小的 ServiceLargeURL 影像。</span><span class="sxs-lookup"><span data-stu-id="e4888-119">To support both versions 11 and 12 of Windows Media Player, you must provide two separate ServiceInfo.xml documents, each of which points to the appropriately sized image for ServiceLargeURL.</span></span>

<span data-ttu-id="e4888-120">針對第2類型的線上商店，這是 Windows Media Player 顯示在 [ **線上商店** ] 索引標籤旁邊或 [工作窗格] 按鈕旁邊之影像的 URL。</span><span class="sxs-lookup"><span data-stu-id="e4888-120">For a type 2 online store, this is the URL for the image that Windows Media Player displays beside the **Online Stores** tab or beside the task pane buttons.</span></span> <span data-ttu-id="e4888-121">此映射必須是 30 x 30 圖元。</span><span class="sxs-lookup"><span data-stu-id="e4888-121">This image must be 30 x 30 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e4888-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (選用) </span><span class="sxs-lookup"><span data-stu-id="e4888-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="e4888-123">顯示的標誌 URL，以及 **description** 元素中指定的行銷描述。</span><span class="sxs-lookup"><span data-stu-id="e4888-123">URL for the logo that is displayed along with the marketing description specified in the **Description** element.</span></span> <span data-ttu-id="e4888-124">如果未提供，則會是空白。</span><span class="sxs-lookup"><span data-stu-id="e4888-124">If it is not supplied, it will be blank.</span></span> <span data-ttu-id="e4888-125"> (所有類型，選擇性) 這必須是45圖元寬和13圖元高的 PNG 影像。</span><span class="sxs-lookup"><span data-stu-id="e4888-125">(All types, optional) This must be a PNG image that is 45 pixels wide and 13 pixels high.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="e4888-126">父/子項目</span><span class="sxs-lookup"><span data-stu-id="e4888-126">Parent/Child Elements</span></span>



| <span data-ttu-id="e4888-127">階層</span><span class="sxs-lookup"><span data-stu-id="e4888-127">Hierarchy</span></span>       | <span data-ttu-id="e4888-128">元素</span><span class="sxs-lookup"><span data-stu-id="e4888-128">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="e4888-129">父元素</span><span class="sxs-lookup"><span data-stu-id="e4888-129">Parent elements</span></span> | <span data-ttu-id="e4888-130">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e4888-130">**ServiceInfo**</span></span> |
| <span data-ttu-id="e4888-131">子元素</span><span class="sxs-lookup"><span data-stu-id="e4888-131">Child elements</span></span>  | <span data-ttu-id="e4888-132">無</span><span class="sxs-lookup"><span data-stu-id="e4888-132">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="e4888-133">備註</span><span class="sxs-lookup"><span data-stu-id="e4888-133">Remarks</span></span>

<span data-ttu-id="e4888-134">支援的影像格式為 .gif、.jpg、.bmp 和 .png (這是建議的格式) 。</span><span class="sxs-lookup"><span data-stu-id="e4888-134">The supported image formats are .gif, .jpg, .bmp, and .png (which is the recommended format).</span></span> <span data-ttu-id="e4888-135">支援和建議使用 Web 透明度。</span><span class="sxs-lookup"><span data-stu-id="e4888-135">Using Web transparency is both supported and recommended.</span></span> <span data-ttu-id="e4888-136">不支援動畫 GIF 檔。</span><span class="sxs-lookup"><span data-stu-id="e4888-136">Animated GIF files are not supported.</span></span>

<span data-ttu-id="e4888-137">如果您未提供 **MenuURL** 的值，Windows Media Player 在線上商店的功能表上，不會顯示任何圖形。</span><span class="sxs-lookup"><span data-stu-id="e4888-137">If you do not supply a value for **MenuURL**, Windows Media Player displays no graphic on the menu for your online store.</span></span>

<span data-ttu-id="e4888-138">您可以提供 ServiceLargeURL 的動畫影像。</span><span class="sxs-lookup"><span data-stu-id="e4888-138">You can provide an animated image for ServiceLargeURL.</span></span> <span data-ttu-id="e4888-139">在 Windows Media Player 10 或11中，影像會以動畫顯示。</span><span class="sxs-lookup"><span data-stu-id="e4888-139">In Windows Media Player 10 or 11, the image is animated.</span></span> <span data-ttu-id="e4888-140">在 Windows Media Player 12 中，只會顯示影像的第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="e4888-140">In Windows Media Player 12, only the first frame of the image is displayed.</span></span> <span data-ttu-id="e4888-141">若要提供動畫影像，請建立包含動畫後續畫面格的單一影像檔案。</span><span class="sxs-lookup"><span data-stu-id="e4888-141">To provide an animated image, create a single image file that contains successive frames of your animation.</span></span> <span data-ttu-id="e4888-142">例如，對於30圖元寬和30圖元高的影像，您可以在600圖元寬和30圖元高的影像中並排提供20個後續影像。</span><span class="sxs-lookup"><span data-stu-id="e4888-142">For example, for an image that is 30 pixels wide and 30 pixels high, you could supply 20 successive images side by side in an image that is 600 pixels wide and 30 pixels high.</span></span> <span data-ttu-id="e4888-143">Windows Media Player 會自動將20個個別影像顯示在另一個影像上，以建立這類影像的動畫。</span><span class="sxs-lookup"><span data-stu-id="e4888-143">Windows Media Player would automatically animate such an image by showing the 20 individual images one after another.</span></span> <span data-ttu-id="e4888-144">此動畫只會在線上商店開啟時出現一次;它不會重複。</span><span class="sxs-lookup"><span data-stu-id="e4888-144">This animation occurs only once when the online store opens; it does not repeat.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4888-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4888-145">Requirements</span></span>



| <span data-ttu-id="e4888-146">需求</span><span class="sxs-lookup"><span data-stu-id="e4888-146">Requirement</span></span> | <span data-ttu-id="e4888-147">值</span><span class="sxs-lookup"><span data-stu-id="e4888-147">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="e4888-148">版本</span><span class="sxs-lookup"><span data-stu-id="e4888-148">Version</span></span><br/> | <span data-ttu-id="e4888-149">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e4888-149">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4888-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4888-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4888-151">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="e4888-151">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e4888-152">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="e4888-152">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e4888-153">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="e4888-153">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






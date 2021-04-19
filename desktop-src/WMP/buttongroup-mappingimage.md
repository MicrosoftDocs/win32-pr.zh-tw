---
title: BUTTONGROUP. mappingImage
description: MappingImage 屬性會指定或抓取代表 BUTTONGROUP 之按鈕對應的影像名稱。
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP. mappingImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990702"
---
# <a name="buttongroupmappingimage"></a><span data-ttu-id="709e8-104">BUTTONGROUP. mappingImage</span><span class="sxs-lookup"><span data-stu-id="709e8-104">BUTTONGROUP.mappingImage</span></span>

<span data-ttu-id="709e8-105">**MappingImage** 屬性會指定或抓取代表 **BUTTONGROUP** 之按鈕對應的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="709e8-105">The **mappingImage** attribute specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a><span data-ttu-id="709e8-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="709e8-106">Possible Values</span></span>

<span data-ttu-id="709e8-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="709e8-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="709e8-108">備註</span><span class="sxs-lookup"><span data-stu-id="709e8-108">Remarks</span></span>

<span data-ttu-id="709e8-109">這是必須指定的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="709e8-109">This is a mandatory attribute that must be specified.</span></span>

<span data-ttu-id="709e8-110">對應影像的大小應該與主要 **影像** 相同。</span><span class="sxs-lookup"><span data-stu-id="709e8-110">The mapping image should be the same dimensions as the main **image**.</span></span> <span data-ttu-id="709e8-111">它是主影像可點擊區域的對應。</span><span class="sxs-lookup"><span data-stu-id="709e8-111">It is a map of the clickable areas of the main image.</span></span> <span data-ttu-id="709e8-112">以不同的色彩填滿每個可點按的區域，以建立地圖。</span><span class="sxs-lookup"><span data-stu-id="709e8-112">Construct the map by filling each clickable area with a different color.</span></span>

<span data-ttu-id="709e8-113">定義每個 **BUTTONELEMENT** 時，請使用 **mappingColor** 屬性來指定其在地圖中的色彩。</span><span class="sxs-lookup"><span data-stu-id="709e8-113">When defining each **BUTTONELEMENT**, designate its color from the map using the **mappingColor** attribute.</span></span> <span data-ttu-id="709e8-114">例如，如果主要影像中有一個停止符號形狀的按鈕圖形，您可以使用標示為紅色的區域來建立地圖。</span><span class="sxs-lookup"><span data-stu-id="709e8-114">For example, if you have a stop-sign-shaped button graphic in the main image, you can create a map with the area of the sign colored red.</span></span> <span data-ttu-id="709e8-115">然後，必須將 **BUTTONELEMENT** 屬性指定為紅色，才能讓「停止簽署」映射可供按一下。</span><span class="sxs-lookup"><span data-stu-id="709e8-115">The **BUTTONELEMENT** attribute must then be specified as red to make the stop-sign image clickable.</span></span>

<span data-ttu-id="709e8-116">支援的影像格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="709e8-116">The supported image formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span> <span data-ttu-id="709e8-117">由於 Jpg 是失真的，因此可能會發生非預期的色彩變更，因此不建議用於對應影像。</span><span class="sxs-lookup"><span data-stu-id="709e8-117">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for mapping images.</span></span>

## <a name="examples"></a><span data-ttu-id="709e8-118">範例</span><span class="sxs-lookup"><span data-stu-id="709e8-118">Examples</span></span>

<span data-ttu-id="709e8-119">下圖是 **mappingImage** 和它所對應之可見影像的範例。</span><span class="sxs-lookup"><span data-stu-id="709e8-119">The following illustration is an example of a **mappingImage** and the visible image it corresponds to.</span></span> <span data-ttu-id="709e8-120">這些映射屬於 SDK 隨附之小型資料夾中的面板。</span><span class="sxs-lookup"><span data-stu-id="709e8-120">These images are part of the skin in the Tiny folder included with the SDK.</span></span>

![範例對應影像](images/absam01m.png)![範例背景影像](images/absam01f.png)

<span data-ttu-id="709e8-123">請參閱 *BUTTONELEMENT*。說明如何使用此屬性之程式碼範例的 [mappingColor](buttonelement-mappingcolor.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="709e8-123">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a code sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="709e8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="709e8-124">Requirements</span></span>



| <span data-ttu-id="709e8-125">需求</span><span class="sxs-lookup"><span data-stu-id="709e8-125">Requirement</span></span> | <span data-ttu-id="709e8-126">值</span><span class="sxs-lookup"><span data-stu-id="709e8-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="709e8-127">版本</span><span class="sxs-lookup"><span data-stu-id="709e8-127">Version</span></span><br/> | <span data-ttu-id="709e8-128">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="709e8-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="709e8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="709e8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709e8-130">**BUTTONELEMENT.mappingColor**</span><span class="sxs-lookup"><span data-stu-id="709e8-130">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="709e8-131">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="709e8-131">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="709e8-132">**BUTTONGROUP 影像**</span><span class="sxs-lookup"><span data-stu-id="709e8-132">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="709e8-133">**BUTTONGROUP. transparencyColor**</span><span class="sxs-lookup"><span data-stu-id="709e8-133">**BUTTONGROUP.transparencyColor**</span></span>](buttongroup-transparencycolor.md)
</dt> </dl>

 

 






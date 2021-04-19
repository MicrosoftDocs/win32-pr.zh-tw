---
title: BUTTONGROUP. hoverImage
description: HoverImage 屬性會指定或抓取影像的名稱，代表 BUTTONGROUP 中按鈕的暫留狀態。 當按鈕處於 [已啟動] 狀態，且使用者將滑鼠停留在該按鈕上方時，就會發生停留狀態。
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- BUTTONGROUP. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974914"
---
# <a name="buttongrouphoverimage"></a><span data-ttu-id="e93e4-105">BUTTONGROUP. hoverImage</span><span class="sxs-lookup"><span data-stu-id="e93e4-105">BUTTONGROUP.hoverImage</span></span>

<span data-ttu-id="e93e4-106">**HoverImage** 屬性會指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫留狀態。</span><span class="sxs-lookup"><span data-stu-id="e93e4-106">The **hoverImage** attribute specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="e93e4-107">當按鈕處於 [已啟動] 狀態，且使用者將滑鼠停留在該按鈕上方時，就會發生停留狀態。</span><span class="sxs-lookup"><span data-stu-id="e93e4-107">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="e93e4-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="e93e4-108">Possible Values</span></span>

<span data-ttu-id="e93e4-109">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="e93e4-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e93e4-110">備註</span><span class="sxs-lookup"><span data-stu-id="e93e4-110">Remarks</span></span>

<span data-ttu-id="e93e4-111">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="e93e4-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="e93e4-112">如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。</span><span class="sxs-lookup"><span data-stu-id="e93e4-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="e93e4-113">預設影像是 **image** 屬性中指定的影像或其預設值。</span><span class="sxs-lookup"><span data-stu-id="e93e4-113">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="e93e4-114">如果暫留影像大於定義的區域，則會裁剪停留影像。</span><span class="sxs-lookup"><span data-stu-id="e93e4-114">If the hover image is larger than the defined region, the hover image will be cropped.</span></span>

<span data-ttu-id="e93e4-115">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="e93e4-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="e93e4-116">範例</span><span class="sxs-lookup"><span data-stu-id="e93e4-116">Examples</span></span>

<span data-ttu-id="e93e4-117">請參閱 *BUTTONELEMENT*。說明如何使用此屬性之範例的 [mappingColor](buttonelement-mappingcolor.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e93e4-117">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="e93e4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e93e4-118">Requirements</span></span>



| <span data-ttu-id="e93e4-119">需求</span><span class="sxs-lookup"><span data-stu-id="e93e4-119">Requirement</span></span> | <span data-ttu-id="e93e4-120">值</span><span class="sxs-lookup"><span data-stu-id="e93e4-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e93e4-121">版本</span><span class="sxs-lookup"><span data-stu-id="e93e4-121">Version</span></span><br/> | <span data-ttu-id="e93e4-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="e93e4-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e93e4-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e93e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93e4-124">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="e93e4-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="e93e4-125">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="e93e4-125">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="e93e4-126">**BUTTONGROUP 影像**</span><span class="sxs-lookup"><span data-stu-id="e93e4-126">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="e93e4-127">**BUTTONGROUP 飽和度**</span><span class="sxs-lookup"><span data-stu-id="e93e4-127">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 






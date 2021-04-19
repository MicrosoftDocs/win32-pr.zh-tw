---
title: BUTTONGROUP. transparencyColor
description: TransparencyColor 屬性會指定或抓取 BUTTONGROUP 影像的透明色彩。
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- BUTTONGROUP. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001810"
---
# <a name="buttongrouptransparencycolor"></a><span data-ttu-id="372e1-104">BUTTONGROUP. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="372e1-104">BUTTONGROUP.transparencyColor</span></span>

<span data-ttu-id="372e1-105">**TransparencyColor** 屬性會指定或抓取 **BUTTONGROUP** 影像的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="372e1-105">The **transparencyColor** attribute specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="372e1-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="372e1-106">Possible Values</span></span>

<span data-ttu-id="372e1-107">這個屬性是沒有預設值的讀取/寫入 **字串** ，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="372e1-107">This attribute is a read/write **String** with no default, containing one of the following values.</span></span>



| <span data-ttu-id="372e1-108">值</span><span class="sxs-lookup"><span data-stu-id="372e1-108">Value</span></span>                                       | <span data-ttu-id="372e1-109">描述</span><span class="sxs-lookup"><span data-stu-id="372e1-109">Description</span></span>                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="372e1-110">自動</span><span class="sxs-lookup"><span data-stu-id="372e1-110">Auto</span></span>                                        | <span data-ttu-id="372e1-111">影像中位置0、0的圖元會變成透明色彩。</span><span class="sxs-lookup"><span data-stu-id="372e1-111">The pixel at location 0,0 in the image becomes the transparent color.</span></span>                              |
| <span data-ttu-id="372e1-112">任何 Microsoft Internet Explorer 色彩值</span><span class="sxs-lookup"><span data-stu-id="372e1-112">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="372e1-113">Internet Explorer 色彩值變成透明色彩 (例如，「紅色」或「 \# FF0000」 ) 。</span><span class="sxs-lookup"><span data-stu-id="372e1-113">An Internet Explorer color value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="372e1-114">無</span><span class="sxs-lookup"><span data-stu-id="372e1-114">None</span></span>                                        | <span data-ttu-id="372e1-115">預設值。</span><span class="sxs-lookup"><span data-stu-id="372e1-115">Default.</span></span> <span data-ttu-id="372e1-116">沒有透明度。</span><span class="sxs-lookup"><span data-stu-id="372e1-116">No transparency.</span></span>                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="372e1-117">備註</span><span class="sxs-lookup"><span data-stu-id="372e1-117">Remarks</span></span>

<span data-ttu-id="372e1-118">影像中的透明色彩會允許影像背後的任何內容顯示在透明區域中。</span><span class="sxs-lookup"><span data-stu-id="372e1-118">A transparent color in an image will allow whatever is behind the image to show through the areas of transparency.</span></span> <span data-ttu-id="372e1-119">透明區域是可按的，除非 **clippingImage** 標記將其裁剪。</span><span class="sxs-lookup"><span data-stu-id="372e1-119">The transparent region is clickable unless clipped by the **clippingImage** tag.</span></span>

<span data-ttu-id="372e1-120">色彩可以是任何 Microsoft Internet Explorer 的色彩值。</span><span class="sxs-lookup"><span data-stu-id="372e1-120">The color can be any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="372e1-121">如果值為 Auto，則會使用影像中位置0、0的圖元色彩。</span><span class="sxs-lookup"><span data-stu-id="372e1-121">If the value is Auto, then the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="372e1-122">如果指定的色彩不是有效 Internet Explorer 色彩之一，則會傳回警告，並維持先前的值。</span><span class="sxs-lookup"><span data-stu-id="372e1-122">If the color specified is not one of the valid Internet Explorer colors, a warning is returned and the previous value is maintained.</span></span>

<span data-ttu-id="372e1-123">由於 Jpg 是有損耗的，因此可能會發生未預期的色彩變更，因此在使用 **transparencyColor** 時不建議使用。</span><span class="sxs-lookup"><span data-stu-id="372e1-123">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="372e1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="372e1-124">Requirements</span></span>



| <span data-ttu-id="372e1-125">需求</span><span class="sxs-lookup"><span data-stu-id="372e1-125">Requirement</span></span> | <span data-ttu-id="372e1-126">值</span><span class="sxs-lookup"><span data-stu-id="372e1-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="372e1-127">版本</span><span class="sxs-lookup"><span data-stu-id="372e1-127">Version</span></span><br/> | <span data-ttu-id="372e1-128">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="372e1-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="372e1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="372e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="372e1-130">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="372e1-130">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="372e1-131">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="372e1-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 






---
title: 按鈕. transparencyColor
description: TransparencyColor 屬性會指定或抓取按鈕影像中透明的色彩。
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- TransparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001190"
---
# <a name="buttontransparencycolor"></a><span data-ttu-id="b464f-104">按鈕. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="b464f-104">BUTTON.transparencyColor</span></span>

<span data-ttu-id="b464f-105">**TransparencyColor** 屬性會指定或抓取 **按鈕** 影像中透明的色彩。</span><span class="sxs-lookup"><span data-stu-id="b464f-105">The **transparencyColor** attribute specifies or retrieves the color that will be transparent in the **BUTTON** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="b464f-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="b464f-106">Possible Values</span></span>

<span data-ttu-id="b464f-107">這個屬性是一個不含預設值的讀取/寫入 **字串** ，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b464f-107">This attribute is a read/write **String** with no default containing one of the following values.</span></span>



| <span data-ttu-id="b464f-108">值</span><span class="sxs-lookup"><span data-stu-id="b464f-108">Value</span></span>                                    | <span data-ttu-id="b464f-109">描述</span><span class="sxs-lookup"><span data-stu-id="b464f-109">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b464f-110">自動</span><span class="sxs-lookup"><span data-stu-id="b464f-110">Auto</span></span>                                     | <span data-ttu-id="b464f-111">影像中位置0、0的圖元色彩會變成透明色彩。</span><span class="sxs-lookup"><span data-stu-id="b464f-111">The color of the pixel at location 0,0 in the image becomes the transparent color.</span></span>                        |
| <span data-ttu-id="b464f-112">任何 Internet Explorer 色彩格式值</span><span class="sxs-lookup"><span data-stu-id="b464f-112">Any Internet Explorer color format value</span></span> | <span data-ttu-id="b464f-113">Internet Explorer 的色彩格式值會變成透明色彩 (例如，「紅色」或「 \# FF0000」 ) 。</span><span class="sxs-lookup"><span data-stu-id="b464f-113">An Internet Explorer color format value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="b464f-114">無</span><span class="sxs-lookup"><span data-stu-id="b464f-114">None</span></span>                                     | <span data-ttu-id="b464f-115">沒有透明度。</span><span class="sxs-lookup"><span data-stu-id="b464f-115">No transparency.</span></span>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="b464f-116">備註</span><span class="sxs-lookup"><span data-stu-id="b464f-116">Remarks</span></span>

<span data-ttu-id="b464f-117">影像中的透明色彩可讓影像背後的任何內容顯示在透明區域中。</span><span class="sxs-lookup"><span data-stu-id="b464f-117">A transparent color in an image allows whatever is behind the image to show through the transparent areas.</span></span> <span data-ttu-id="b464f-118">**按鈕** 仍會在透明區域上收到點擊。</span><span class="sxs-lookup"><span data-stu-id="b464f-118">The **BUTTON** will still receive clicks on the transparent region.</span></span>

<span data-ttu-id="b464f-119">透明色彩可以是任何 Internet Explorer 的色彩值。</span><span class="sxs-lookup"><span data-stu-id="b464f-119">The transparent color can be any Internet Explorer color value.</span></span> <span data-ttu-id="b464f-120">如果 **transparencyColor** 屬性的值設定為「自動」，則會使用影像中位置0、0的圖元色彩。</span><span class="sxs-lookup"><span data-stu-id="b464f-120">If the value of the **transparencyColor** attribute is set to "Auto", the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="b464f-121">如果指定的色彩不是其中一種有效的 IE 色彩，則會保留先前的值。</span><span class="sxs-lookup"><span data-stu-id="b464f-121">If the color specified is not one of the valid IE colors, the previous value is maintained.</span></span>

<span data-ttu-id="b464f-122">由於 Jpg 是有損耗的，因此可能會發生未預期的色彩變更，因此在使用 **transparencyColor** 時不建議使用。</span><span class="sxs-lookup"><span data-stu-id="b464f-122">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b464f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b464f-123">Requirements</span></span>



| <span data-ttu-id="b464f-124">需求</span><span class="sxs-lookup"><span data-stu-id="b464f-124">Requirement</span></span> | <span data-ttu-id="b464f-125">值</span><span class="sxs-lookup"><span data-stu-id="b464f-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b464f-126">版本</span><span class="sxs-lookup"><span data-stu-id="b464f-126">Version</span></span><br/> | <span data-ttu-id="b464f-127">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b464f-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b464f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b464f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b464f-129">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="b464f-129">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="b464f-130">**按鈕。影像**</span><span class="sxs-lookup"><span data-stu-id="b464f-130">**BUTTON.image**</span></span>](button-image.md)
</dt> <dt>

[<span data-ttu-id="b464f-131">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="b464f-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 






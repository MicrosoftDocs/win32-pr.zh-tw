---
title: BackgroundColor
description: BackgroundColor 屬性會指定或抓取文字控制項的背景色彩。
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- BackgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995638"
---
# <a name="textbackgroundcolor"></a><span data-ttu-id="af047-104">BackgroundColor</span><span class="sxs-lookup"><span data-stu-id="af047-104">TEXT.backgroundColor</span></span>

<span data-ttu-id="af047-105">**BackgroundColor** 屬性會指定或抓取文字控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="af047-105">The **backgroundColor** attribute specifies or retrieves the background color for the Text control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="af047-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="af047-106">Possible Values</span></span>

<span data-ttu-id="af047-107">這個屬性是包含任何 Microsoft Internet Explorer 色彩值或值為 "none" 的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="af047-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="af047-108">預設值為 "none"，表示背景是透明的。</span><span class="sxs-lookup"><span data-stu-id="af047-108">It has a default value of "none", which means the background is transparent.</span></span>

## <a name="remarks"></a><span data-ttu-id="af047-109">備註</span><span class="sxs-lookup"><span data-stu-id="af047-109">Remarks</span></span>

<span data-ttu-id="af047-110">背景色彩會設定為控制項的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="af047-110">The background color is set for the height and width of the control.</span></span> <span data-ttu-id="af047-111">如果未設定高度和寬度，則會將背景色彩設定為文字的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="af047-111">If height and width are not set, the background color is set to the height and width of the text.</span></span>

<span data-ttu-id="af047-112">當您使用 **AlphaBlend** 或 **AlphaBlendTo** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="af047-112">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="af047-113">如果前景色彩也是黑色 (這是 **foregroundColor** 屬性) 的預設值，您的文字可能會變成無法讀取。</span><span class="sxs-lookup"><span data-stu-id="af047-113">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="af047-114">若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。</span><span class="sxs-lookup"><span data-stu-id="af047-114">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

<span data-ttu-id="af047-115">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="af047-115">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="af047-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="af047-116">Requirements</span></span>



| <span data-ttu-id="af047-117">需求</span><span class="sxs-lookup"><span data-stu-id="af047-117">Requirement</span></span> | <span data-ttu-id="af047-118">值</span><span class="sxs-lookup"><span data-stu-id="af047-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="af047-119">版本</span><span class="sxs-lookup"><span data-stu-id="af047-119">Version</span></span><br/> | <span data-ttu-id="af047-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="af047-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af047-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af047-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af047-122">**AmbientAttributes. AlphaBlend**</span><span class="sxs-lookup"><span data-stu-id="af047-122">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="af047-123">**AmbientAttributes.AlphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="af047-123">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="af047-124">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="af047-124">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="af047-125">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="af047-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="af047-126">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="af047-126">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 






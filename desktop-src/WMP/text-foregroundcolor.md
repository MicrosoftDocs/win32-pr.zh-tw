---
title: ForegroundColor
description: ForegroundColor 屬性會指定或抓取文字控制項的文字色彩。
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- ForegroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982951"
---
# <a name="textforegroundcolor"></a><span data-ttu-id="8219a-104">ForegroundColor</span><span class="sxs-lookup"><span data-stu-id="8219a-104">TEXT.foregroundColor</span></span>

<span data-ttu-id="8219a-105">**ForegroundColor** 屬性會指定或抓取文字控制項的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="8219a-105">The **foregroundColor** attribute specifies or retrieves the text color for the Text control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="8219a-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="8219a-106">Possible Values</span></span>

<span data-ttu-id="8219a-107">這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="8219a-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="8219a-108">預設值為「黑色」。</span><span class="sxs-lookup"><span data-stu-id="8219a-108">The default value is "black".</span></span>

<span data-ttu-id="8219a-109">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="8219a-109">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

<span data-ttu-id="8219a-110">當您使用 **AlphaBlend** 或 **AlphaBlendTo** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="8219a-110">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="8219a-111">如果前景色彩也是黑色 (這是 **foregroundColor** 屬性) 的預設值，您的文字可能會變成無法讀取。</span><span class="sxs-lookup"><span data-stu-id="8219a-111">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="8219a-112">若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。</span><span class="sxs-lookup"><span data-stu-id="8219a-112">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

## <a name="requirements"></a><span data-ttu-id="8219a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8219a-113">Requirements</span></span>



| <span data-ttu-id="8219a-114">需求</span><span class="sxs-lookup"><span data-stu-id="8219a-114">Requirement</span></span> | <span data-ttu-id="8219a-115">值</span><span class="sxs-lookup"><span data-stu-id="8219a-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8219a-116">版本</span><span class="sxs-lookup"><span data-stu-id="8219a-116">Version</span></span><br/> | <span data-ttu-id="8219a-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8219a-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8219a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8219a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8219a-119">**AmbientAttributes. AlphaBlend**</span><span class="sxs-lookup"><span data-stu-id="8219a-119">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="8219a-120">**AmbientAttributes.AlphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="8219a-120">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="8219a-121">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="8219a-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="8219a-122">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="8219a-122">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="8219a-123">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="8219a-123">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> </dl>

 

 






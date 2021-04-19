---
title: AmbientAttributes.AlphaBlendTo
description: AlphaBlendTo 方法會在一段時間內調整 AlphaBlend 屬性。
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes. AlphaBlendTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999333"
---
# <a name="ambientattributesalphablendto"></a><span data-ttu-id="1b4e8-104">AmbientAttributes.AlphaBlendTo</span><span class="sxs-lookup"><span data-stu-id="1b4e8-104">AmbientAttributes.alphaBlendTo</span></span>

<span data-ttu-id="1b4e8-105">**AlphaBlendTo** 方法會在一段時間內調整 **AlphaBlend** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-105">The **alphaBlendTo** method adjusts the **alphaBlend** property over a period of time.</span></span>

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a><span data-ttu-id="1b4e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="1b4e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4e8-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span><span class="sxs-lookup"><span data-stu-id="1b4e8-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span></span>
</dt> <dd>

<span data-ttu-id="1b4e8-108"> (long) 指定新的不透明度值的 **數位**。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-108">**Number** (long) specifying the new opacity value.</span></span> <span data-ttu-id="1b4e8-109">範圍從 0 (不會) 255 (完全不透明度) 。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-109">Ranges from 0 (no opacity) to 255 (full opacity).</span></span>

</dd> <dt>

<span data-ttu-id="1b4e8-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*AlphaTime*</span><span class="sxs-lookup"><span data-stu-id="1b4e8-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span></span>
</dt> <dd>

<span data-ttu-id="1b4e8-111">**Number** (**long**) 指定時間（以毫秒為單位），這會讓元素變更不透明度。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-111">**Number** (**long**) specifying the time, in milliseconds, that it takes the element to change opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4e8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b4e8-112">Return Value</span></span>

<span data-ttu-id="1b4e8-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b4e8-114">備註</span><span class="sxs-lookup"><span data-stu-id="1b4e8-114">Remarks</span></span>

<span data-ttu-id="1b4e8-115">這個方法適用于讓元素逐漸出現或消失。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-115">This method is useful for making elements gradually appear or disappear.</span></span>

<span data-ttu-id="1b4e8-116">當您使用 **AlphaBlendTo** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-116">When you use **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="1b4e8-117">如果前景色彩也是黑色 (這是 *文字* 的預設值。**foregroundColor**) ，您的文字可能會變成無法讀取。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="1b4e8-118">若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="1b4e8-119">Windows 98 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1b4e8-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b4e8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b4e8-120">Requirements</span></span>



| <span data-ttu-id="1b4e8-121">需求</span><span class="sxs-lookup"><span data-stu-id="1b4e8-121">Requirement</span></span> | <span data-ttu-id="1b4e8-122">值</span><span class="sxs-lookup"><span data-stu-id="1b4e8-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1b4e8-123">版本</span><span class="sxs-lookup"><span data-stu-id="1b4e8-123">Version</span></span><br/> | <span data-ttu-id="1b4e8-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1b4e8-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b4e8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b4e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4e8-126">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b4e8-127">**AmbientAttributes. AlphaBlend**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-127">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="1b4e8-128">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="1b4e8-129">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="1b4e8-130">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="1b4e8-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 






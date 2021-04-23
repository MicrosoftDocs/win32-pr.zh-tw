---
description: 效果元素定義音訊或影片效果物件。 效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: 'effect 元素 (Gdipluseffects .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908656"
---
# <a name="effect-element"></a><span data-ttu-id="cd631-104">effect 元素</span><span class="sxs-lookup"><span data-stu-id="cd631-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="cd631-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="cd631-105">\[Deprecated.</span></span> <span data-ttu-id="cd631-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="cd631-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cd631-107">`effect`元素定義音訊或影片效果物件。</span><span class="sxs-lookup"><span data-stu-id="cd631-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="cd631-108">效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。</span><span class="sxs-lookup"><span data-stu-id="cd631-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="cd631-109">屬性</span><span class="sxs-lookup"><span data-stu-id="cd631-109">Attributes</span></span>

<span data-ttu-id="cd631-110">[**clsid**](clsid-attribute.md)、[**鎖定**](lock-attribute.md)、[**靜音**](mute-attribute.md)、[**啟動**](start-attribute.md)、[**停止**](stop-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid、使用者**](userid-attribute.md)[**名稱**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="cd631-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="cd631-111">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="cd631-111">Parent/Child Information</span></span>



| <span data-ttu-id="cd631-112">標籤</span><span class="sxs-lookup"><span data-stu-id="cd631-112">Label</span></span> | <span data-ttu-id="cd631-113">值</span><span class="sxs-lookup"><span data-stu-id="cd631-113">Value</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd631-114">父代</span><span class="sxs-lookup"><span data-stu-id="cd631-114">Parent</span></span>   | <span data-ttu-id="cd631-115">[**複合**](composite-element.md)、 [**群組**](group-element.md)、 [**剪輯**](clip-element.md)、 [**追蹤**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="cd631-115">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="cd631-116">Children</span><span class="sxs-lookup"><span data-stu-id="cd631-116">Children</span></span> | [<span data-ttu-id="cd631-117">**參數**</span><span class="sxs-lookup"><span data-stu-id="cd631-117">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="cd631-118">備註</span><span class="sxs-lookup"><span data-stu-id="cd631-118">Remarks</span></span>

<span data-ttu-id="cd631-119">**Clsid** 屬性會指定建立效果的子物件。</span><span class="sxs-lookup"><span data-stu-id="cd631-119">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="cd631-120">範例</span><span class="sxs-lookup"><span data-stu-id="cd631-120">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="cd631-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd631-121">Requirements</span></span>



| <span data-ttu-id="cd631-122">需求</span><span class="sxs-lookup"><span data-stu-id="cd631-122">Requirement</span></span> | <span data-ttu-id="cd631-123">值</span><span class="sxs-lookup"><span data-stu-id="cd631-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd631-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cd631-124">Header</span></span><br/> | <dl> <span data-ttu-id="cd631-125"><dt>Gdipluseffects。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd631-125"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd631-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd631-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd631-127">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="cd631-127">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 





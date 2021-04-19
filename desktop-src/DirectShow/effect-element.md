---
description: 效果元素定義音訊或影片效果物件。 效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: 'effect 元素 (Gdipluseffects .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991187"
---
# <a name="effect-element"></a><span data-ttu-id="c4e39-104">effect 元素</span><span class="sxs-lookup"><span data-stu-id="c4e39-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="c4e39-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c4e39-105">\[Deprecated.</span></span> <span data-ttu-id="c4e39-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c4e39-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4e39-107">`effect`元素定義音訊或影片效果物件。</span><span class="sxs-lookup"><span data-stu-id="c4e39-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="c4e39-108">效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。</span><span class="sxs-lookup"><span data-stu-id="c4e39-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="c4e39-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c4e39-109">Attributes</span></span>

<span data-ttu-id="c4e39-110">[**clsid**](clsid-attribute.md)、[**鎖定**](lock-attribute.md)、[**靜音**](mute-attribute.md)、[**啟動**](start-attribute.md)、[**停止**](stop-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid、使用者**](userid-attribute.md)[**名稱**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="c4e39-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="c4e39-111">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="c4e39-111">Parent/Child Information</span></span>



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e39-112">父代</span><span class="sxs-lookup"><span data-stu-id="c4e39-112">Parent</span></span>   | <span data-ttu-id="c4e39-113">[**複合**](composite-element.md)、 [**群組**](group-element.md)、 [**剪輯**](clip-element.md)、 [**追蹤**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="c4e39-113">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="c4e39-114">Children</span><span class="sxs-lookup"><span data-stu-id="c4e39-114">Children</span></span> | [<span data-ttu-id="c4e39-115">**參數**</span><span class="sxs-lookup"><span data-stu-id="c4e39-115">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c4e39-116">備註</span><span class="sxs-lookup"><span data-stu-id="c4e39-116">Remarks</span></span>

<span data-ttu-id="c4e39-117">**Clsid** 屬性會指定建立效果的子物件。</span><span class="sxs-lookup"><span data-stu-id="c4e39-117">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="c4e39-118">範例</span><span class="sxs-lookup"><span data-stu-id="c4e39-118">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="c4e39-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4e39-119">Requirements</span></span>



| <span data-ttu-id="c4e39-120">需求</span><span class="sxs-lookup"><span data-stu-id="c4e39-120">Requirement</span></span> | <span data-ttu-id="c4e39-121">值</span><span class="sxs-lookup"><span data-stu-id="c4e39-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e39-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c4e39-122">Header</span></span><br/> | <dl> <span data-ttu-id="c4e39-123"><dt>Gdipluseffects。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4e39-123"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e39-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4e39-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e39-125">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="c4e39-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 





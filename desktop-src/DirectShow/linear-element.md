---
description: 線性元素會在特定時間定義 param 專案的值，相對於包含 param 專案的轉換或效果的開頭。
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: '線性元素 (Camerauicontrol .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910086"
---
# <a name="linear-element"></a><span data-ttu-id="3abcc-103">線性元素</span><span class="sxs-lookup"><span data-stu-id="3abcc-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="3abcc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3abcc-104">\[Deprecated.</span></span> <span data-ttu-id="3abcc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3abcc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3abcc-106">線性元素會在特定時間定義 [**param**](param-element.md) 專案的值，相對於包含 **param** 專案的轉換或效果的開頭。</span><span class="sxs-lookup"><span data-stu-id="3abcc-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="3abcc-107">`linear`元素會讓參數從先前的值轉換成新值。</span><span class="sxs-lookup"><span data-stu-id="3abcc-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="3abcc-108">若要立即跳至新的值，請使用 [**at**](at-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="3abcc-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="3abcc-109">屬性</span><span class="sxs-lookup"><span data-stu-id="3abcc-109">Attributes</span></span>

<span data-ttu-id="3abcc-110">[**時間**](time-attribute.md)、 [**值**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="3abcc-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="3abcc-111">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="3abcc-111">Parent/Child Information</span></span>



| <span data-ttu-id="3abcc-112">標籤</span><span class="sxs-lookup"><span data-stu-id="3abcc-112">Label</span></span> | <span data-ttu-id="3abcc-113">值</span><span class="sxs-lookup"><span data-stu-id="3abcc-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="3abcc-114">父代</span><span class="sxs-lookup"><span data-stu-id="3abcc-114">Parent</span></span>   | [<span data-ttu-id="3abcc-115">**參數**</span><span class="sxs-lookup"><span data-stu-id="3abcc-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="3abcc-116">Children</span><span class="sxs-lookup"><span data-stu-id="3abcc-116">Children</span></span> | <span data-ttu-id="3abcc-117">無</span><span class="sxs-lookup"><span data-stu-id="3abcc-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="3abcc-118">範例</span><span class="sxs-lookup"><span data-stu-id="3abcc-118">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="3abcc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3abcc-119">Requirements</span></span>



| <span data-ttu-id="3abcc-120">需求</span><span class="sxs-lookup"><span data-stu-id="3abcc-120">Requirement</span></span> | <span data-ttu-id="3abcc-121">值</span><span class="sxs-lookup"><span data-stu-id="3abcc-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abcc-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3abcc-122">Header</span></span><br/> | <dl> <span data-ttu-id="3abcc-123"><dt>Camerauicontrol。h</dt></span><span class="sxs-lookup"><span data-stu-id="3abcc-123"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3abcc-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3abcc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3abcc-125">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="3abcc-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 





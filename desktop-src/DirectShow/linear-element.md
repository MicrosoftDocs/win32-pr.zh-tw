---
description: 線性元素會在特定時間定義 param 專案的值，相對於包含 param 專案的轉換或效果的開頭。
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: '線性元素 (Camerauicontrol .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999100"
---
# <a name="linear-element"></a><span data-ttu-id="4db98-103">線性元素</span><span class="sxs-lookup"><span data-stu-id="4db98-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="4db98-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4db98-104">\[Deprecated.</span></span> <span data-ttu-id="4db98-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4db98-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4db98-106">線性元素會在特定時間定義 [**param**](param-element.md) 專案的值，相對於包含 **param** 專案的轉換或效果的開頭。</span><span class="sxs-lookup"><span data-stu-id="4db98-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="4db98-107">`linear`元素會讓參數從先前的值轉換成新值。</span><span class="sxs-lookup"><span data-stu-id="4db98-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="4db98-108">若要立即跳至新的值，請使用 [**at**](at-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="4db98-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="4db98-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4db98-109">Attributes</span></span>

<span data-ttu-id="4db98-110">[**時間**](time-attribute.md)、 [**值**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="4db98-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="4db98-111">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="4db98-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="4db98-112">父代</span><span class="sxs-lookup"><span data-stu-id="4db98-112">Parent</span></span>   | [<span data-ttu-id="4db98-113">**參數**</span><span class="sxs-lookup"><span data-stu-id="4db98-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="4db98-114">Children</span><span class="sxs-lookup"><span data-stu-id="4db98-114">Children</span></span> | <span data-ttu-id="4db98-115">無</span><span class="sxs-lookup"><span data-stu-id="4db98-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="4db98-116">範例</span><span class="sxs-lookup"><span data-stu-id="4db98-116">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="4db98-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4db98-117">Requirements</span></span>



| <span data-ttu-id="4db98-118">需求</span><span class="sxs-lookup"><span data-stu-id="4db98-118">Requirement</span></span> | <span data-ttu-id="4db98-119">值</span><span class="sxs-lookup"><span data-stu-id="4db98-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db98-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4db98-120">Header</span></span><br/> | <dl> <span data-ttu-id="4db98-121"><dt>Camerauicontrol。h</dt></span><span class="sxs-lookup"><span data-stu-id="4db98-121"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db98-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4db98-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db98-123">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="4db98-123">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 





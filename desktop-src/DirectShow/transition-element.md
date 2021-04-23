---
description: 轉換元素會定義轉換物件。 轉換是兩個輸入轉換，會導致從某個資料流程 (例如複合或追蹤) 轉換為另一個資料流程。
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: 轉換元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910036"
---
# <a name="transition-element"></a><span data-ttu-id="fee5b-104">轉換元素</span><span class="sxs-lookup"><span data-stu-id="fee5b-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="fee5b-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fee5b-105">\[Deprecated.</span></span> <span data-ttu-id="fee5b-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fee5b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fee5b-107">`transition`元素會定義轉換物件。</span><span class="sxs-lookup"><span data-stu-id="fee5b-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="fee5b-108">轉換是兩個輸入轉換，會導致從某個資料流程 (例如複合或追蹤) 轉換為另一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="fee5b-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="fee5b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="fee5b-109">Attributes</span></span>

<span data-ttu-id="fee5b-110">[**clsid**](clsid-attribute.md)、 [**cutpoint**](cutpoint-attribute.md)、 [**cutsonly**](cutsonly-attribute.md)、 [**lock**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**start**](start-attribute.md)、 [**stop**](stop-attribute.md)、 [**swapinputs**](swapinputs-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="fee5b-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="fee5b-111">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="fee5b-111">Parent/Child Information</span></span>



| <span data-ttu-id="fee5b-112">標籤</span><span class="sxs-lookup"><span data-stu-id="fee5b-112">Label</span></span> | <span data-ttu-id="fee5b-113">值</span><span class="sxs-lookup"><span data-stu-id="fee5b-113">Value</span></span> |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="fee5b-114">父代</span><span class="sxs-lookup"><span data-stu-id="fee5b-114">Parent</span></span>   | <span data-ttu-id="fee5b-115">[**複合**](composite-element.md)、 [**追蹤**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="fee5b-115">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="fee5b-116">Children</span><span class="sxs-lookup"><span data-stu-id="fee5b-116">Children</span></span> | [<span data-ttu-id="fee5b-117">**參數**</span><span class="sxs-lookup"><span data-stu-id="fee5b-117">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="fee5b-118">備註</span><span class="sxs-lookup"><span data-stu-id="fee5b-118">Remarks</span></span>

<span data-ttu-id="fee5b-119">**Clsid** 屬性會指定建立轉換的子物件。</span><span class="sxs-lookup"><span data-stu-id="fee5b-119">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="fee5b-120">範例</span><span class="sxs-lookup"><span data-stu-id="fee5b-120">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="fee5b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fee5b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee5b-122">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="fee5b-122">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




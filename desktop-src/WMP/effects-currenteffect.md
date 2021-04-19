---
title: 效果。 currentEffect
description: CurrentEffect 屬性會指定或抓取目前的視覺效果。
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- 效果： currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000384"
---
# <a name="effectscurrenteffect"></a><span data-ttu-id="20f0d-104">效果。 currentEffect</span><span class="sxs-lookup"><span data-stu-id="20f0d-104">EFFECTS.currentEffect</span></span>

<span data-ttu-id="20f0d-105">**CurrentEffect** 屬性會指定或抓取目前的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="20f0d-105">The **currentEffect** attribute specifies or retrieves the current visualization.</span></span>

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a><span data-ttu-id="20f0d-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="20f0d-106">Possible Values</span></span>

<span data-ttu-id="20f0d-107">此屬性是讀取/寫入 **物件**。</span><span class="sxs-lookup"><span data-stu-id="20f0d-107">This attribute is a read/write **object**.</span></span> <span data-ttu-id="20f0d-108">預設值是撰寫順序中的第一個視覺效果。</span><span class="sxs-lookup"><span data-stu-id="20f0d-108">The default value is the first visualization in the authoring order.</span></span> <span data-ttu-id="20f0d-109">如果面板中未撰寫任何視覺效果，則預設為登錄中的第一個視覺效果。</span><span class="sxs-lookup"><span data-stu-id="20f0d-109">If there are no visualizations authored in the skin, the default is the first visualization in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="20f0d-110">備註</span><span class="sxs-lookup"><span data-stu-id="20f0d-110">Remarks</span></span>

<span data-ttu-id="20f0d-111">您可以使用此物件來存取您所建立的自訂視覺效果。</span><span class="sxs-lookup"><span data-stu-id="20f0d-111">You can use this object to access custom visualizations you have created.</span></span> <span data-ttu-id="20f0d-112">例如，您可以透過視覺效果中的 **IDispatch** 介面公開屬性。</span><span class="sxs-lookup"><span data-stu-id="20f0d-112">For example, you could expose a property through the **IDispatch** interface in your visualization.</span></span> <span data-ttu-id="20f0d-113">然後，您可以將視覺效果設為目前效果，然後使用 **currentEffect** 物件來設定屬性的新值，藉以變更面板中的屬性值。</span><span class="sxs-lookup"><span data-stu-id="20f0d-113">You can then change the property value from your skin by making your visualization the current effect, and then using the **currentEffect** object to set a new value for the property.</span></span> <span data-ttu-id="20f0d-114">例如，如果您的視覺效果公開名為 backgroundColor 的屬性，則下列 JScript 程式碼會指定新的值：</span><span class="sxs-lookup"><span data-stu-id="20f0d-114">For example, if your visualization exposes a property named backgroundColor, the following JScript code specifies a new value:</span></span>


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a><span data-ttu-id="20f0d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="20f0d-115">Requirements</span></span>



| <span data-ttu-id="20f0d-116">需求</span><span class="sxs-lookup"><span data-stu-id="20f0d-116">Requirement</span></span> | <span data-ttu-id="20f0d-117">值</span><span class="sxs-lookup"><span data-stu-id="20f0d-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="20f0d-118">版本</span><span class="sxs-lookup"><span data-stu-id="20f0d-118">Version</span></span><br/> | <span data-ttu-id="20f0d-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="20f0d-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20f0d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20f0d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f0d-121">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="20f0d-121">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="20f0d-122">**效果。 currentEffectTitle**</span><span class="sxs-lookup"><span data-stu-id="20f0d-122">**EFFECTS.currentEffectTitle**</span></span>](effects-currenteffecttitle.md)
</dt> <dt>

[<span data-ttu-id="20f0d-123">**效果。 currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="20f0d-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 






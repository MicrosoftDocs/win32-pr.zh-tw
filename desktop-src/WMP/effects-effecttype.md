---
title: 效果。 >effecttype
description: '>effecttype 方法會使用指定的登錄索引來抓取視覺效果的登錄名稱。 這個名稱是視覺效果作者所定義的唯一識別碼。'
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- 效果： >effecttype Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978716"
---
# <a name="effectseffecttype"></a><span data-ttu-id="90ff1-105">效果。 >effecttype</span><span class="sxs-lookup"><span data-stu-id="90ff1-105">EFFECTS.effectType</span></span>

<span data-ttu-id="90ff1-106">**>effecttype** 方法會使用指定的登錄索引來抓取視覺效果的登錄名稱。</span><span class="sxs-lookup"><span data-stu-id="90ff1-106">The **effectType** method retrieves the registry name of the visualization with the specified registry index.</span></span> <span data-ttu-id="90ff1-107">這個名稱是視覺效果作者所定義的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="90ff1-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a><span data-ttu-id="90ff1-108">參數</span><span class="sxs-lookup"><span data-stu-id="90ff1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ff1-109"><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="90ff1-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="90ff1-110">包含視覺效果登錄索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="90ff1-110">**Number** (**long**) containing the registry index of a visualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ff1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="90ff1-111">Return Value</span></span>

<span data-ttu-id="90ff1-112">這個方法會傳回 **字串**。</span><span class="sxs-lookup"><span data-stu-id="90ff1-112">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ff1-113">備註</span><span class="sxs-lookup"><span data-stu-id="90ff1-113">Remarks</span></span>

<span data-ttu-id="90ff1-114">在腳本的視覺效果之間切換時，這個方法很有用。</span><span class="sxs-lookup"><span data-stu-id="90ff1-114">This method is useful for switching between visualizations in script.</span></span> <span data-ttu-id="90ff1-115">使用者介面可以顯示一組標題，但是當使用者選取其中一個時，腳本必須使用 **currentEffectType** 來切換視覺效果。</span><span class="sxs-lookup"><span data-stu-id="90ff1-115">A user interface could display the set of titles, but when the user selects one, the script must use **currentEffectType** to switch visualizations.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ff1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="90ff1-116">Requirements</span></span>



| <span data-ttu-id="90ff1-117">需求</span><span class="sxs-lookup"><span data-stu-id="90ff1-117">Requirement</span></span> | <span data-ttu-id="90ff1-118">值</span><span class="sxs-lookup"><span data-stu-id="90ff1-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="90ff1-119">版本</span><span class="sxs-lookup"><span data-stu-id="90ff1-119">Version</span></span><br/> | <span data-ttu-id="90ff1-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="90ff1-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90ff1-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90ff1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ff1-122">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="90ff1-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="90ff1-123">**效果。 currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="90ff1-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 






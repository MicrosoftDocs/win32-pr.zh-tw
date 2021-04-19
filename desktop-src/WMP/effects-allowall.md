---
title: 效果。 allowAll
description: AllowAll 屬性會指定或抓取值，指出是否要包含登錄中的所有視覺效果。
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- 效果： allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985552"
---
# <a name="effectsallowall"></a><span data-ttu-id="38b1e-104">效果。 allowAll</span><span class="sxs-lookup"><span data-stu-id="38b1e-104">EFFECTS.allowAll</span></span>

<span data-ttu-id="38b1e-105">**AllowAll** 屬性會指定或抓取值，指出是否要包含登錄中的所有視覺效果。</span><span class="sxs-lookup"><span data-stu-id="38b1e-105">The **allowAll** attribute specifies or retrieves a value indicating whether to include all the visualizations that are in the registry.</span></span>

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a><span data-ttu-id="38b1e-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="38b1e-106">Possible Values</span></span>

<span data-ttu-id="38b1e-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="38b1e-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="38b1e-108">值</span><span class="sxs-lookup"><span data-stu-id="38b1e-108">Value</span></span> | <span data-ttu-id="38b1e-109">描述</span><span class="sxs-lookup"><span data-stu-id="38b1e-109">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="38b1e-110">true</span><span class="sxs-lookup"><span data-stu-id="38b1e-110">true</span></span>  | <span data-ttu-id="38b1e-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="38b1e-111">Default.</span></span> <span data-ttu-id="38b1e-112">允許迴圈使用者系統上的所有視覺效果。</span><span class="sxs-lookup"><span data-stu-id="38b1e-112">Allows cycling of all visualizations on the user's system.</span></span> |
| <span data-ttu-id="38b1e-113">false</span><span class="sxs-lookup"><span data-stu-id="38b1e-113">false</span></span> | <span data-ttu-id="38b1e-114">限制迴圈出現在 **效果** 標記內的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="38b1e-114">Limits cycling to visualizations appearing within **EFFECTS** tags.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="38b1e-115">備註</span><span class="sxs-lookup"><span data-stu-id="38b1e-115">Remarks</span></span>

<span data-ttu-id="38b1e-116">如果這個屬性設定為 false，則只有在 **效果** 標籤內出現的視覺效果可以使用上一個/下一個來迴圈。</span><span class="sxs-lookup"><span data-stu-id="38b1e-116">If this attribute is set to false, only the visualizations appearing within **EFFECTS** tags can be cycled through using previous/next.</span></span> <span data-ttu-id="38b1e-117">如果設定為 true，則所有在使用者系統上註冊的視覺效果都可以迴圈執行。</span><span class="sxs-lookup"><span data-stu-id="38b1e-117">If it is set to true, then all visualizations that are registered on the user's system can be cycled through.</span></span> <span data-ttu-id="38b1e-118">如果設定為 true，且您在 **效果** 標記內指定任何視覺效果，則會將這些標記中指定的屬性套用至使用者系統上的所有視覺效果。</span><span class="sxs-lookup"><span data-stu-id="38b1e-118">If it is set to true and you specify any visualizations within **EFFECTS** tags, then the attributes specified in these tags are applied to all visualizations on the user's system.</span></span>

## <a name="requirements"></a><span data-ttu-id="38b1e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="38b1e-119">Requirements</span></span>



| <span data-ttu-id="38b1e-120">需求</span><span class="sxs-lookup"><span data-stu-id="38b1e-120">Requirement</span></span> | <span data-ttu-id="38b1e-121">值</span><span class="sxs-lookup"><span data-stu-id="38b1e-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="38b1e-122">版本</span><span class="sxs-lookup"><span data-stu-id="38b1e-122">Version</span></span><br/> | <span data-ttu-id="38b1e-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="38b1e-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38b1e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38b1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b1e-125">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="38b1e-125">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 






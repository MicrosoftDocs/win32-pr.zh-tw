---
title: 效果。 currentEffectType
description: CurrentEffectType 屬性會指定或抓取目前視覺效果的登錄名稱。 這個名稱是視覺效果作者所定義的唯一識別碼。
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- 效果： currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999144"
---
# <a name="effectscurrenteffecttype"></a><span data-ttu-id="f52a3-105">效果。 currentEffectType</span><span class="sxs-lookup"><span data-stu-id="f52a3-105">EFFECTS.currentEffectType</span></span>

<span data-ttu-id="f52a3-106">**CurrentEffectType** 屬性會指定或抓取目前視覺效果的登錄名稱。</span><span class="sxs-lookup"><span data-stu-id="f52a3-106">The **currentEffectType** attribute specifies or retrieves the registry name of the current visualization.</span></span> <span data-ttu-id="f52a3-107">這個名稱是視覺效果作者所定義的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f52a3-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a><span data-ttu-id="f52a3-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="f52a3-108">Possible Values</span></span>

<span data-ttu-id="f52a3-109">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f52a3-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f52a3-110">備註</span><span class="sxs-lookup"><span data-stu-id="f52a3-110">Remarks</span></span>

<span data-ttu-id="f52a3-111">您可以在執行時間使用這個屬性來變更目前顯示的效果。</span><span class="sxs-lookup"><span data-stu-id="f52a3-111">You can use this attribute at run time to change the currently displayed effect.</span></span> <span data-ttu-id="f52a3-112">若要這樣做，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f52a3-112">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="f52a3-113">使用 **effectCount** 來取得已註冊效果的計數。</span><span class="sxs-lookup"><span data-stu-id="f52a3-113">Use **effectCount** to retrieve the count of registered effects.</span></span>
2.  <span data-ttu-id="f52a3-114">在迴圈中，使用 **>effecttype** 取出每個已註冊效果的名稱。</span><span class="sxs-lookup"><span data-stu-id="f52a3-114">In a loop, retrieve the name of each registered effect by using **effectType**.</span></span>
3.  <span data-ttu-id="f52a3-115">指定您為 **currentEffectType** 抓取的其中一個名稱，以設定目前的效果。</span><span class="sxs-lookup"><span data-stu-id="f52a3-115">Specify one of the names you retrieved for **currentEffectType** to set the current effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52a3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f52a3-116">Requirements</span></span>



| <span data-ttu-id="f52a3-117">需求</span><span class="sxs-lookup"><span data-stu-id="f52a3-117">Requirement</span></span> | <span data-ttu-id="f52a3-118">值</span><span class="sxs-lookup"><span data-stu-id="f52a3-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f52a3-119">版本</span><span class="sxs-lookup"><span data-stu-id="f52a3-119">Version</span></span><br/> | <span data-ttu-id="f52a3-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="f52a3-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f52a3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f52a3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52a3-122">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="f52a3-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="f52a3-123">**效果。 currentEffect**</span><span class="sxs-lookup"><span data-stu-id="f52a3-123">**EFFECTS.currentEffect**</span></span>](effects-currenteffect.md)
</dt> <dt>

[<span data-ttu-id="f52a3-124">**效果。 effectCount**</span><span class="sxs-lookup"><span data-stu-id="f52a3-124">**EFFECTS.effectCount**</span></span>](effects-effectcount.md)
</dt> <dt>

[<span data-ttu-id="f52a3-125">**效果。 >effecttype**</span><span class="sxs-lookup"><span data-stu-id="f52a3-125">**EFFECTS.effectType**</span></span>](effects-effecttype.md)
</dt> </dl>

 

 






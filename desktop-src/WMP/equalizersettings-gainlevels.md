---
title: EQUALIZERSETTINGS.gainLevels
description: GainLevels 屬性會指定或抓取對應于所提供之索引的帶狀增益層級。
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS. gainLevels Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977463"
---
# <a name="equalizersettingsgainlevels"></a><span data-ttu-id="a25a1-104">EQUALIZERSETTINGS.gainLevels</span><span class="sxs-lookup"><span data-stu-id="a25a1-104">EQUALIZERSETTINGS.gainLevels</span></span>

<span data-ttu-id="a25a1-105">**GainLevels** 屬性會指定或抓取對應于所提供之索引的帶狀增益層級。</span><span class="sxs-lookup"><span data-stu-id="a25a1-105">The **gainLevels** attribute specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a><span data-ttu-id="a25a1-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="a25a1-106">Possible Values</span></span>

<span data-ttu-id="a25a1-107">這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。</span><span class="sxs-lookup"><span data-stu-id="a25a1-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span>

## <a name="parameters"></a><span data-ttu-id="a25a1-108">參數</span><span class="sxs-lookup"><span data-stu-id="a25a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a25a1-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span><span class="sxs-lookup"><span data-stu-id="a25a1-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span></span>
</dt> <dd>

<span data-ttu-id="a25a1-110">**數位** (**長**) 介於1到10之間，表示帶狀的索引。</span><span class="sxs-lookup"><span data-stu-id="a25a1-110">**Number**(**long**) between 1 and 10 indicating the index of the band.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a25a1-111">備註</span><span class="sxs-lookup"><span data-stu-id="a25a1-111">Remarks</span></span>

<span data-ttu-id="a25a1-112">這個屬性會接受參數，但其值是以與其他屬性值相同的方式，在腳本程式碼中指定。</span><span class="sxs-lookup"><span data-stu-id="a25a1-112">This attribute takes a parameter, but its value is specified in script code the same way as other attribute values.</span></span> <span data-ttu-id="a25a1-113">它不能在 EQUALIZERSETTINGS 元素中指定，也不能與 **wmpprop** 接聽屬性一起使用。</span><span class="sxs-lookup"><span data-stu-id="a25a1-113">It cannot be specified in the EQUALIZERSETTINGS element, nor can it be used with the **wmpprop** listening attribute.</span></span> <span data-ttu-id="a25a1-114">相反地，在這些情況下，會提供編號增益層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="a25a1-114">Instead, the numbered gain level attributes are provided for these situations.</span></span>

## <a name="requirements"></a><span data-ttu-id="a25a1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a25a1-115">Requirements</span></span>



| <span data-ttu-id="a25a1-116">需求</span><span class="sxs-lookup"><span data-stu-id="a25a1-116">Requirement</span></span> | <span data-ttu-id="a25a1-117">值</span><span class="sxs-lookup"><span data-stu-id="a25a1-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a25a1-118">版本</span><span class="sxs-lookup"><span data-stu-id="a25a1-118">Version</span></span><br/> | <span data-ttu-id="a25a1-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="a25a1-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a25a1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a25a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25a1-121">**EQUALIZERSETTINGS 元素**</span><span class="sxs-lookup"><span data-stu-id="a25a1-121">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="a25a1-122">**接聽屬性**</span><span class="sxs-lookup"><span data-stu-id="a25a1-122">**Listening Attributes**</span></span>](listening-attributes.md)
</dt> </dl>

 

 






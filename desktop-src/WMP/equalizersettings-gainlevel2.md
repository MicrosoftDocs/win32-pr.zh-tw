---
title: EQUALIZERSETTINGS.gainLevel2
description: GainLevel2 屬性會指定或抓取寬線2的增益層級。
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- EQUALIZERSETTINGS. gainLevel2 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ca8619f4792b509c5c591c84d547fb7408f747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982531"
---
# <a name="equalizersettingsgainlevel2"></a><span data-ttu-id="25012-104">EQUALIZERSETTINGS.gainLevel2</span><span class="sxs-lookup"><span data-stu-id="25012-104">EQUALIZERSETTINGS.gainLevel2</span></span>

<span data-ttu-id="25012-105">**GainLevel2** 屬性會指定或抓取寬線2的增益層級。</span><span class="sxs-lookup"><span data-stu-id="25012-105">The **gainLevel2** attribute specifies or retrieves the gain level of band 2.</span></span>

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a><span data-ttu-id="25012-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="25012-106">Possible Values</span></span>

<span data-ttu-id="25012-107">這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。</span><span class="sxs-lookup"><span data-stu-id="25012-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span> <span data-ttu-id="25012-108">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="25012-108">It has a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="25012-109">備註</span><span class="sxs-lookup"><span data-stu-id="25012-109">Remarks</span></span>

<span data-ttu-id="25012-110">這個屬性會調整以62Hz 為中心的音訊頻率範圍部分。</span><span class="sxs-lookup"><span data-stu-id="25012-110">This attribute adjusts the portion of the audio frequency spectrum centered on 62Hz.</span></span>

<span data-ttu-id="25012-111">如果未指定此屬性，則會保留先前的值。</span><span class="sxs-lookup"><span data-stu-id="25012-111">If this attribute is not specified, the previous value will be retained.</span></span>

## <a name="requirements"></a><span data-ttu-id="25012-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="25012-112">Requirements</span></span>



| <span data-ttu-id="25012-113">需求</span><span class="sxs-lookup"><span data-stu-id="25012-113">Requirement</span></span> | <span data-ttu-id="25012-114">值</span><span class="sxs-lookup"><span data-stu-id="25012-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="25012-115">版本</span><span class="sxs-lookup"><span data-stu-id="25012-115">Version</span></span><br/> | <span data-ttu-id="25012-116">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="25012-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25012-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25012-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25012-118">**EQUALIZERSETTINGS 元素**</span><span class="sxs-lookup"><span data-stu-id="25012-118">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="25012-119">**EQUALIZERSETTINGS.gainLevels**</span><span class="sxs-lookup"><span data-stu-id="25012-119">**EQUALIZERSETTINGS. gainLevels**</span></span>](equalizersettings-gainlevels.md)
</dt> </dl>

 

 






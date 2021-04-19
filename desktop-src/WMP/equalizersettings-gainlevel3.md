---
title: EQUALIZERSETTINGS.gainLevel3
description: GainLevel3 屬性會指定或抓取寬線3的增益層級。
ms.assetid: 508d00c6-2429-4f35-b7ab-bf30f774e614
keywords:
- EQUALIZERSETTINGS. gainLevel3 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29665777596541f1938360ce057b00c6718d1d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977505"
---
# <a name="equalizersettingsgainlevel3"></a><span data-ttu-id="f1566-104">EQUALIZERSETTINGS.gainLevel3</span><span class="sxs-lookup"><span data-stu-id="f1566-104">EQUALIZERSETTINGS.gainLevel3</span></span>

<span data-ttu-id="f1566-105">**GainLevel3** 屬性會指定或抓取寬線3的增益層級。</span><span class="sxs-lookup"><span data-stu-id="f1566-105">The **gainLevel3** attribute specifies or retrieves the gain level of band 3.</span></span>

``` syntax
        elementID.gainLevel3
```

## <a name="possible-values"></a><span data-ttu-id="f1566-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="f1566-106">Possible Values</span></span>

<span data-ttu-id="f1566-107">這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。</span><span class="sxs-lookup"><span data-stu-id="f1566-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span> <span data-ttu-id="f1566-108">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="f1566-108">It has a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1566-109">備註</span><span class="sxs-lookup"><span data-stu-id="f1566-109">Remarks</span></span>

<span data-ttu-id="f1566-110">這個屬性會調整以125Hz 為中心的音訊頻率範圍部分。</span><span class="sxs-lookup"><span data-stu-id="f1566-110">This attribute adjusts the portion of the audio frequency spectrum centered on 125Hz.</span></span>

<span data-ttu-id="f1566-111">如果未指定此屬性，則會保留先前的值。</span><span class="sxs-lookup"><span data-stu-id="f1566-111">If this attribute is not specified, the previous value will be retained.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1566-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1566-112">Requirements</span></span>



| <span data-ttu-id="f1566-113">需求</span><span class="sxs-lookup"><span data-stu-id="f1566-113">Requirement</span></span> | <span data-ttu-id="f1566-114">值</span><span class="sxs-lookup"><span data-stu-id="f1566-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f1566-115">版本</span><span class="sxs-lookup"><span data-stu-id="f1566-115">Version</span></span><br/> | <span data-ttu-id="f1566-116">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="f1566-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1566-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1566-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1566-118">**EQUALIZERSETTINGS 元素**</span><span class="sxs-lookup"><span data-stu-id="f1566-118">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="f1566-119">**EQUALIZERSETTINGS.gainLevels**</span><span class="sxs-lookup"><span data-stu-id="f1566-119">**EQUALIZERSETTINGS. gainLevels**</span></span>](equalizersettings-gainlevels.md)
</dt> </dl>

 

 






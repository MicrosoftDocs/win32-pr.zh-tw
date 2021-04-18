---
title: EQUALIZERSETTINGS.crossFade
description: CrossFade 屬性會指定或抓取值，指出是否已啟用交叉淡化。
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. crossFade Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996494"
---
# <a name="equalizersettingscrossfade"></a><span data-ttu-id="e5d95-104">EQUALIZERSETTINGS.crossFade</span><span class="sxs-lookup"><span data-stu-id="e5d95-104">EQUALIZERSETTINGS.crossFade</span></span>

<span data-ttu-id="e5d95-105">**CrossFade** 屬性會指定或抓取值，指出是否已啟用交叉淡化。</span><span class="sxs-lookup"><span data-stu-id="e5d95-105">The **crossFade** attribute specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a><span data-ttu-id="e5d95-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="e5d95-106">Possible Values</span></span>

<span data-ttu-id="e5d95-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="e5d95-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="e5d95-108">值</span><span class="sxs-lookup"><span data-stu-id="e5d95-108">Value</span></span> | <span data-ttu-id="e5d95-109">描述</span><span class="sxs-lookup"><span data-stu-id="e5d95-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="e5d95-110">true</span><span class="sxs-lookup"><span data-stu-id="e5d95-110">true</span></span>  | <span data-ttu-id="e5d95-111">啟用交叉淡化。</span><span class="sxs-lookup"><span data-stu-id="e5d95-111">Cross-fade is enabled.</span></span>           |
| <span data-ttu-id="e5d95-112">false</span><span class="sxs-lookup"><span data-stu-id="e5d95-112">false</span></span> | <span data-ttu-id="e5d95-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="e5d95-113">Default.</span></span> <span data-ttu-id="e5d95-114">停用交叉淡化已停用。</span><span class="sxs-lookup"><span data-stu-id="e5d95-114">Cross-fade is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e5d95-115">備註</span><span class="sxs-lookup"><span data-stu-id="e5d95-115">Remarks</span></span>

<span data-ttu-id="e5d95-116">交叉淡化是一種音訊處理功能，它會逐漸減少播放媒體專案結束時的音量，同時在最小磁片區上同時開始播放下一個媒體專案，並逐漸將它逐漸增加到一般磁片區。</span><span class="sxs-lookup"><span data-stu-id="e5d95-116">Cross-fade is an audio processing feature that gradually decreases the volume of one media item near the end of its playback while simultaneously starting playback of the next media item at minimum volume and gradually increasing it to normal volume.</span></span> <span data-ttu-id="e5d95-117">第二個媒體專案開始與第一個媒體專案的結尾之間的重迭，是由 **crossFadeWindow** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="e5d95-117">The overlap between the start of the second media item and the end of the first media item is specified by the **crossFadeWindow** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d95-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5d95-118">Requirements</span></span>



| <span data-ttu-id="e5d95-119">需求</span><span class="sxs-lookup"><span data-stu-id="e5d95-119">Requirement</span></span> | <span data-ttu-id="e5d95-120">值</span><span class="sxs-lookup"><span data-stu-id="e5d95-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e5d95-121">版本</span><span class="sxs-lookup"><span data-stu-id="e5d95-121">Version</span></span><br/> | <span data-ttu-id="e5d95-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e5d95-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5d95-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5d95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d95-124">**EQUALIZERSETTINGS 元素**</span><span class="sxs-lookup"><span data-stu-id="e5d95-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="e5d95-125">**EQUALIZERSETTINGS.crossFadeWindow**</span><span class="sxs-lookup"><span data-stu-id="e5d95-125">**EQUALIZERSETTINGS.crossFadeWindow**</span></span>](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 






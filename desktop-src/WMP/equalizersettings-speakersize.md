---
title: EQUALIZERSETTINGS.speakerSize
description: SpeakerSize 屬性會指定或抓取目前說話者大小的索引編號。
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. speakerSize Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000780"
---
# <a name="equalizersettingsspeakersize"></a><span data-ttu-id="657bc-104">EQUALIZERSETTINGS.speakerSize</span><span class="sxs-lookup"><span data-stu-id="657bc-104">EQUALIZERSETTINGS.speakerSize</span></span>

<span data-ttu-id="657bc-105">**SpeakerSize** 屬性會指定或抓取目前說話者大小的索引編號。</span><span class="sxs-lookup"><span data-stu-id="657bc-105">The **speakerSize** attribute specifies or retrieves the index number of the current speaker size.</span></span>

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a><span data-ttu-id="657bc-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="657bc-106">Possible Values</span></span>

<span data-ttu-id="657bc-107">這個屬性是包含下列其中一個值 (long) 的讀取/寫入 **號碼** 。</span><span class="sxs-lookup"><span data-stu-id="657bc-107">This attribute is a read/write **Number** (long) containing one of the following values.</span></span>



| <span data-ttu-id="657bc-108">值</span><span class="sxs-lookup"><span data-stu-id="657bc-108">Value</span></span> | <span data-ttu-id="657bc-109">描述</span><span class="sxs-lookup"><span data-stu-id="657bc-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="657bc-110">0</span><span class="sxs-lookup"><span data-stu-id="657bc-110">0</span></span>     | <span data-ttu-id="657bc-111">目前的喇叭是耳機。</span><span class="sxs-lookup"><span data-stu-id="657bc-111">The current speakers are headphones.</span></span>     |
| <span data-ttu-id="657bc-112">1</span><span class="sxs-lookup"><span data-stu-id="657bc-112">1</span></span>     | <span data-ttu-id="657bc-113">目前的喇叭是正常的大小。</span><span class="sxs-lookup"><span data-stu-id="657bc-113">The current speakers are of normal size.</span></span> |
| <span data-ttu-id="657bc-114">2</span><span class="sxs-lookup"><span data-stu-id="657bc-114">2</span></span>     | <span data-ttu-id="657bc-115">目前的喇叭很大。</span><span class="sxs-lookup"><span data-stu-id="657bc-115">The current speakers are large.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="657bc-116">備註</span><span class="sxs-lookup"><span data-stu-id="657bc-116">Remarks</span></span>

<span data-ttu-id="657bc-117">您可以使用 **currentSpeakerName** 屬性來取出喇叭大小的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="657bc-117">The friendly name of the speaker size can be retrieved using the **currentSpeakerName** attribute.</span></span>

<span data-ttu-id="657bc-118">如果 **enhancedAudio** 設定為 false，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="657bc-118">This attribute is ignored if **enhancedAudio** is set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="657bc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="657bc-119">Requirements</span></span>



| <span data-ttu-id="657bc-120">需求</span><span class="sxs-lookup"><span data-stu-id="657bc-120">Requirement</span></span> | <span data-ttu-id="657bc-121">值</span><span class="sxs-lookup"><span data-stu-id="657bc-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="657bc-122">版本</span><span class="sxs-lookup"><span data-stu-id="657bc-122">Version</span></span><br/> | <span data-ttu-id="657bc-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="657bc-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="657bc-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="657bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657bc-125">**EQUALIZERSETTINGS 元素**</span><span class="sxs-lookup"><span data-stu-id="657bc-125">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="657bc-126">**EQUALIZERSETTINGS.currentSpeakerName**</span><span class="sxs-lookup"><span data-stu-id="657bc-126">**EQUALIZERSETTINGS.currentSpeakerName**</span></span>](equalizersettings-currentspeakername.md)
</dt> <dt>

[<span data-ttu-id="657bc-127">**EQUALIZERSETTINGS.enhancedAudio**</span><span class="sxs-lookup"><span data-stu-id="657bc-127">**EQUALIZERSETTINGS.enhancedAudio**</span></span>](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 






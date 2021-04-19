---
title: 效果。全螢幕
description: 全螢幕屬性會指定或抓取值，指出目前的視覺效果是否以全螢幕顯示。 這個屬性只能在執行時間設定。
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- 效果。全螢幕 Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990809"
---
# <a name="effectsfullscreen"></a><span data-ttu-id="c271e-105">效果。全螢幕</span><span class="sxs-lookup"><span data-stu-id="c271e-105">EFFECTS.fullScreen</span></span>

<span data-ttu-id="c271e-106">**全** 螢幕屬性會指定或抓取值，指出目前的視覺效果是否以全螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="c271e-106">The **fullScreen** attribute specifies or retrieves a value indicating whether the current visualization is displayed full-screen.</span></span> <span data-ttu-id="c271e-107">這個屬性只能在執行時間設定。</span><span class="sxs-lookup"><span data-stu-id="c271e-107">This attribute can only be set at run time.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="c271e-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="c271e-108">Possible Values</span></span>

<span data-ttu-id="c271e-109">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="c271e-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c271e-110">值</span><span class="sxs-lookup"><span data-stu-id="c271e-110">Value</span></span> | <span data-ttu-id="c271e-111">描述</span><span class="sxs-lookup"><span data-stu-id="c271e-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="c271e-112">true</span><span class="sxs-lookup"><span data-stu-id="c271e-112">true</span></span>  | <span data-ttu-id="c271e-113">視覺效果會以全螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="c271e-113">Visualization is displayed full-screen.</span></span>              |
| <span data-ttu-id="c271e-114">false</span><span class="sxs-lookup"><span data-stu-id="c271e-114">false</span></span> | <span data-ttu-id="c271e-115">預設值。</span><span class="sxs-lookup"><span data-stu-id="c271e-115">Default.</span></span> <span data-ttu-id="c271e-116">視覺效果不會顯示全螢幕。</span><span class="sxs-lookup"><span data-stu-id="c271e-116">Visualization is not displayed full-screen.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c271e-117">備註</span><span class="sxs-lookup"><span data-stu-id="c271e-117">Remarks</span></span>

<span data-ttu-id="c271e-118">只有當媒體現正播放或暫停時，視覺效果才能進入全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="c271e-118">A visualization can be put into full-screen mode only while media is playing or paused.</span></span> <span data-ttu-id="c271e-119">如果 *播放機*。**currentMedia** 是影片，必須有影片外掛程式。</span><span class="sxs-lookup"><span data-stu-id="c271e-119">If *Player*.**currentMedia** is video, a video plug-in must be present.</span></span> <span data-ttu-id="c271e-120">如果是音訊，則必須有支援全螢幕顯示的視覺化外掛程式。</span><span class="sxs-lookup"><span data-stu-id="c271e-120">If it is audio, a visualization plug-in that supports full-screen display must be present.</span></span>

## <a name="requirements"></a><span data-ttu-id="c271e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c271e-121">Requirements</span></span>



| <span data-ttu-id="c271e-122">需求</span><span class="sxs-lookup"><span data-stu-id="c271e-122">Requirement</span></span> | <span data-ttu-id="c271e-123">值</span><span class="sxs-lookup"><span data-stu-id="c271e-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c271e-124">版本</span><span class="sxs-lookup"><span data-stu-id="c271e-124">Version</span></span><br/> | <span data-ttu-id="c271e-125">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c271e-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c271e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c271e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c271e-127">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="c271e-127">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 






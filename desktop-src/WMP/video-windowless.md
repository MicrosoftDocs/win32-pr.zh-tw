---
title: VIDEO。無視窗
description: 無視窗屬性會指定或抓取值，指出影片控制項是否為視窗化或無視窗;也就是說，控制項的整個矩形是否隨時都可以看見，或是可以裁剪。
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDEO：無視窗 Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999353"
---
# <a name="videowindowless"></a><span data-ttu-id="14b3b-104">VIDEO。無視窗</span><span class="sxs-lookup"><span data-stu-id="14b3b-104">VIDEO.windowless</span></span>

<span data-ttu-id="14b3b-105">**無視窗** 屬性會指定或抓取值，指出影片控制項是否為視窗化或無視窗;也就是說，控制項的整個矩形是否隨時都可以看見，或是可以裁剪。</span><span class="sxs-lookup"><span data-stu-id="14b3b-105">The **windowless** attribute specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="14b3b-106">只能在設計階段設定。</span><span class="sxs-lookup"><span data-stu-id="14b3b-106">Can only be set at design time.</span></span>

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a><span data-ttu-id="14b3b-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="14b3b-107">Possible Values</span></span>

<span data-ttu-id="14b3b-108">這個屬性是在設計階段指定的 **布林值** ，之後是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="14b3b-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="14b3b-109">值</span><span class="sxs-lookup"><span data-stu-id="14b3b-109">Value</span></span> | <span data-ttu-id="14b3b-110">描述</span><span class="sxs-lookup"><span data-stu-id="14b3b-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="14b3b-111">true</span><span class="sxs-lookup"><span data-stu-id="14b3b-111">true</span></span>  | <span data-ttu-id="14b3b-112">影片控制項將會是無視窗的。</span><span class="sxs-lookup"><span data-stu-id="14b3b-112">Video control will be windowless.</span></span>        |
| <span data-ttu-id="14b3b-113">false</span><span class="sxs-lookup"><span data-stu-id="14b3b-113">false</span></span> | <span data-ttu-id="14b3b-114">預設值。</span><span class="sxs-lookup"><span data-stu-id="14b3b-114">Default.</span></span> <span data-ttu-id="14b3b-115">影片控制項將會是視窗化。</span><span class="sxs-lookup"><span data-stu-id="14b3b-115">Video control will be windowed.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="14b3b-116">備註</span><span class="sxs-lookup"><span data-stu-id="14b3b-116">Remarks</span></span>

<span data-ttu-id="14b3b-117">如果需要非矩形的影片視窗，或您想要使用影像來涵蓋影片視窗的任何部分，則必須將此屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="14b3b-117">If a non-rectangular video window is desired, or if you want to cover any part of the video window with an image, this attribute must be set to true.</span></span> <span data-ttu-id="14b3b-118">這會犧牲一些執行必要裁剪的效能。</span><span class="sxs-lookup"><span data-stu-id="14b3b-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="14b3b-119">影片播放已針對播放裁剪進行優化。</span><span class="sxs-lookup"><span data-stu-id="14b3b-119">Video playback is optimized for unclipped playback.</span></span> <span data-ttu-id="14b3b-120">在此情況下， **無視窗** 屬性會設定為 false，且一律會顯示整個影片矩形。</span><span class="sxs-lookup"><span data-stu-id="14b3b-120">In this case, the **windowless** attribute is set to false, and the entire video rectangle is always displayed.</span></span> <span data-ttu-id="14b3b-121">會忽略涵蓋影片視窗的任何影像，而影片視窗具有最高層級的迭置順序。</span><span class="sxs-lookup"><span data-stu-id="14b3b-121">Any image covering the video window is ignored, and the video window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b3b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="14b3b-122">Requirements</span></span>



| <span data-ttu-id="14b3b-123">需求</span><span class="sxs-lookup"><span data-stu-id="14b3b-123">Requirement</span></span> | <span data-ttu-id="14b3b-124">值</span><span class="sxs-lookup"><span data-stu-id="14b3b-124">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="14b3b-125">版本</span><span class="sxs-lookup"><span data-stu-id="14b3b-125">Version</span></span><br/> | <span data-ttu-id="14b3b-126">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="14b3b-126">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14b3b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14b3b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b3b-128">**影片元素**</span><span class="sxs-lookup"><span data-stu-id="14b3b-128">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 






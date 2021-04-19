---
title: 影片。縮放
description: Zoom 屬性指定調整影片的百分比。
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. zoom Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000369"
---
# <a name="videozoom"></a><span data-ttu-id="02568-104">影片。縮放</span><span class="sxs-lookup"><span data-stu-id="02568-104">VIDEO.zoom</span></span>

<span data-ttu-id="02568-105">**Zoom** 屬性指定調整影片的百分比。</span><span class="sxs-lookup"><span data-stu-id="02568-105">The **zoom** attribute specifies the percentage by which to scale the video.</span></span>

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a><span data-ttu-id="02568-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="02568-106">Possible Values</span></span>

<span data-ttu-id="02568-107">此屬性是讀取/寫入 **號碼** (**長**) 範圍從1到可由影片控制項的寬度和高度容納的大小上限。</span><span class="sxs-lookup"><span data-stu-id="02568-107">This attribute is a read/write **Number** (**long**) ranging from 1 to the maximum size accommodated by the width and height of the Video control.</span></span> <span data-ttu-id="02568-108">預設值為100。</span><span class="sxs-lookup"><span data-stu-id="02568-108">It has a default value of 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="02568-109">備註</span><span class="sxs-lookup"><span data-stu-id="02568-109">Remarks</span></span>

<span data-ttu-id="02568-110">這個屬性不能與 **全螢幕** 屬性一起使用。</span><span class="sxs-lookup"><span data-stu-id="02568-110">This attribute cannot be used in conjunction with the **fullScreen** attribute.</span></span>

<span data-ttu-id="02568-111">如果指定了 **寬度** 和 **高度** ，而所產生的影片視窗大於播放的影片，則可以藉由相應增加到視窗所容納的大小上限來放大影片。</span><span class="sxs-lookup"><span data-stu-id="02568-111">If **width** and **height** are specified, and the resulting video window is larger than the video being played, the video can be enlarged by scaling up to the maximum size accommodated by the window.</span></span> <span data-ttu-id="02568-112">如果未指定 **寬度** 和 **高度** ，則 **縮放** 範圍會限制為100或更小的值。</span><span class="sxs-lookup"><span data-stu-id="02568-112">If **width** and **height** are not specified, **zoom** is limited to values of 100 or less.</span></span>

<span data-ttu-id="02568-113">如果 **shrinkToFit** 屬性為 false，則影片會在縮放時變更比例，以符合可用空間。</span><span class="sxs-lookup"><span data-stu-id="02568-113">If the **shrinkToFit** property is false, the video will change proportion upon zooming, to fit itself to the available space.</span></span> <span data-ttu-id="02568-114">如果 **shrinkToFit** 為 true，影片將會縮小以符合最嚴格的維度，同時保留其原始比例。</span><span class="sxs-lookup"><span data-stu-id="02568-114">If **shrinkToFit** is true, the video will shrink to fit within the most restrictive dimension, while retaining its original proportions.</span></span>

## <a name="requirements"></a><span data-ttu-id="02568-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="02568-115">Requirements</span></span>



| <span data-ttu-id="02568-116">需求</span><span class="sxs-lookup"><span data-stu-id="02568-116">Requirement</span></span> | <span data-ttu-id="02568-117">值</span><span class="sxs-lookup"><span data-stu-id="02568-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="02568-118">版本</span><span class="sxs-lookup"><span data-stu-id="02568-118">Version</span></span><br/> | <span data-ttu-id="02568-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="02568-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02568-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02568-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02568-121">**影片元素**</span><span class="sxs-lookup"><span data-stu-id="02568-121">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="02568-122">**全螢幕影片**</span><span class="sxs-lookup"><span data-stu-id="02568-122">**VIDEO.fullScreen**</span></span>](video-fullscreen.md)
</dt> <dt>

[<span data-ttu-id="02568-123">**ShrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="02568-123">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> </dl>

 

 






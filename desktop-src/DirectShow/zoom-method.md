---
description: Zoom 方法會放大或縮小影片，並以一組指定的螢幕座標為中心。
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469405"
---
# <a name="zoom-method"></a><span data-ttu-id="a4be7-103">Zoom 方法</span><span class="sxs-lookup"><span data-stu-id="a4be7-103">Zoom Method</span></span>

> [!Note]  
> <span data-ttu-id="a4be7-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a4be7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a4be7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a4be7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a4be7-106">`Zoom`方法會放大或縮小影片，並以一組指定的螢幕座標為中心。</span><span class="sxs-lookup"><span data-stu-id="a4be7-106">The `Zoom` method zooms the video display in or out, centered on a given set of screen coordinates.</span></span>

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a><span data-ttu-id="a4be7-107">參數</span><span class="sxs-lookup"><span data-stu-id="a4be7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4be7-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span><span class="sxs-lookup"><span data-stu-id="a4be7-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span></span>
</dt> <dd>

<span data-ttu-id="a4be7-109">將矩形縮放區域中央的 x 座標指定為整數。</span><span class="sxs-lookup"><span data-stu-id="a4be7-109">Specifies the x-coordinate at the center of the rectangular zoom area as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="a4be7-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span><span class="sxs-lookup"><span data-stu-id="a4be7-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span></span>
</dt> <dd>

<span data-ttu-id="a4be7-111">指定矩形中央的 y 座標，以縮放為整數。</span><span class="sxs-lookup"><span data-stu-id="a4be7-111">Specifies the y-coordinate at the center of the rectangle to be zoomed as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="a4be7-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span><span class="sxs-lookup"><span data-stu-id="a4be7-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span></span>
</dt> <dd>

<span data-ttu-id="a4be7-113">指定以整數形式套用至目前縮放值的放大因數。</span><span class="sxs-lookup"><span data-stu-id="a4be7-113">Specifies the magnification factor applied to the current zoom value as an Integer.</span></span> <span data-ttu-id="a4be7-114">總最大值取決於硬體重迭可支援的內容;這通常是原始大小32到64倍的因素。</span><span class="sxs-lookup"><span data-stu-id="a4be7-114">The total maximum value depends on what the hardware overlay can support; this is typically a factor of 32 to 64 times the original size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4be7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4be7-115">Return Value</span></span>

<span data-ttu-id="a4be7-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a4be7-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4be7-117">備註</span><span class="sxs-lookup"><span data-stu-id="a4be7-117">Remarks</span></span>

<span data-ttu-id="a4be7-118">新的縮放比例會一直有效，直到它還原為原始大小或再次變更為止。</span><span class="sxs-lookup"><span data-stu-id="a4be7-118">The new zoom ratio stays in effect until it is restored to the original size or changed again.</span></span> <span data-ttu-id="a4be7-119">換言之，兩個呼叫這個方法來指定兩個的 *iZoomRatio* ，會導致比原始影片大四倍的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="a4be7-119">In other words, two calls to this method specifying an *iZoomRatio* of two will result in a zoom ratio four times larger than the original video size.</span></span> <span data-ttu-id="a4be7-120">如果使用者嘗試放大超過硬體可支援的範圍，此方法將會成功，但不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="a4be7-120">If the user tries to zoom beyond what the hardware can support, this method will succeed but do nothing.</span></span>

<span data-ttu-id="a4be7-121">[**SetClipVideoRect**](setclipvideorect-method.md)方法是另一種放大的方式;這兩種方法之間的唯一差異在於指定縮放矩形的方式。</span><span class="sxs-lookup"><span data-stu-id="a4be7-121">The [**SetClipVideoRect**](setclipvideorect-method.md) method is another way to zoom in; the only difference between the two methods is the way in which the zoom rectangle is specified.</span></span>

 

 




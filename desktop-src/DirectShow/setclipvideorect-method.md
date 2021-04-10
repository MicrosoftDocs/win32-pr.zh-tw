---
description: SetClipVideoRect 方法會將影片顯示星號調整至指定的 subrectangle。
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: SetClipVideoRect 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687824"
---
# <a name="setclipvideorect-method"></a><span data-ttu-id="fd349-103">SetClipVideoRect 方法</span><span class="sxs-lookup"><span data-stu-id="fd349-103">SetClipVideoRect Method</span></span>

> [!Note]  
> <span data-ttu-id="fd349-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="fd349-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fd349-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fd349-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fd349-106">方法會將 `SetClipVideoRect` 影片顯示星號調整至指定的 subrectangle。</span><span class="sxs-lookup"><span data-stu-id="fd349-106">The `SetClipVideoRect` method zooms the video display to the specified subrectangle.</span></span>

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a><span data-ttu-id="fd349-107">參數</span><span class="sxs-lookup"><span data-stu-id="fd349-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd349-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span><span class="sxs-lookup"><span data-stu-id="fd349-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span></span>
</dt> <dd>

<span data-ttu-id="fd349-109">指定包含裁剪矩形的 [DVDRect](dvdrect-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="fd349-109">Specifies a [DVDRect](dvdrect-object.md) object, which contains the clipping rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd349-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd349-110">Return Value</span></span>

<span data-ttu-id="fd349-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="fd349-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd349-112">備註</span><span class="sxs-lookup"><span data-stu-id="fd349-112">Remarks</span></span>

<span data-ttu-id="fd349-113">當您設定新的裁剪矩形時，物件會將該區域放大，以符合應用程式的整體顯示尺寸。</span><span class="sxs-lookup"><span data-stu-id="fd349-113">When you set a new clipping rectangle, the object enlarges that area to fit within the application's overall display dimensions.</span></span> <span data-ttu-id="fd349-114">這會在螢幕的特定區域中建立效果放大。</span><span class="sxs-lookup"><span data-stu-id="fd349-114">This creates the effect zooming in on a particular area of the screen.</span></span> <span data-ttu-id="fd349-115">若要指定矩形，請建立新的 [DVDRect](dvdrect-object.md) 物件並填入其屬性。</span><span class="sxs-lookup"><span data-stu-id="fd349-115">To specify the rectangle, create a new [DVDRect](dvdrect-object.md) object and fill in its properties.</span></span>

<span data-ttu-id="fd349-116">影片顯示最常見的矩形是 720 x 540。</span><span class="sxs-lookup"><span data-stu-id="fd349-116">The most common rectangle for video display is 720 x 540.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd349-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd349-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd349-118">**GetClipVideoRect**</span><span class="sxs-lookup"><span data-stu-id="fd349-118">**GetClipVideoRect**</span></span>](getclipvideorect-method.md)
</dt> </dl>

 

 




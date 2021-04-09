---
description: PlayForwards 方法會從目前位置開始，以指定的速度向前播放。
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: PlayForwards 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688075"
---
# <a name="playforwards-method"></a><span data-ttu-id="e5bc5-103">PlayForwards 方法</span><span class="sxs-lookup"><span data-stu-id="e5bc5-103">PlayForwards Method</span></span>

> [!Note]  
> <span data-ttu-id="e5bc5-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e5bc5-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e5bc5-106">`PlayForwards`方法會從目前位置開始，以指定的速度向前播放。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-106">The `PlayForwards` method starts forward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="e5bc5-107">參數</span><span class="sxs-lookup"><span data-stu-id="e5bc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5bc5-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="e5bc5-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="e5bc5-109">指定以整數值播放的速度。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-109">Specifies the speed at which to play as an Integer value.</span></span> <span data-ttu-id="e5bc5-110">此值為乘數，1.0 是正常的播放速度;2.0 是雙速度、0.5 為半快，依此類推。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-110">This value is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="e5bc5-111">當 **nSpeed** 不等於1.0 時，會將音訊靜音，並關閉子圖片。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5bc5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5bc5-112">Return Value</span></span>

<span data-ttu-id="e5bc5-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5bc5-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5bc5-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5bc5-115">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="e5bc5-115">**PlayBackwards**</span></span>](playbackwards-method.md)
</dt> </dl>

 

 




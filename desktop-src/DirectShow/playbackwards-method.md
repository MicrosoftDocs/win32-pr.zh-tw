---
description: PlayBackwards 方法會從目前位置開始，以指定的速度向前播放。
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: PlayBackwards 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467410"
---
# <a name="playbackwards-method"></a><span data-ttu-id="dfe9a-103">PlayBackwards 方法</span><span class="sxs-lookup"><span data-stu-id="dfe9a-103">PlayBackwards Method</span></span>

> [!Note]  
> <span data-ttu-id="dfe9a-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dfe9a-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dfe9a-106">`PlayBackwards`方法會從目前位置開始，以指定的速度向前播放。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-106">The `PlayBackwards` method starts backward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="dfe9a-107">參數</span><span class="sxs-lookup"><span data-stu-id="dfe9a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfe9a-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="dfe9a-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="dfe9a-109">指定要以數位的形式播放的速度。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-109">Specifies the speed at which to play as a number.</span></span> <span data-ttu-id="dfe9a-110">這個數位是乘數，1.0 是正常的播放速度;2.0 是雙速度、0.5 為半快，依此類推。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-110">This number is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="dfe9a-111">當 **nSpeed** 不等於1.0 時，會將音訊靜音，並關閉子圖片。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfe9a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfe9a-112">Return Value</span></span>

<span data-ttu-id="dfe9a-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfe9a-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfe9a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe9a-115">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="dfe9a-115">**PlayForwards**</span></span>](playforwards-method.md)
</dt> </dl>

 

 




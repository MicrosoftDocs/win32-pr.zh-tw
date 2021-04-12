---
description: Play 方法會播放目前的 DVD 標題。
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: 'Play 方法 (DirectShow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509985"
---
# <a name="play-method-directshow"></a><span data-ttu-id="e4a51-103">Play 方法 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="e4a51-103">Play Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="e4a51-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e4a51-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e4a51-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e4a51-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e4a51-106">`Play`方法會播放目前的 DVD 標題。</span><span class="sxs-lookup"><span data-stu-id="e4a51-106">The `Play` method plays the current DVD title.</span></span>

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a><span data-ttu-id="e4a51-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4a51-107">Return Value</span></span>

<span data-ttu-id="e4a51-108">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e4a51-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a51-109">備註</span><span class="sxs-lookup"><span data-stu-id="e4a51-109">Remarks</span></span>

<span data-ttu-id="e4a51-110">如果播放暫停或停止，且 [**EnableResetOnStop**](enableresetonstop-property.md) 為 true，則呼叫 **Play** 將會在目前的位置繼續以正常速度播放。</span><span class="sxs-lookup"><span data-stu-id="e4a51-110">If playback is paused or stopped and [**EnableResetOnStop**](enableresetonstop-property.md) is true, then calling **Play** will resume playback at normal speed at the current location.</span></span> <span data-ttu-id="e4a51-111">如果播放已停止，且 **EnableResetOnStop** 為 false，則呼叫 **Play** 將會導致光碟在第一個標題的開頭開始播放。</span><span class="sxs-lookup"><span data-stu-id="e4a51-111">If playback is stopped and **EnableResetOnStop** is false, then calling **Play** will cause the disc to start playing at the beginning of the first title.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4a51-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4a51-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a51-113">**繼續**</span><span class="sxs-lookup"><span data-stu-id="e4a51-113">**Resume**</span></span>](resume-method.md)
</dt> </dl>

 

 




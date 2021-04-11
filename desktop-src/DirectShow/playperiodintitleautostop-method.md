---
description: PlayPeriodInTitleAutoStop 方法會在指定的時間點開始播放指定的標題，直到指定的停止時間為止。
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: PlayPeriodInTitleAutoStop 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846144"
---
# <a name="playperiodintitleautostop-method"></a><span data-ttu-id="78e55-103">PlayPeriodInTitleAutoStop 方法</span><span class="sxs-lookup"><span data-stu-id="78e55-103">PlayPeriodInTitleAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="78e55-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="78e55-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="78e55-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="78e55-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="78e55-106">方法會在指定的 `PlayPeriodInTitleAutoStop` 時間點開始播放指定的標題，直到指定的停止時間為止。</span><span class="sxs-lookup"><span data-stu-id="78e55-106">The `PlayPeriodInTitleAutoStop` method starts playback at the specified time in the specified title until the specified stop time.</span></span>

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a><span data-ttu-id="78e55-107">參數</span><span class="sxs-lookup"><span data-stu-id="78e55-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78e55-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="78e55-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="78e55-109">將標題指定為整數。</span><span class="sxs-lookup"><span data-stu-id="78e55-109">Specifies the title as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="78e55-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span><span class="sxs-lookup"><span data-stu-id="78e55-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span></span>
</dt> <dd>

<span data-ttu-id="78e55-111">將開始時間指定為 "hh： mm： ss： ff" 格式的字串 (指定小時、分鐘、秒、畫面格) 。</span><span class="sxs-lookup"><span data-stu-id="78e55-111">Specifies the start time as a string in "hh:mm:ss:ff" format (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="78e55-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span><span class="sxs-lookup"><span data-stu-id="78e55-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span></span>
</dt> <dd>

<span data-ttu-id="78e55-113">以 "hh： mm： ss： ff" 格式將結束時間指定為字串。</span><span class="sxs-lookup"><span data-stu-id="78e55-113">Specifies the end time as a String in "hh:mm:ss:ff" format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78e55-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="78e55-114">Return Value</span></span>

<span data-ttu-id="78e55-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="78e55-115">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="78e55-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78e55-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e55-117">**PlayChaptersAutoStop**</span><span class="sxs-lookup"><span data-stu-id="78e55-117">**PlayChaptersAutoStop**</span></span>](playchaptersautostop-method.md)
</dt> </dl>

 

 




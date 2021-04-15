---
description: PlayAtTimeInTitle 方法會在指定的標題內開始播放指定的時間。
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: PlayAtTimeInTitle 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467411"
---
# <a name="playattimeintitle-method"></a><span data-ttu-id="221b8-103">PlayAtTimeInTitle 方法</span><span class="sxs-lookup"><span data-stu-id="221b8-103">PlayAtTimeInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="221b8-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="221b8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="221b8-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="221b8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="221b8-106">`PlayAtTimeInTitle`方法會在指定的標題內開始播放指定的時間。</span><span class="sxs-lookup"><span data-stu-id="221b8-106">The `PlayAtTimeInTitle` method starts playback at the specified time within the specified title.</span></span>

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a><span data-ttu-id="221b8-107">參數</span><span class="sxs-lookup"><span data-stu-id="221b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="221b8-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span><span class="sxs-lookup"><span data-stu-id="221b8-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span></span>
</dt> <dd>

<span data-ttu-id="221b8-109">指定開始播放的時間（以字串表示）。</span><span class="sxs-lookup"><span data-stu-id="221b8-109">Specifies the time at which to start playback as a string.</span></span> <span data-ttu-id="221b8-110">字串的格式必須是 "hh： mm： ss： ff" (指定小時、分鐘、秒、畫面格) 。</span><span class="sxs-lookup"><span data-stu-id="221b8-110">The string must be in the format "hh:mm:ss:ff" (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="221b8-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="221b8-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="221b8-112">將標題的索引指定為整數。</span><span class="sxs-lookup"><span data-stu-id="221b8-112">Specifies the index of the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="221b8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="221b8-113">Return Value</span></span>

<span data-ttu-id="221b8-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="221b8-114">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="221b8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="221b8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="221b8-116">**CurrentTitle**</span><span class="sxs-lookup"><span data-stu-id="221b8-116">**CurrentTitle**</span></span>](currenttitle-property.md)
</dt> <dt>

[<span data-ttu-id="221b8-117">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="221b8-117">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="221b8-118">**TitlesAvailable**</span><span class="sxs-lookup"><span data-stu-id="221b8-118">**TitlesAvailable**</span></span>](titlesavailable-property.md)
</dt> </dl>

 

 




---
description: FramesPerSecond 屬性會抓取目前 DVD 標題的影片畫面播放速率。
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: FramesPerSecond 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970688"
---
# <a name="framespersecond-property"></a><span data-ttu-id="69dbf-103">FramesPerSecond 屬性</span><span class="sxs-lookup"><span data-stu-id="69dbf-103">FramesPerSecond Property</span></span>

> [!Note]  
> <span data-ttu-id="69dbf-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="69dbf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="69dbf-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="69dbf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="69dbf-106">屬性會抓取 `FramesPerSecond` 目前 DVD 標題的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="69dbf-106">The `FramesPerSecond` property retrieves the video frame rate for the current DVD title.</span></span>

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a><span data-ttu-id="69dbf-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="69dbf-107">Return Value</span></span>

<span data-ttu-id="69dbf-108">傳回代表影片畫面播放速率的整數值;每秒25或30個畫面格。</span><span class="sxs-lookup"><span data-stu-id="69dbf-108">Returns an integer value representing the video frame rate; either 25 or 30 frames per second.</span></span>

## <a name="remarks"></a><span data-ttu-id="69dbf-109">備註</span><span class="sxs-lookup"><span data-stu-id="69dbf-109">Remarks</span></span>

<span data-ttu-id="69dbf-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="69dbf-110">This property is read-only with no default value.</span></span> <span data-ttu-id="69dbf-111">NTSC 視訊訊號會在每秒30個畫面上顯示。</span><span class="sxs-lookup"><span data-stu-id="69dbf-111">NTSC video signals are displayed at 30 frames per second.</span></span> <span data-ttu-id="69dbf-112">PAL 以每秒25個畫面顯示。</span><span class="sxs-lookup"><span data-stu-id="69dbf-112">PAL is displayed at 25 frames per second.</span></span> <span data-ttu-id="69dbf-113">光碟會編碼為在 NTSC 或 PAL 上播放，但無法在兩者上播放。</span><span class="sxs-lookup"><span data-stu-id="69dbf-113">A disc is encoded to play on either NTSC or PAL, but cannot play on both.</span></span>

 

 




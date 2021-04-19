---
description: StillOff 方法會繼續播放，正在取消仍處於模式。
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: StillOff 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985669"
---
# <a name="stilloff-method"></a><span data-ttu-id="2a6c6-103">StillOff 方法</span><span class="sxs-lookup"><span data-stu-id="2a6c6-103">StillOff Method</span></span>

> [!Note]  
> <span data-ttu-id="2a6c6-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="2a6c6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2a6c6-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="2a6c6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2a6c6-106">`StillOff`方法會繼續播放，正在取消仍處於模式。</span><span class="sxs-lookup"><span data-stu-id="2a6c6-106">The `StillOff` method resumes playback, canceling still mode.</span></span>

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a><span data-ttu-id="2a6c6-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a6c6-107">Return Value</span></span>

<span data-ttu-id="2a6c6-108">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2a6c6-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a6c6-109">備註</span><span class="sxs-lookup"><span data-stu-id="2a6c6-109">Remarks</span></span>

<span data-ttu-id="2a6c6-110">當 [DVD 瀏覽器](dvd-navigator-filter.md) 遇到在光碟上撰寫的靜止畫面時，仍會進入模式。它會傳送 EC \_ DVD \_ 仍 \_ 在事件上，以通知您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2a6c6-110">The [DVD Navigator](dvd-navigator-filter.md) goes into still mode when it encounters a still frame authored on the disc. It notifies your application by sending an EC\_DVD\_STILL\_ON event.</span></span> <span data-ttu-id="2a6c6-111">由於使用者作業的不同，所以仍然模式與 DVD 導覽器處於暫停狀態的不同。</span><span class="sxs-lookup"><span data-stu-id="2a6c6-111">Still mode is different from the DVD Navigator being in a paused state because of a user operation.</span></span> <span data-ttu-id="2a6c6-112">呼叫 `StillOff` 會從仍模式繼續播放，但不會在 DVD 導覽器處於暫停狀態時重新開機。</span><span class="sxs-lookup"><span data-stu-id="2a6c6-112">Calling `StillOff` resumes playback from still mode but does not restart the DVD Navigator when it is in a paused state.</span></span>

 

 




---
description: '[磁片區] 屬性會設定或抓取音訊串流輸出的喇叭音量。'
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512532"
---
# <a name="volume-property"></a><span data-ttu-id="f0e6a-103">Volume 屬性</span><span class="sxs-lookup"><span data-stu-id="f0e6a-103">Volume Property</span></span>

> [!Note]  
> <span data-ttu-id="f0e6a-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f0e6a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f0e6a-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f0e6a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f0e6a-106">`Volume`屬性會設定或抓取音訊串流輸出的喇叭音量。</span><span class="sxs-lookup"><span data-stu-id="f0e6a-106">The `Volume` property sets or retrieves the speaker volume for the audio stream output.</span></span>

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a><span data-ttu-id="f0e6a-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0e6a-107">Return Value</span></span>

<span data-ttu-id="f0e6a-108">將磁片區層級傳回為分貝（以分貝為單位），以做為整數。</span><span class="sxs-lookup"><span data-stu-id="f0e6a-108">Returns the volume level as attenuation in decibels as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0e6a-109">備註</span><span class="sxs-lookup"><span data-stu-id="f0e6a-109">Remarks</span></span>

<span data-ttu-id="f0e6a-110">這個屬性是讀取/寫入，預設值是0。</span><span class="sxs-lookup"><span data-stu-id="f0e6a-110">This property is read/write with a default value of 0.</span></span> <span data-ttu-id="f0e6a-111">完整磁片區為0，而10000為無回應;尺規為對數。</span><span class="sxs-lookup"><span data-stu-id="f0e6a-111">Full volume is 0, and 10,000 is silence; the scale is logarithmic.</span></span> <span data-ttu-id="f0e6a-112">將所需的分貝層級乘以 100 (例如 10000 = 100 dB) 。</span><span class="sxs-lookup"><span data-stu-id="f0e6a-112">Multiply the desired decibel level by 100 (for example 10,000 = 100 dB).</span></span>

 

 




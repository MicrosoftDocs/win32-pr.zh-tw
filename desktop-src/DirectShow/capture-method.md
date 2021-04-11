---
description: 當 MSWebDVD 物件處於無視窗模式時，Capture 方法會從影片框架中捕捉靜止的影像。
ms.assetid: 704e64ef-3593-403c-8ecf-625fb4983882
title: Capture 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db16bbc6ef50de303dbcdac66bd066861bb5811
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108596"
---
# <a name="capture-method"></a><span data-ttu-id="d92c0-103">Capture 方法</span><span class="sxs-lookup"><span data-stu-id="d92c0-103">Capture Method</span></span>

> [!Note]  
> <span data-ttu-id="d92c0-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="d92c0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d92c0-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d92c0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d92c0-106">`Capture`當 MSWebDVD 物件處於無視窗模式時，方法會從影片框架中捕捉靜止影像。</span><span class="sxs-lookup"><span data-stu-id="d92c0-106">The `Capture` method captures a still image from the video frame when the MSWebDVD object is in windowless mode.</span></span>

``` syntax
MSWebDVD.Capture()
```

## <a name="remarks"></a><span data-ttu-id="d92c0-107">備註</span><span class="sxs-lookup"><span data-stu-id="d92c0-107">Remarks</span></span>

<span data-ttu-id="d92c0-108">這個方法會從 DVD-Video 影像中捕捉目前的畫面格，並將其貼入視窗中，讓使用者可以從中儲存或編輯影像。</span><span class="sxs-lookup"><span data-stu-id="d92c0-108">This method captures the current frame from the DVD-Video image and pastes it into a window from which the user can save or edit the image.</span></span> <span data-ttu-id="d92c0-109">MSWebDVD 物件必須處於無視窗模式，此方法才能成功。</span><span class="sxs-lookup"><span data-stu-id="d92c0-109">The MSWebDVD object must be in windowless mode for this method to succeed.</span></span>

 

 




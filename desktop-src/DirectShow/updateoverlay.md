---
description: 當重迭表面已移動或調整大小，或其色彩索引鍵已變更時，就會傳送 UpdateOverlay 事件。
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: 'UpdateOverlay (Ddraw) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990835"
---
# <a name="updateoverlay"></a><span data-ttu-id="94caf-103">UpdateOverlay</span><span class="sxs-lookup"><span data-stu-id="94caf-103">UpdateOverlay</span></span>

> [!Note]  
> <span data-ttu-id="94caf-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="94caf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="94caf-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="94caf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="94caf-106">當重迭表面已移動或調整大小，或其色彩索引鍵已變更時，就會傳送 **UpdateOverlay** 事件。</span><span class="sxs-lookup"><span data-stu-id="94caf-106">The **UpdateOverlay** event is sent when the overlay surface has been moved or resized or its color key has changed.</span></span>

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a><span data-ttu-id="94caf-107">備註</span><span class="sxs-lookup"><span data-stu-id="94caf-107">Remarks</span></span>

<span data-ttu-id="94caf-108">應用程式永遠不會擔心調整大小或移動的重迭表面。</span><span class="sxs-lookup"><span data-stu-id="94caf-108">Applications should never be concerned about the overlay surface being resized or moved.</span></span> <span data-ttu-id="94caf-109">這是在內部處理。</span><span class="sxs-lookup"><span data-stu-id="94caf-109">This is all handled internally.</span></span> <span data-ttu-id="94caf-110">但是，當顏色按鍵變更時，也會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="94caf-110">But this event is also sent when the color key changes.</span></span> <span data-ttu-id="94caf-111">這表示，如果應用程式將 MSWebDVD 裝載為無視窗控制項，並在全螢幕模式下的影片表面上顯示浮動按鈕，則應該取得 **>colorkey** 屬性的新值，讓它可以正確地繪製按鈕，以回應此事件。</span><span class="sxs-lookup"><span data-stu-id="94caf-111">That means that if an application is hosting MSWebDVD as a windowless control and displaying floating buttons on top of the video surface in full-screen mode, it should respond to this event by getting the new value of the **ColorKey** property so that it can draw the buttons properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="94caf-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="94caf-112">Requirements</span></span>



| <span data-ttu-id="94caf-113">需求</span><span class="sxs-lookup"><span data-stu-id="94caf-113">Requirement</span></span> | <span data-ttu-id="94caf-114">值</span><span class="sxs-lookup"><span data-stu-id="94caf-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94caf-115">標頭</span><span class="sxs-lookup"><span data-stu-id="94caf-115">Header</span></span><br/> | <dl> <span data-ttu-id="94caf-116"><dt>Ddraw。h</dt></span><span class="sxs-lookup"><span data-stu-id="94caf-116"><dt>Ddraw.h</dt></span></span> </dl> |



 

 





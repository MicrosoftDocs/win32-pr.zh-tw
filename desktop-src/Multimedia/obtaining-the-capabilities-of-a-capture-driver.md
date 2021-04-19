---
title: 取得 Capture 驅動程式的功能
description: 取得 Capture 驅動程式的功能
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- WM_CAP_DRIVER_GET_CAPS 訊息
- capDriverGetCaps 宏
- CAPDRIVERCAPS 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969488"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a><span data-ttu-id="412fe-106">取得 Capture 驅動程式的功能</span><span class="sxs-lookup"><span data-stu-id="412fe-106">Obtaining the Capabilities of a Capture Driver</span></span>

<span data-ttu-id="412fe-107">[**WM \_ cap \_ 驅動程式 \_ 取得 \_ cap**](wm-cap-driver-get-caps.md)訊息會傳回 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構中的 capture 驅動程式和基礎硬體的功能。</span><span class="sxs-lookup"><span data-stu-id="412fe-107">The [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span> <span data-ttu-id="412fe-108">每次應用程式將新的捕獲驅動程式連接到 [捕獲] 視窗時，就應該更新 **CAPDRIVERCAPS** 結構。</span><span class="sxs-lookup"><span data-stu-id="412fe-108">Each time an application connects a new capture driver to the capture window, it should update the **CAPDRIVERCAPS** structure.</span></span> <span data-ttu-id="412fe-109">下列範例會使用 [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) 宏來取得 capture 驅動程式功能。</span><span class="sxs-lookup"><span data-stu-id="412fe-109">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to obtain the capture driver capabilities.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a><span data-ttu-id="412fe-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="412fe-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="412fe-111">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="412fe-111">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 





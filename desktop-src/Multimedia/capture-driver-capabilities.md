---
title: Capture 驅動程式功能
description: Capture 驅動程式功能
ms.assetid: 6e74635e-9dac-419d-a264-08fee04ae7b7
keywords:
- WM_CAP_DRIVER_GET_CAPS 訊息
- capDriverGetCaps 宏
- CAPDRIVERCAPS 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87fb4f9cb439229721b6c10aa6207af601f9ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021048"
---
# <a name="capture-driver-capabilities"></a><span data-ttu-id="c5b79-106">Capture 驅動程式功能</span><span class="sxs-lookup"><span data-stu-id="c5b79-106">Capture Driver Capabilities</span></span>

<span data-ttu-id="c5b79-107">您可以使用 [ [**WM \_ cap \_ 驅動程式 \_ 取得 \_ cap**](wm-cap-driver-get-caps.md) 訊息 (] 或 [ [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) 宏) ，來取得目前連線的捕獲驅動程式的硬體功能。</span><span class="sxs-lookup"><span data-stu-id="c5b79-107">You can retrieve the hardware capabilities of the currently connected capture driver by using the [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message (or the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro).</span></span> <span data-ttu-id="c5b79-108">這則訊息會傳回 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) 結構中的 capture 驅動程式和基礎硬體的功能。</span><span class="sxs-lookup"><span data-stu-id="c5b79-108">This message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

 

 





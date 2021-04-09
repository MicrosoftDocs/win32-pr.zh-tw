---
title: 捕捉速率
description: 捕捉速率
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- CAPTUREPARMS 結構
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021449"
---
# <a name="capture-rate"></a><span data-ttu-id="993c4-108">捕捉速率</span><span class="sxs-lookup"><span data-stu-id="993c4-108">Capture Rate</span></span>

<span data-ttu-id="993c4-109">「捕獲速率」是每秒在捕獲會話中所捕獲的框架數目。</span><span class="sxs-lookup"><span data-stu-id="993c4-109">The capture rate is the number of frames that are captured each second of a capture session.</span></span> <span data-ttu-id="993c4-110">您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得目前的捕獲速度。</span><span class="sxs-lookup"><span data-stu-id="993c4-110">You can retrieve the current capture rate by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="993c4-111">目前的捕獲速率會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **dwRequestMicroSecPerFrame** 成員中。</span><span class="sxs-lookup"><span data-stu-id="993c4-111">The current capture rate is stored in the **dwRequestMicroSecPerFrame** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="993c4-112">您可以藉由指定連續框架與此成員的值之間的微秒數來設定捕捉速率，然後使用 [ [**WM \_ CAP \_ set \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ] 宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="993c4-112">You can set the capture rate by specifying the number of microseconds between successive frames as the value of this member, then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="993c4-113">**DwRequestMicroSecPerFrame** 的預設值是66667，對應至每秒15個畫面格。</span><span class="sxs-lookup"><span data-stu-id="993c4-113">The default value of **dwRequestMicroSecPerFrame** is 66667, which corresponds to 15 frames per second.</span></span>

 

 





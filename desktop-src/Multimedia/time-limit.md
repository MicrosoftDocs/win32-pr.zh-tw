---
title: 時間限制
description: 時間限制
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- CAPTUREPARMS 結構
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- CAPTUREPARMS 結構
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675827"
---
# <a name="time-limit"></a><span data-ttu-id="612b7-109">時間限制</span><span class="sxs-lookup"><span data-stu-id="612b7-109">Time Limit</span></span>

<span data-ttu-id="612b7-110">您可以使用 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fLimitEnabled** 和 **wTimeLimit** 成員來限制捕捉作業的持續時間。</span><span class="sxs-lookup"><span data-stu-id="612b7-110">You can limit the duration of a capture operation by using the **fLimitEnabled** and **wTimeLimit** members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="612b7-111">**FLimitEnabled** 成員會指出是否要計時捕捉作業，而 **wTimeLimit** 則會指定捕捉作業的最長持續時間。</span><span class="sxs-lookup"><span data-stu-id="612b7-111">The **fLimitEnabled** member indicates whether the capture operation is to be timed, while **wTimeLimit** specifies the maximum duration of the capture operation.</span></span>

<span data-ttu-id="612b7-112">您可以使用 **fLimitEnabled** 和 **wTimeLimit** 的值，方法是使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="612b7-112">You can retrieve the values for **fLimitEnabled** and **wTimeLimit** by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="612b7-113">您可以藉由指定 **TRUE** 作為 **fLimitEnabled** 的值來啟用捕捉作業的計時器，也可以指定 **wTimeLimit** 的值（以秒為單位）來設定捕捉作業的持續時間。</span><span class="sxs-lookup"><span data-stu-id="612b7-113">You can enable a timer for the capture operation by specifying **TRUE** as the value of **fLimitEnabled**, or you can set the duration of the capture operation by specifying a value, in seconds, for **wTimeLimit**.</span></span> <span data-ttu-id="612b7-114">設定這些成員之後，請使用 [ [**WM \_ CAP \_ set \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md) message (或 [**CapCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="612b7-114">After you set these members, send the updated [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="612b7-115">**FLimitEnabled** 的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="612b7-115">The default value of **fLimitEnabled** is **FALSE**.</span></span>

 

 





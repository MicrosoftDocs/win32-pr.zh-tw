---
title: 影片捕獲設定
description: 影片捕獲設定
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- CAPTUREPARMS 結構
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967405"
---
# <a name="video-capture-settings"></a><span data-ttu-id="030c5-108">影片捕獲設定</span><span class="sxs-lookup"><span data-stu-id="030c5-108">Video Capture Settings</span></span>

<span data-ttu-id="030c5-109">[**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構包含串流處理影片捕獲的控制項參數。</span><span class="sxs-lookup"><span data-stu-id="030c5-109">The [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure contains the control parameters for streaming video capture.</span></span> <span data-ttu-id="030c5-110">此結構可控制捕捉程式的幾個層面，並可讓您執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="030c5-110">This structure controls several aspects of the capture process, and allows you to perform the following tasks:</span></span>

-   <span data-ttu-id="030c5-111">指定畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="030c5-111">Specify the frame rate.</span></span>
-   <span data-ttu-id="030c5-112">指定已配置的影片緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="030c5-112">Specify the number of allocated video buffers.</span></span>
-   <span data-ttu-id="030c5-113">停用並啟用音訊捕獲。</span><span class="sxs-lookup"><span data-stu-id="030c5-113">Disable and enable audio capture.</span></span>
-   <span data-ttu-id="030c5-114">指定 capture 的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="030c5-114">Specify the time interval for the capture.</span></span>
-   <span data-ttu-id="030c5-115">指定是否在捕獲期間使用 MCI 裝置 (VCR 或 videodisc) 。</span><span class="sxs-lookup"><span data-stu-id="030c5-115">Specify whether an MCI device (VCR or videodisc) is used during capture.</span></span>
-   <span data-ttu-id="030c5-116">指定用於結束資料流程的鍵盤或滑鼠控制項。</span><span class="sxs-lookup"><span data-stu-id="030c5-116">Specify keyboard or mouse control for ending streaming.</span></span>
-   <span data-ttu-id="030c5-117">指定在捕捉期間套用的最平均影片類型。</span><span class="sxs-lookup"><span data-stu-id="030c5-117">Specify the type of video averaging applied during capture.</span></span>

<span data-ttu-id="030c5-118">您可以在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構中取出目前的捕獲設定，方法是將 [**WM \_ CAP \_ GET \_ SEQUENCE \_ 安裝**](wm-cap-get-sequence-setup.md) 訊息 (或 [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) 傳送至 capture 視窗。</span><span class="sxs-lookup"><span data-stu-id="030c5-118">You can retrieve the current capture settings within the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure by sending the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro) to a capture window.</span></span> <span data-ttu-id="030c5-119">您可以設定一或多個目前的捕獲設定，方法是更新 **CAPTUREPARMS** 結構的適當成員，然後將 [**WM \_ CAP \_ set \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md) 訊息 (或 [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) 宏) 和 **CAPTUREPARMS** 傳送至 [capture] 視窗。</span><span class="sxs-lookup"><span data-stu-id="030c5-119">You can set one or more current capture settings by updating the appropriate members of the **CAPTUREPARMS** structure and then sending the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro) and **CAPTUREPARMS** to a capture window.</span></span>

 

 





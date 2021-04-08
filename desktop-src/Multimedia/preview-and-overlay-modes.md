---
title: 預覽和重迭模式
description: 預覽和重迭模式
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW 訊息
- capPreview 宏
- WM_CAP_SET_PREVIEWRATE 訊息
- capPreviewRate 宏
- WM_CAP_SET_SCALE 訊息
- capPreviewScale 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932101"
---
# <a name="preview-and-overlay-modes"></a><span data-ttu-id="0b149-109">預覽和重迭模式</span><span class="sxs-lookup"><span data-stu-id="0b149-109">Preview and Overlay Modes</span></span>

<span data-ttu-id="0b149-110">Capture 驅動程式可執行兩種方法來觀看內送影片串流：預覽模式和重迭模式。</span><span class="sxs-lookup"><span data-stu-id="0b149-110">A capture driver can implement two methods for viewing an incoming video stream: preview mode and overlay mode.</span></span> <span data-ttu-id="0b149-111">如果捕捉驅動程式同時執行這兩種方法，則使用者可以選擇要使用的方法。</span><span class="sxs-lookup"><span data-stu-id="0b149-111">If a capture driver implements both methods, the user can choose which method to use.</span></span>

<span data-ttu-id="0b149-112">[預覽] 模式會將數位化的框架從捕獲硬體傳輸到系統記憶體，然後使用圖形裝置介面 (GDI) 函式，在 [捕捉] 視窗中顯示數位化的框架。</span><span class="sxs-lookup"><span data-stu-id="0b149-112">Preview mode transfers digitized frames from the capture hardware to system memory and then displays the digitized frames in the capture window by using graphics device interface (GDI) functions.</span></span> <span data-ttu-id="0b149-113">當父視窗失去焦點時，應用程式可能會降低預覽率，並在父視窗取得焦點時增加預覽率。</span><span class="sxs-lookup"><span data-stu-id="0b149-113">Applications might decrease the preview rate when the parent window loses focus, and increase the preview rate when the parent window gains focus.</span></span> <span data-ttu-id="0b149-114">此動作可改善一般系統回應性，因為預覽作業需要大量處理器。</span><span class="sxs-lookup"><span data-stu-id="0b149-114">This action improves general system responsiveness because the preview operation is processor intensive.</span></span>

<span data-ttu-id="0b149-115">有三個訊息可控制預覽作業。</span><span class="sxs-lookup"><span data-stu-id="0b149-115">There are three messages to control the preview operation.</span></span>

-   <span data-ttu-id="0b149-116">若要啟用或停用 [預覽] 模式，請 [**透過將 (\_ \_ \_**](wm-cap-set-preview.md) 或 [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) 宏) 傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="0b149-116">Use the [**WM\_CAP\_SET\_PREVIEW**](wm-cap-set-preview.md) message to enable or disable preview mode by sending the (or the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro) to a capture window.</span></span>
-   <span data-ttu-id="0b149-117">使用 [**WM \_ CAP \_ SET \_ PREVIEWRATE**](wm-cap-set-previewrate.md) message (或 [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) 宏) 來設定在預覽模式中顯示畫面格的速率</span><span class="sxs-lookup"><span data-stu-id="0b149-117">Use the [**WM\_CAP\_SET\_PREVIEWRATE**](wm-cap-set-previewrate.md) message (or the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro) to set the rate at which frames are displayed in preview mode</span></span>
-   <span data-ttu-id="0b149-118">使用「 [**WM \_ CAP \_ 集 \_ 調整**](wm-cap-set-scale.md) 訊息 (或 [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) 宏) 來啟用或停用預覽版影片的縮放。</span><span class="sxs-lookup"><span data-stu-id="0b149-118">Use the [**WM\_CAP\_SET\_SCALE**](wm-cap-set-scale.md) message (or the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro) to enable or disable scaling of the preview video.</span></span>

<span data-ttu-id="0b149-119">如果同時啟用預覽和調整，則會將捕獲的影片畫面延展至 [捕捉] 視窗的維度。</span><span class="sxs-lookup"><span data-stu-id="0b149-119">When preview and scaling are both enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="0b149-120">啟用預覽模式會自動停用覆迭模式。</span><span class="sxs-lookup"><span data-stu-id="0b149-120">Enabling preview mode automatically disables overlay mode.</span></span>

<span data-ttu-id="0b149-121">覆迭模式是一種硬體功能，會在不使用 CPU 資源的情況下，顯示監視器上的擷取緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="0b149-121">Overlay mode is a hardware function that displays the contents of the capture buffer on the monitor without using CPU resources.</span></span> <span data-ttu-id="0b149-122">您可以藉由將 [**WM \_ CAP \_ 集合 \_**](wm-cap-set-overlay.md) 重迭訊息 (或 [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) 宏) 傳送至 [捕獲] 視窗，來啟用和停用覆迭模式。</span><span class="sxs-lookup"><span data-stu-id="0b149-122">You can enable and disable overlay mode by sending the [**WM\_CAP\_SET\_OVERLAY**](wm-cap-set-overlay.md) message (or the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro) to a capture window.</span></span> <span data-ttu-id="0b149-123">啟用覆迭模式會自動停用預覽模式。</span><span class="sxs-lookup"><span data-stu-id="0b149-123">Enabling overlay mode automatically disables preview mode.</span></span>

<span data-ttu-id="0b149-124">您也可以在 [預覽] 模式或 [覆迭模式] 的 [捕捉] 視窗的工作區中，將 [ [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos)宏) 傳送至 [捕獲] 視窗，以設定影片框架的滾動 [**(條位置 \_ \_ \_**](wm-cap-set-scroll.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b149-124">You can also set the scroll position of the video frame within the client area of the capture window for preview mode or overlay mode by sending the [**WM\_CAP\_SET\_SCROLL**](wm-cap-set-scroll.md) message (or the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro) to a capture window.</span></span>

 

 





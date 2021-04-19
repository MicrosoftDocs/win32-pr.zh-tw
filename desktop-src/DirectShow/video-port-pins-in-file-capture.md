---
description: 檔案捕捉中的影片埠 Pin
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: 檔案捕捉中的影片埠 Pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996629"
---
# <a name="video-port-pins-in-file-capture"></a><span data-ttu-id="7943d-103">檔案捕捉中的影片埠 Pin</span><span class="sxs-lookup"><span data-stu-id="7943d-103">Video Port Pins in File Capture</span></span>

<span data-ttu-id="7943d-104">如果捕捉裝置有影片埠，則即使您只想要捕捉至檔案，影片埠 pin 也必須連接到影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="7943d-104">If the capture device has a video port, the video port pin must be connected to a video renderer, even if you only want to capture to a file.</span></span>

<span data-ttu-id="7943d-105">如果您使用值 **釘選 \_ 類別 \_ 捕獲** 來呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，且裝置有影片埠 pin，則「捕獲圖形產生器」會自動將影片埠 pin 連接至重迭 [混音](overlay-mixer-filter.md)器篩選器，並將覆迭混音器連接至影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="7943d-105">If you call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the value **PIN\_CATEGORY\_CAPTURE** and the device has a video port pin, the Capture Graph Builder automatically connects the video port pin to the [Overlay Mixer](overlay-mixer-filter.md) filter and connects the Overlay Mixer to the Video Renderer.</span></span> <span data-ttu-id="7943d-106">「捕獲圖形產生器」會藉由呼叫 [**IVideoWindow：:p [ \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) **OAFALSE**] 來顯示值，以隱藏影片視窗。</span><span class="sxs-lookup"><span data-stu-id="7943d-106">The Capture Graph Builder hides the video window by calling [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value **OAFALSE**.</span></span> <span data-ttu-id="7943d-107">如果應用程式稍後以釘選 **\_ 類別 \_ 預覽** 來呼叫 **RenderStream** ，「捕獲圖形產生器」會呼叫 **put \_ ，** 並顯示值 OATRUE，以便顯示影片視窗。</span><span class="sxs-lookup"><span data-stu-id="7943d-107">If the application later calls **RenderStream** with **PIN\_CATEGORY\_PREVIEW**, the Capture Graph Builder calls **put\_AutoShow** with the value **OATRUE**, in order to show the video window.</span></span>

<span data-ttu-id="7943d-108">使用 **PIN \_ 類別 \_ 捕獲** 來呼叫 **RenderStream** 之後，您可以藉由查詢 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)介面的篩選圖形管理員來檢查它是否已新增影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="7943d-108">After you call **RenderStream** with **PIN\_CATEGORY\_CAPTURE**, you can check whether it has added the Video Renderer by querying the Filter Graph Manager for the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7943d-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="7943d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7943d-110">將影片捕獲至檔案</span><span class="sxs-lookup"><span data-stu-id="7943d-110">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 




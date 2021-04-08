---
title: 手動畫面格捕獲
description: 手動畫面格捕獲
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- WM_CAP_SINGLE_FRAME_OPEN 訊息
- WM_CAP_SINGLE_FRAME 訊息
- WM_CAP_SINGLE_FRAME_CLOSE 訊息
- capCaptureSingleFrameOpen 宏
- capCaptureSingleFrame 宏
- capCaptureSingleFrameClose 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839751"
---
# <a name="manual-frame-capture"></a><span data-ttu-id="97165-109">手動畫面格捕獲</span><span class="sxs-lookup"><span data-stu-id="97165-109">Manual Frame Capture</span></span>

<span data-ttu-id="97165-110">如果您想要個別指定要在影片串流中捕捉的框架，您可以使用「 [**wm」 \_ \_ 單一 \_ 畫面格 \_ 開啟**](wm-cap-single-frame-open.md)、 [**WM \_ cap \_ 單一 \_ 框架**](wm-cap-single-frame.md)，以及「 [**wm 端點」 \_ \_ 單一 \_ 框架 \_ 關閉**](wm-cap-single-frame-close.md) 訊息 (或 [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen)、 [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)和 [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) 宏) 來控制序列。</span><span class="sxs-lookup"><span data-stu-id="97165-110">If you want to individually specify the frames to capture in a video stream, you can control the sequence by using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md), [**WM\_CAP\_SINGLE\_FRAME**](wm-cap-single-frame.md), and [**WM\_CAP\_SINGLE\_FRAME\_CLOSE**](wm-cap-single-frame-close.md) messages (or the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe), and [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macros).</span></span> <span data-ttu-id="97165-111">一般而言，這些訊息是用來建立動畫，方法是將個別的框架附加至 capture 檔案。</span><span class="sxs-lookup"><span data-stu-id="97165-111">Typically, these messages are used to create animation by appending individual frames to the capture file.</span></span> <span data-ttu-id="97165-112">[WM \_ CAP \_ 單一畫面格開啟] 會開啟檔案 \_ \_ 以進行手動驅動的捕獲操作。</span><span class="sxs-lookup"><span data-stu-id="97165-112">WM\_CAP\_SINGLE\_FRAME\_OPEN opens a file for a manually driven capture operation.</span></span> <span data-ttu-id="97165-113">WM \_ CAP \_ 單一 \_ 畫面格會捕捉個別的畫面格，並將其附加至 capture 檔案。</span><span class="sxs-lookup"><span data-stu-id="97165-113">WM\_CAP\_SINGLE\_FRAME captures an individual frame and appends it to the capture file.</span></span> <span data-ttu-id="97165-114">WM \_ CAP \_ 單一 \_ 畫面格 \_ 關閉會關閉手動畫面格捕獲所用的檔案。</span><span class="sxs-lookup"><span data-stu-id="97165-114">WM\_CAP\_SINGLE\_FRAME\_CLOSE closes the file used for manual frame capture.</span></span>

> [!Note]  
> <span data-ttu-id="97165-115">此捕捉方法不支援使用影片捕獲同時進行音訊捕獲。</span><span class="sxs-lookup"><span data-stu-id="97165-115">This capture method does not support simultaneous audio capture with video capture.</span></span>

 

 

 





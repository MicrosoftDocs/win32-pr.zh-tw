---
title: 自訂檔案和串流處理常式
description: 自訂檔案和串流處理常式
ms.assetid: c61e0118-d405-4c1e-9ae8-ed6a145a5d6b
keywords:
- Windows (VFW) 自訂檔案處理常式的影片
- Windows (VFW) 、自訂串流處理常式的影片
- Windows (VFW) 的影片，檔處理常式
- 適用于 Windows (VFW) 、串流處理常式的影片
- 適用于 Windows) 、自訂檔案處理常式的 VFW (影片
- 適用于 Windows) 、自訂串流處理常式的 VFW (影片
- 適用于 Windows) 的 VFW (影片，檔處理常式
- 適用于 Windows) 、串流處理常式的 VFW (影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f991ac3197eb6d2f23fcd20d0d14e5f7c65e48de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462293"
---
# <a name="custom-file-and-stream-handlers"></a><span data-ttu-id="e3dea-111">自訂檔案和串流處理常式</span><span class="sxs-lookup"><span data-stu-id="e3dea-111">Custom File and Stream Handlers</span></span>

<span data-ttu-id="e3dea-112">檔案和串流處理常式是為控制多媒體資料的應用程式提供一致介面的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e3dea-112">File and stream handlers are drivers that provide consistent interfaces to an application that controls multimedia data.</span></span> <span data-ttu-id="e3dea-113">作業系統中所含的檔案和串流處理常式會使用影片和波形音訊資料，並以音訊顯示 (AVI) 和波形音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="e3dea-113">The file and stream handlers included in the operating system use video and waveform-audio data stored in audio-video interleaved (AVI) and waveform-audio files.</span></span>

<span data-ttu-id="e3dea-114">您可以撰寫處理常式，以允許您的應用程式寫入或存取另一個來源的多媒體資料，例如使用專屬格式的檔案、已擴充為包含其他資料流程的 AVI 檔案，或是產生它自己的多媒體資料的處理常式。</span><span class="sxs-lookup"><span data-stu-id="e3dea-114">You can write handlers to allow your application to write or access multimedia data from another source, such as a file using a proprietary format, an AVI file that has been expanded to contain additional data streams, or a handler that generates its own multimedia data.</span></span> <span data-ttu-id="e3dea-115">如果您有想要搭配 AVIFile 函式 [和宏](avifile-functions-and-macros.md)使用之 AVI 資料的自訂檔案格式，則需要撰寫自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="e3dea-115">If you have a custom file format for AVI data that you would like to use with the [AVIFile Functions and Macros](avifile-functions-and-macros.md), you need to write a custom handler.</span></span>

-   [<span data-ttu-id="e3dea-116">關於自訂檔案和串流處理常式</span><span class="sxs-lookup"><span data-stu-id="e3dea-116">About Custom File and Stream Handlers</span></span>](about-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="e3dea-117">使用自訂檔案和串流處理常式</span><span class="sxs-lookup"><span data-stu-id="e3dea-117">Using Custom File and Stream Handlers</span></span>](using-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="e3dea-118">自訂檔案和資料流程處理常式參考</span><span class="sxs-lookup"><span data-stu-id="e3dea-118">Custom File and Stream Handler Reference</span></span>](custom-file-and-stream-handler-reference.md)

 

 





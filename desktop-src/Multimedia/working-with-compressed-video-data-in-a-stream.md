---
title: 在資料流程中使用壓縮的影片資料
description: 在資料流程中使用壓縮的影片資料
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023370"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a><span data-ttu-id="a5db5-103">在資料流程中使用壓縮的影片資料</span><span class="sxs-lookup"><span data-stu-id="a5db5-103">Working with Compressed Video Data in a Stream</span></span>

<span data-ttu-id="a5db5-104">AVIFile 提供數種方式讓您存取壓縮的影片串流。</span><span class="sxs-lookup"><span data-stu-id="a5db5-104">AVIFile provides several ways for you to access compressed video streams.</span></span>

<span data-ttu-id="a5db5-105">如果您想要顯示一或多個已壓縮影片資料流程的框架，您可以使用 [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) 函式來取出框架，然後將壓縮的框架資料轉送至 DrawDib 函式來顯示它們。</span><span class="sxs-lookup"><span data-stu-id="a5db5-105">If you want to display one or more frames of a compressed video stream, you can retrieve the frames by using the [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) function and forwarding the compressed frame data to DrawDib functions to display them.</span></span> <span data-ttu-id="a5db5-106">DrawDib 函式可以顯示數個影像深度的影像，並自動顯示無法處理特定類型的裝置獨立點陣圖 (Dib) 的顯示器影像。</span><span class="sxs-lookup"><span data-stu-id="a5db5-106">DrawDib functions can display images of several image depths and automatically dither images for displays that cannot handle certain types of device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="a5db5-107">這些函式適用于未壓縮和壓縮的影像。</span><span class="sxs-lookup"><span data-stu-id="a5db5-107">These functions work with uncompressed and compressed images.</span></span> <span data-ttu-id="a5db5-108">如需 DrawDib 函數的詳細資訊，請參閱 [DrawDib 函數](drawdib-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="a5db5-108">For more information about DrawDib functions, see [DrawDib Functions](drawdib-functions.md).</span></span>

<span data-ttu-id="a5db5-109">AVIFile 提供可解壓縮單一影片框架的函式。</span><span class="sxs-lookup"><span data-stu-id="a5db5-109">AVIFile provides functions for decompressing a single video frame.</span></span> <span data-ttu-id="a5db5-110">若要配置資源，請使用 [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) 函數。</span><span class="sxs-lookup"><span data-stu-id="a5db5-110">To allocate resources, use the [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) function.</span></span> <span data-ttu-id="a5db5-111">此函數會建立解壓縮資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a5db5-111">This function creates a buffer for the decompressed data.</span></span>

<span data-ttu-id="a5db5-112">您可以使用 [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) 函式來解壓縮單一的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="a5db5-112">You can decompress a single video frame by using the [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) function.</span></span> <span data-ttu-id="a5db5-113">此函式會將框架解壓縮，並抓取影像資料的完整框架，以傳回 [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) 結構中的 DIB 位址。</span><span class="sxs-lookup"><span data-stu-id="a5db5-113">This function decompresses the frame and retrieves a complete frame of image data, returning the address of the DIB in the [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) structure.</span></span> <span data-ttu-id="a5db5-114">您的應用程式可以使用標準繪圖函數或使用 DrawDib 函式來顯示 DIB。</span><span class="sxs-lookup"><span data-stu-id="a5db5-114">Your application can display the DIB by using standard drawing functions or by using the DrawDib functions.</span></span>

<span data-ttu-id="a5db5-115">如果您的應用程式會連續呼叫 **AVIStreamGetFrame**，函式會將每個抓取的框架覆寫緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a5db5-115">If your application makes successive calls to **AVIStreamGetFrame**, the function overwrites its buffer with each retrieved frame.</span></span>

<span data-ttu-id="a5db5-116">當您完成使用 **AVIStreamGetFrame** ，且解壓縮的 DIB 位於其緩衝區時，您可以使用 [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) 函數來釋放已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="a5db5-116">When you finish using **AVIStreamGetFrame** and the decompressed DIB is in its buffer, you can release the allocated resources by using the [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) function.</span></span>

<span data-ttu-id="a5db5-117">如需解壓縮影像的詳細資訊，請參閱 [影片壓縮管理員](video-compression-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="a5db5-117">For more information about decompressing images, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 
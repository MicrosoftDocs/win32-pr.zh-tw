---
title: 影像轉譯
description: 影像轉譯
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib，影像轉譯
- DrawDib，繪圖 Dib
- DrawDibDraw 函式
- DrawDibGetBuffer 函式
- DrawDibUpdate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022018"
---
# <a name="image-rendering"></a><span data-ttu-id="bc9c7-108">影像轉譯</span><span class="sxs-lookup"><span data-stu-id="bc9c7-108">Image Rendering</span></span>

<span data-ttu-id="bc9c7-109">在您呼叫 [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) 來建立 DrawDib DC (請參閱 [DrawDib 作業](drawdib-operations.md)) ，您可以使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式在畫面上繪製一個 DIB。</span><span class="sxs-lookup"><span data-stu-id="bc9c7-109">After you call [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) to create a DrawDib DC (see [DrawDib Operations](drawdib-operations.md)), you can draw a DIB to the screen by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span> <span data-ttu-id="bc9c7-110">**DrawDibDraw** dithers 真色彩點陣圖，以8位的顯示器介面卡顯示。</span><span class="sxs-lookup"><span data-stu-id="bc9c7-110">**DrawDibDraw** dithers true-color bitmaps when displaying them with 8-bit display adapters.</span></span>

<span data-ttu-id="bc9c7-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 也支援在顯示壓縮點陣圖時透明地壓縮機影片。</span><span class="sxs-lookup"><span data-stu-id="bc9c7-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) also supports video compressors transparently when displaying compressed bitmaps.</span></span> <span data-ttu-id="bc9c7-112">您可以使用 [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) 函式來存取包含解壓縮映射的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bc9c7-112">You can access the buffer that contains the decompressed image by using the [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) function.</span></span> <span data-ttu-id="bc9c7-113">繪製未壓縮的點陣圖時， **DrawDibGetBuffer** 會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bc9c7-113">**DrawDibGetBuffer** returns **NULL** when drawing an uncompressed bitmap.</span></span> <span data-ttu-id="bc9c7-114">您應該準備您的應用程式來處理壓縮和未壓縮的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="bc9c7-114">You should prepare your application to handle compressed and uncompressed bitmaps.</span></span>

<span data-ttu-id="bc9c7-115">您可以使用 [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) 宏，重新整理應用程式所顯示的影像或部分影像。</span><span class="sxs-lookup"><span data-stu-id="bc9c7-115">You can refresh an image or a portion of an image displayed by your application by using the [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) macro.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc9c7-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc9c7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc9c7-117">關於 DrawDib 函式</span><span class="sxs-lookup"><span data-stu-id="bc9c7-117">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 





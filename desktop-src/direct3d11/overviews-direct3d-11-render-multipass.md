---
title: Multiple-Pass 轉譯
description: 「多重傳遞轉譯」是一種程式，應用程式在此程式中會多次行程其場景圖形，以產生要轉譯成顯示的輸出。
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fcf7f3f04bd641fdf82c9cf317e8a2ec99e85c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301280"
---
# <a name="multiple-pass-rendering"></a><span data-ttu-id="9ede6-103">Multiple-Pass 轉譯</span><span class="sxs-lookup"><span data-stu-id="9ede6-103">Multiple-Pass Rendering</span></span>

<span data-ttu-id="9ede6-104">「多重傳遞轉譯」是一種程式，應用程式在此程式中會多次行程其場景圖形，以產生要轉譯成顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="9ede6-104">Multiple-pass rendering is a process in which an application traverses its scene graph multiple times in order to produce an output to render to the display.</span></span> <span data-ttu-id="9ede6-105">多重傳遞轉譯可改善效能，因為它會將複雜的場景分成可同時執行的工作。</span><span class="sxs-lookup"><span data-stu-id="9ede6-105">Multiple-pass rendering improves performance because it breaks up complex scenes into tasks that can run concurrently.</span></span>

<span data-ttu-id="9ede6-106">若要執行多重傳遞轉譯，您可以為每個額外的行程建立延遲的內容和命令清單。</span><span class="sxs-lookup"><span data-stu-id="9ede6-106">To perform multiple-pass rendering, you create a deferred context and command list for each additional pass.</span></span> <span data-ttu-id="9ede6-107">當應用程式流經場景圖形時，它會記錄命令 (例如，將) [**繪製**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw) 至延遲的內容。</span><span class="sxs-lookup"><span data-stu-id="9ede6-107">While the application traverses the scene graph, it records commands (for example, rendering commands such as [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) into a deferred context.</span></span> <span data-ttu-id="9ede6-108">應用程式完成遍歷之後，它會在延遲的內容上呼叫 [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) 方法。</span><span class="sxs-lookup"><span data-stu-id="9ede6-108">After the application finishes the traversal, it calls the [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) method on the deferred context.</span></span> <span data-ttu-id="9ede6-109">最後，應用程式會在立即內容上呼叫 [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) 方法，以在每個命令清單中執行命令。</span><span class="sxs-lookup"><span data-stu-id="9ede6-109">Finally, the application calls the [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) method on the immediate context to execute the commands in each command list.</span></span>

<span data-ttu-id="9ede6-110">下列虛擬虛擬會顯示如何執行多重傳遞轉譯：</span><span class="sxs-lookup"><span data-stu-id="9ede6-110">The following pseudocode shows how to perform multiple-pass rendering:</span></span>

``` syntax
{
 ImmCtx->SetRenderTarget( pRTViewOfResourceX );
 DefCtx1->SetTexture( pSRView1OfResourceX );
 DefCtx2->SetTexture( pSRView2OfResourceX );

 for () // Traverse the scene graph.
  {
    ImmCtx->Draw(); // Pass 0: immediate context renders primitives into resource X.

    // The following texturing by the deferred contexts occurs after the 
    // immediate context makes calls to ExecuteCommandList. 
    // Resource X is then comletely updated by the immediate context. 
    DefCtx1->Draw(); // Pass 1: deferred context 1 performs texturing from resource X.
    DefCtx2->Draw(); // Pass 2: deferred context 2 performs texturing from resource X.
      }

  // Create command lists and record commands into them.
  DefCtx1->FinishCommandList( &pCL1 ); 
  DefCtx2->FinishCommandList( &pCL2 );

  ImmCtx->ExecuteCommandList( pCL1 ); // Execute pass 1.
  ImmCtx->ExecuteCommandList( pCL2 ); // Exeucte pass 2.
}
```

> [!Note]  
> <span data-ttu-id="9ede6-111">立即內容會修改資源，此資源系結至立即內容，做為轉譯目標視圖 (RTV) ;相反地，每個延遲的內容只會使用資源，此資源會系結至延遲的內容，做為著色器資源檢視 (SRV) 。</span><span class="sxs-lookup"><span data-stu-id="9ede6-111">The immediate context modifies a resource, which is bound to the immediate context as a render target view (RTV); in contrast, each deferred context simply uses the resource, which is bound to the deferred context as a shader resource view (SRV).</span></span> <span data-ttu-id="9ede6-112">如需立即和延後內容的詳細資訊，請參閱 [立即和延](overviews-direct3d-11-render-multi-thread-render.md)後轉譯。</span><span class="sxs-lookup"><span data-stu-id="9ede6-112">For more information about immediate and deferred contexts, see [Immediate and Deferred Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9ede6-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ede6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ede6-114">轉譯</span><span class="sxs-lookup"><span data-stu-id="9ede6-114">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





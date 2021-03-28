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
# <a name="multiple-pass-rendering"></a>Multiple-Pass 轉譯

「多重傳遞轉譯」是一種程式，應用程式在此程式中會多次行程其場景圖形，以產生要轉譯成顯示的輸出。 多重傳遞轉譯可改善效能，因為它會將複雜的場景分成可同時執行的工作。

若要執行多重傳遞轉譯，您可以為每個額外的行程建立延遲的內容和命令清單。 當應用程式流經場景圖形時，它會記錄命令 (例如，將) [**繪製**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw) 至延遲的內容。 應用程式完成遍歷之後，它會在延遲的內容上呼叫 [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) 方法。 最後，應用程式會在立即內容上呼叫 [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) 方法，以在每個命令清單中執行命令。

下列虛擬虛擬會顯示如何執行多重傳遞轉譯：

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
> 立即內容會修改資源，此資源系結至立即內容，做為轉譯目標視圖 (RTV) ;相反地，每個延遲的內容只會使用資源，此資源會系結至延遲的內容，做為著色器資源檢視 (SRV) 。 如需立即和延後內容的詳細資訊，請參閱 [立即和延](overviews-direct3d-11-render-multi-thread-render.md)後轉譯。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





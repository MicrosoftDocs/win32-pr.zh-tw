---
title: 如何錄製命令清單
description: 本主題說明如何建立和記錄命令清單。
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673896"
---
# <a name="how-to-record-a-command-list"></a>如何：錄製命令清單

[命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)是轉譯命令的記錄清單。 本主題說明如何建立和記錄 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)。 使用命令清單來錄製轉譯命令，稍後再播放。 命令清單可方便線上程之間分割轉譯工作。

**錄製命令清單**

1.  命令清單必須從延遲的內容建立，其中包含裝置狀態和轉譯動作。 針對裝置，藉由呼叫 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)來建立延遲的內容。

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  使用延後的內容來呈現。

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    這個簡單的範例會清除轉譯目標，但您可以新增其他轉譯命令。

3.  藉由呼叫 [**>id3d11devicecoNtext：： FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) ，並將指標傳遞至未初始化的 [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) 介面，來建立/記錄命令清單。

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    當方法傳回時，會建立包含所有轉譯命令的命令清單，並將介面傳回給應用程式。

    布林值參數會告知執行時間要如何處理延遲內容中的管線狀態。 **TRUE** 表示在錄製完成時，將裝置內容的狀態還原至其前置命令清單條件， **FALSE** 表示在錄製之後不會變更狀態。 這表示裝置內容會反映命令清單中所包含的狀態變更。

若要查看播放命令清單的範例，請參閱 [如何：播放命令清單](overviews-direct3d-11-render-multi-thread-command-list-play.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





---
description: 宣告並初始化常數、紋理和著色器狀態之後，唯一要做的事就是在裝置中設定效果狀態。
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: '將技術套用 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468093"
---
# <a name="apply-a-technique-direct3d-10"></a>將技術套用 (Direct3D 10) 

宣告並初始化常數、紋理和著色器狀態之後，唯一要做的事就是在裝置中設定效果狀態。

## <a name="set-non-shader-state-in-the-device"></a>設定裝置中的非著色器狀態

某些管線狀態不是由效果設定。 例如，清除轉譯目標可準備資料的呈現目標。 在裝置上設定效果狀態之前，以下是清除輸出緩衝區的範例。


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>在裝置中設定效果狀態

設定效果狀態是藉由在轉譯迴圈內套用效果狀態來完成。 這是從的外部進行。 也就是說，請選取一項技術，然後根據您想要的結果) ，設定每個通過 (的狀態。


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



效果不會轉譯任何事物，而只會將效果狀態設定為裝置。 轉譯程式碼會在效果狀態更新裝置狀態之後呼叫。 在此範例中，DrawIndexed 呼叫會執行轉譯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯 (Direct3D 10) 的效果 ](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




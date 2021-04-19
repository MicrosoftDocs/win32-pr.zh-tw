---
description: 剪下測試選出在剪下矩形之外的圖元，也就是呈現目標的使用者定義矩形子區段。
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: " (Direct3D 9) 的剪式測試"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971119"
---
# <a name="scissor-test-direct3d-9"></a> (Direct3D 9) 的剪式測試

剪下測試選出在剪下矩形之外的圖元，也就是呈現目標的使用者定義矩形子區段。

剪式矩形可用來指出繪製遊戲世界的呈現目的地區域。 矩形外的區域是挑選，而且可能專門用於遊戲的 GUI。 剪式測試無法挑選非矩形區域。

剪式矩形的設定不能大於轉譯目標，但可以設定為大於視口的範圍。

剪式矩形是由裝置呈現狀態所管理。 將 renderstate 設為 **TRUE** 或 **FALSE**，以啟用或停用剪下測試。 這項測試是在計算片段色彩之後，但在 Alpha 測試之前執行。 [**IDirect3DDevice9：： SetRenderTarget**](/windows/desktop/api) 會將剪式矩形重設為完整轉譯目標，類似于重設區域。 [**IDirect3DDevice9：： SetScissorRect**](/windows/desktop/api) 是由 stateblocks 所記錄，而 [**IDirect3DDevice9：： CreateStateBlock**](/windows/desktop/api) 具有 [全部狀態] 設定 (D3DSBT \_) [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md) 中的所有值。 剪式測試也會影響裝置 [**IDirect3DDevice9：： Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) 操作。


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



預設的剪式矩形是完整的視口。

在圖元著色器或固定函式管線完成圖元處理之後，剪下測試就會完成，如下圖所示。

![相對於其他步驟執行剪式測試的圖表](images/scissor-test.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元管線](pixel-pipeline.md)
</dt> </dl>

 

 

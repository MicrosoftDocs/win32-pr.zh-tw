---
description: " (的多個轉譯目標) 指的是轉譯成多個表面的能力 (請參閱使用單一繪製呼叫的 IDirect3D9Surface) 。"
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: " (Direct3D 9) 的多個呈現目標"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d617eb5912557620d9c11bc7fc1a6347fa79b5572abad7fdea0d729445205697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092898"
---
# <a name="multiple-render-targets-direct3d-9"></a> (Direct3D 9) 的多個呈現目標

 (的多個轉譯目標) 指的是轉譯成多個表面的能力 (請參閱使用單一繪製呼叫的 [**IDirect3D9Surface**](/windows/desktop/api)) 。 這些表面可以獨立建立。 您可以使用 [**IDirect3DDevice9：： SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)來設定呈現目標。

多個呈現目標有下列限制：

-   搭配使用的所有轉譯目標表面都必須具有相同的位深度，但可以是不同的格式，除非 \_ 已設定 D3DPMISCCAPS MRTINDEPENDENTBITDEPTHS 端點。
-   多個呈現目標的所有表面都應該具有相同的寬度和高度。
-   某些實作為無法在多個轉譯目標上執行後續圖元著色器作業，包括：無遞色、Alpha 測試、無 fogging、無混色或遮罩（z 測試和樣板測試除外）。 可支援後置圖元著色器作業的裝置會將 cap 位設定為 D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING。

    \_設定 D3DPMISCCAPS MRTPOSTPIXELSHADERBLENDING cap 時，您必須先參考 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) ，並 \_ \_ \_ 針對特定的介面格式使用使用方式查詢 POSTPIXELSHADER 混合結果。 如果為 false，則表示該特定表面格式無法使用任何的後置圖元著色器混合作業。 若為 true，則裝置預期會將相同的狀態套用至所有同時呈現的目標，如下所示：

    -   Alpha blend： oCi 中的色彩值與第 i 個呈現目標混合。
    -   Alpha 測試： oC0 會進行比較。 如果比較失敗，則會結束所有呈現目標的圖元測試。
    -   霧化：轉譯目標0將會取得 fogged。 未定義其他呈現目標。 您可以選擇使用相同的狀態將它們全部霧化。
    -   遞色：未定義。

-   不支援消除鋸齒。
-   部分的執行不會將輸出寫入遮罩套用 (D3DRS \_ COLORWRITEENABLE) 。 可以有獨立色彩寫入遮罩的人。 這是使用新的功能位來表示。 可用的獨立色彩寫入遮罩數目將會等於裝置所能使用的元素數目上限。

新的硬體 cap：


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元管線](pixel-pipeline.md)
</dt> </dl>

 

 

---
description: 光源引擎結合了材質色彩、頂點色彩和光源資訊來產生每個頂點的色彩。
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: " (Direct3D 9) 的 Alpha 材質混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499e915fd786e4cee40ecf6dc9b8b1965e61e41d2f9ac2968cfe1057436d1257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911689"
---
# <a name="alpha-texture-blending-direct3d-9"></a> (Direct3D 9) 的 Alpha 材質混合

光源引擎結合了材質色彩、頂點色彩和光源資訊來產生每個頂點的色彩。 一旦插入，就會產生寫入至框架緩衝區的每圖元色彩。 如果應用程式啟用紋理混色，圖元色彩會變成框架緩衝區中目前圖元的組合和材質色彩。

此公式會決定最終混合的圖元色彩：


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



其中：

-   Color 是輸出圖元色彩。
-   TexelColor 是材質篩選後的輸入色彩。
-   SourceBlend 是由來源材質色彩所組成之最終圖元色彩的百分比。
-   CurrentPixelColor 是目前圖元的色彩。
-   DestBlend 是最後圖元色彩的百分比，由目前的圖元色彩組成。

最終的混合方程式是藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) ，並指定 blend 轉譯狀態 (D3DRS \_ BLENDXXX) 與對應的混合因數 ([**D3DBLEND**](./d3dblend.md)) 來設定。 SourceBlend 和 DestBlend 的值範圍從 0.0 (透明) 至 1.0 (不透明) 內含。 此外，應用程式可以藉由設定材質中的 Alpha 值，來控制圖元的透明度。 在此情況下，請使用下列各項：


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



混合方程式會使呈現的圖元變成透明。 預設值是：


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質混色](texture-blending.md)
</dt> <dt>

[ (Direct3D 9) 的材質篩選 ](texture-filtering.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 

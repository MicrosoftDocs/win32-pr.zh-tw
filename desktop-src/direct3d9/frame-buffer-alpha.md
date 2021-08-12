---
description: 框架緩衝區 Alpha-混色與頂點 Alpha、材質 Alpha 和材質 Alpha 有點不同。
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: " (Direct3D 9) 的框架緩衝區 Alpha"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec091e8cc42d6b21142d3b9372f6d2931ba25d1dfe12aa7717e0b09acf0b0718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297493"
---
# <a name="frame-buffer-alpha-direct3d-9"></a> (Direct3D 9) 的框架緩衝區 Alpha

框架緩衝區 Alpha-混色與頂點 Alpha、材質 Alpha 和材質 Alpha 有點不同。 頂點、材質和材質 Alpha 設定的透明度值只用于目前的基本專案，而且本身不會影響其他基本專案。 框架緩衝區 Alpha-混合控制目前的基本類型如何與框架緩衝區中的現有圖元結合，以產生最終圖元色彩。

執行 Alpha 混色時，會結合兩種色彩：來源色彩和目的色彩。 來源色彩是來自透明物件，目的色彩是已在圖元位置的色彩。 目的色彩是轉譯其他位於透明物件後方的物件（也就是可透過透明物件看見的物件）的結果。 Alpha 混色會使用公式來控制來源和目的地物件之間的比率。


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor 是在目前圖元位置轉譯的基本內容。 PixelColor 是來自目前圖元位置的框架緩衝區所占的比重。

以下列出一組可以使用的 Alpha blend 因素。



| Blend 模式因數         | 描述                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ 零            |  (0、0、0、0)                                                                                                                                                                              |
| D3DBLEND \_ 一             |  (1，1，1，1)                                                                                                                                                                              |
| D3DBLEND \_ SRCCOLOR        |  (Rs、Gs、Bs)                                                                                                                                                                          |
| D3DBLEND \_ INVSRCCOLOR     |  (1-Rs、1-Gs、1-Bs、1-As)                                                                                                                                                                  |
| D3DBLEND \_ SRCALPHA        |  (As，as，as，as)                                                                                                                                                                          |
| D3DBLEND \_ INVSRCALPHA     |  (1-As，1-as，1-As，1-As)                                                                                                                                                                  |
| D3DBLEND \_ DESTALPHA       |  (Ad、Ad、Ad、Ad)                                                                                                                                                                          |
| D3DBLEND \_ INVDESTALPHA    |  (1-Ad、1-Ad、1-Ad、1-Ad)                                                                                                                                                                  |
| D3DBLEND \_ DESTCOLOR       |  (Rd、Gd、Bd、Ad)                                                                                                                                                                          |
| D3DBLEND \_ INVDESTCOLOR    |  (1-Rd、1-Gd、1-Bd、1-Ad)                                                                                                                                                                  |
| D3DBLEND \_ SRCALPHASAT     |  (f、f、f、1) ;f = min (As，1-Ad)                                                                                                                                                           |
| D3DBLEND \_ BOTHSRCALPHA    | DirectX 6 和更新版本已淘汰。 您可以藉由將來源和目的地 blend 因數設定為 \_ \_ 在個別呼叫中 D3DBLEND SRCALPHA 和 D3DBLEND INVSRCALPHA 來達到相同的效果。 |
| D3DBLEND \_ BOTHINVSRCALPHA | DirectX 6 已淘汰。 您可以藉由將來源和目的地 blend 因數設定為 \_ \_ 在個別呼叫中 D3DBLEND INVSRCALPHA 和 D3DBLEND SRCALPHA 來達到相同的效果。           |
| D3DBLEND \_ BLENDFACTOR     | 使用 color. r、color. g、color. b 和 color。從 D3DRS BLENDFACTOR 設定取得的。 \_                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | 使用 1-color、1-color. g、1-color. b 和1色彩。從 D3DRS BLENDFACTOR 設定取得的。 \_                                                                                         |



 

Direct3D 使用 D3DRS \_ ALPHABLENDENABLE 轉譯狀態來啟用 Alpha 透明度混合。 完成的 Alpha 混色類型取決於 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND 轉譯狀態。 來源和目的地 blend 狀態會成對使用。 下列程式碼片段會將來源 blend 狀態設定為 D3DBLEND \_ SRCCOLOR，並將目的地 blend 狀態設定為 D3DBLEND \_ INVSRCCOLOR。


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



這段程式碼會在來源色彩之間執行線性 blend (在目前) 位置轉譯的基本型別，以及目的地色彩 (框架緩衝區) 中目前位置的色彩。 產生的外觀類似于彩色玻璃，因為目的地物件的某些色彩似乎是透過來源物件傳輸;其餘的部分則會被吸收。

其中許多 blend 因數都需要材質中的 Alpha 值，才能正確運作。 因此，使用頂點或材質 Alpha 時，應用程式會限制為會產生有趣結果的模式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Alpha 混色](alpha-blending.md)
</dt> </dl>

 

 




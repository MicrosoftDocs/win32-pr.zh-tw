---
description: 本節包含下列效果系統介面的相關資訊：
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: " (Direct3D 10) 的效果介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07e6ecf45f4ef052c7d576849a55d00ef0f877dde7c41fa5dc80b7592761325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303971"
---
# <a name="effect-interfaces-direct3d-10"></a> (Direct3D 10) 的效果介面

本節包含下列效果系統介面的相關資訊：



| 介面                                                                                     | 描述                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**ID3D10EffectBlendVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | 存取 blend 狀態。                                            |
| [**ID3D10EffectConstantBuffer 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | 存取材質緩衝區或常數緩衝區。                  |
| [**ID3D10EffectDepthStencilVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | 存取深度範本的狀態。                                    |
| [**ID3D10EffectDepthStencilViewVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | 存取深度範本視圖。                                   |
| [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | 封裝一或多個轉譯技術中的管線狀態。 |
| [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | 用來讀取 include 檔的使用者執行方法。              |
| [**ID3D10EffectMatrixVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | 存取矩陣。                                               |
| [**ID3D10EffectPass 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | 將效果狀態封裝在傳遞中。                             |
| [**ID3D10EffectPool 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | 識別共用效果變數。                              |
| [**ID3D10EffectRasterizerVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | 存取轉譯器狀態。                                       |
| [**ID3D10EffectRenderTargetViewVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | 存取呈現目標。                                        |
| [**ID3D10EffectSamplerVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | 存取取樣器狀態。                                          |
| [**ID3D10EffectScalarVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | 存取純量變數。                                      |
| [**ID3D10EffectShaderResourceVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | 存取著色器資源。                                      |
| [**ID3D10EffectShaderVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | 存取著色器變數。                                      |
| [**ID3D10EffectStringVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | 存取字串。                                               |
| [**ID3D10EffectTechnique 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | 封裝一或多個階段。                                 |
| [**ID3D10EffectType 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | 實行存取效果變數的方法。               |
| [**ID3D10EffectVectorVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | 存取 vector。                                               |



 

效果架構中有兩種介面：轉譯介面以轉譯效果和反映介面，以使用 API 來取得和設定效果變數。 所有反映介面都是衍生自 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果參考](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 

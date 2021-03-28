---
title: 效果11介面
description: 本節包含元件物件模型的參考資訊， (效果11來源的 COM) 介面。
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215e319720f2afc4cf74f6c49056de35fb59d004
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971821"
---
# <a name="effects-11-interfaces"></a>效果11介面

本節包含元件物件模型的參考資訊， (效果11來源的 COM) 介面。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                   | 描述                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | [**ID3DX11Effect**](id3dx11effect.md)介面會管理一組用於執行轉譯效果的狀態物件、資源和著色器。<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | Blend 變數介面會存取 blend 狀態。<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | 存取類別實例。<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | 常數緩衝區介面會存取常數緩衝區或紋理緩衝區。<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | 深度樣板變數介面會存取深度樣板的狀態。<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | 深度樣板視圖變數介面會存取深度樣板視圖。<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | [**ID3DX11EffectGroup**](id3dx11effectgroup.md)介面會存取效果群組。<br/> [**ID3DX11EffectGroup**](id3dx11effectgroup.md)物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | 存取介面變數。<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | 矩陣變數介面會存取矩陣。<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | [**ID3DX11EffectPass**](id3dx11effectpass.md)介面會將狀態指派封裝在技術內。<br/> [**ID3DX11EffectPass**](id3dx11effectpass.md)物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | 轉譯器變數介面會存取轉譯器的狀態。<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | 呈現目標視圖介面會存取轉譯目標。<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | 取樣器介面會存取取樣器狀態。<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | 效果純量變數介面會存取純量值。<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | 著色器資源介面會存取著色器資源。<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | 著色器變數介面會存取著色器變數。<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | 字串變數介面會存取字串變數。<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)介面是通過的集合。<br/> [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | [**ID3DX11EffectType**](id3dx11effecttype.md)介面會依類型存取效果變數。<br/> [**ID3DX11EffectType**](id3dx11effecttype.md)物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | 存取未排序的存取權。<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | [**ID3DX11EffectVariable**](id3dx11effectvariable.md)介面是所有效果變數的基類。<br/> [**ID3DX11EffectVariable**](id3dx11effectvariable.md)物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | 向量變數介面會存取四個元件的向量。<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果11參考](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 






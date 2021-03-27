---
title: " (Direct3D 11) 的效果系統介面"
description: 效果系統會定義許多用於管理效果狀態的介面。
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671896"
---
# <a name="effect-system-interfaces-direct3d-11"></a> (Direct3D 11) 的效果系統介面

效果系統會定義許多用於管理效果狀態的介面。 有兩種類型的介面：執行時間用來呈現效果和反映介面以取得和設定效果變數的介面。

-   [效果執行時間介面](#effect-runtime-interfaces)
-   [效果反映介面](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>效果執行時間介面

使用執行時間介面來呈現效果。



| 執行時間介面                                       | Description                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | 用於轉譯的一或多個群組和技術的集合。 |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | 狀態指派的集合。                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | 一或多個傳遞的集合。                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | 一或多個技術的集合。                        |



 

## <a name="effect-reflection-interfaces"></a>效果反映介面

反映會在效果系統中執行，以支援讀取 (和寫入) 效果狀態。 有多種方式可存取效果變數。

### <a name="setting-groups-of-effect-state"></a>設定效果狀態的群組

使用這些介面來取得和設定一組狀態。



| 反映介面                                                          | Description                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | 取得並設定 blend 狀態。         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | 取得並設定深度樣板狀態。 |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | 取得並設定轉譯器狀態。    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | 取得並設定取樣器狀態。       |



 

### <a name="setting-effect-resources"></a>設定效果資源

使用這些介面來取得和設定資源。



| 反映介面                                                                        | Description                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | 存取材質緩衝區或常數緩衝區中的資料。 |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | 存取深度樣板資源中的資料。            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | 存取轉譯目標中的資料。                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | 存取著色器資源中的資料。                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | 存取未排序存取視圖中的資料。            |



 

### <a name="setting-other-effect-variables"></a>設定其他效果變數

使用這些介面可依變數類型來取得和設定狀態。



| 反映介面                                                            | Description               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | 取得類別實例。     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | 取得和設定介面。 |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | 取得和設定矩陣。     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | 取得和設定純量。     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | 取得著色器變數。    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | 取得並設定字串。     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | 取得變數型別。      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | 取得和設定向量。     |



 

所有反映介面都是衍生自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Direct3D 11 的程式設計指南](dx-graphics-overviews.md)
</dt> </dl>

 

 





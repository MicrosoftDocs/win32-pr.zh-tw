---
description: 效果系統會定義許多用於管理效果狀態的介面。 有兩種類型的介面：執行時間用來呈現效果和反映介面以取得和設定效果變數的介面。
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: " (Direct3D 10) 的效果系統介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110384"
---
# <a name="effect-system-interfaces-direct3d-10"></a> (Direct3D 10) 的效果系統介面

效果系統會定義許多用於管理效果狀態的介面。 有兩種類型的介面：執行時間用來呈現效果和反映介面以取得和設定效果變數的介面。

-   [效果執行時間介面](#effect-runtime-interfaces)
-   [效果反映介面](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>效果執行時間介面

使用執行時間介面來呈現效果。



| 執行時間介面                                               | Description                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | 收集一或多個用於轉譯的技巧。                  |
| [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | 在讀取包含檔案時，用來加入自訂行為的介面。 |
| [**ID3D10EffectPass 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | 狀態指派的集合。                                   |
| [**ID3D10EffectPool 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | 建立要在效果之間共用之變數的記憶體位置。 |
| [**ID3D10EffectTechnique 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | 一或多個傳遞的集合。                                  |



 

## <a name="effect-reflection-interfaces"></a>效果反映介面

反映會在效果系統中執行，以支援讀取 (和寫入) 效果狀態。 有多種方式可存取效果變數。

### <a name="setting-groups-of-effect-state"></a>設定效果狀態的群組

使用這些介面來取得和設定一組狀態。



| 反映介面                                                                  | Description                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**ID3D10EffectBlendVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | 取得並設定 blend 狀態。         |
| [**ID3D10EffectDepthStencilVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | 取得並設定深度樣板狀態。 |
| [**ID3D10EffectRasterizerVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | 取得並設定轉譯器狀態。    |
| [**ID3D10EffectSamplerVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | 取得並設定取樣器狀態。       |



 

### <a name="setting-effect-resources"></a>設定效果資源

使用這些介面來取得和設定資源。



| 反映介面                                                                          | Description                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3D10EffectConstantBuffer 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | 存取材質緩衝區或常數緩衝區中的資料。 |
| [**ID3D10EffectDepthStencilViewVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | 存取深度樣板資源中的資料。            |
| [**ID3D10EffectRenderTargetViewVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | 存取轉譯目標中的資料。                     |
| [**ID3D10EffectShaderResourceVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | 存取著色器資源中的資料。                   |



 

### <a name="setting-other-effect-variables"></a>設定其他效果變數

使用這些介面可依變數類型來取得和設定狀態。



| 反映介面                                                      | Description                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**ID3D10EffectMatrixVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | 取得和設定矩陣。          |
| [**ID3D10EffectScalarVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | 取得和設定純量。          |
| [**ID3D10EffectShaderVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | 取得和設定著色器變數。 |
| [**ID3D10EffectStringVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | 取得並設定字串。          |
| [**ID3D10EffectType 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | 取得變數型別。           |
| [**ID3D10EffectVectorVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | 取得和設定向量。          |



 

所有反映介面都是衍生自 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影響](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 

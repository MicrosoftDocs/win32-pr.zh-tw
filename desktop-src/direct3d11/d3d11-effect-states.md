---
title: '效果狀態群組 (Direct3D 11) '
description: 效果狀態是運算式形式的名稱值配對。
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- '效果、狀態群組 (Direct3D 11) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335332"
---
# <a name="effect-state-groups-direct3d-11"></a>效果狀態群組 (Direct3D 11) 

效果狀態是運算式形式的名稱值配對。

-   [Blend 狀態](#blend-state)
-   [深度和樣板狀態](#depth-and-stencil-state)
-   [轉譯器狀態](#rasterizer-state)
-   [取樣器狀態](#sampler-state)
-   [效果物件狀態](#effect-object-state)
-   [定義和使用狀態物件](#defining-and-using-state-objects)
-   [相關主題](#related-topics)

## <a name="blend-state"></a>混色狀態



| 效果狀態                                                                                                                      | Group                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK | [ **D3D11 \_ BLEND \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>深度和樣板狀態



|  效果狀態                                                                                                                                                              | Group                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | [ **D3D11 深度樣板 \_ \_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC | [ **D3D11 \_ 深度 \_ STENCILOP \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>轉譯器狀態



| 效果狀態                                                                                                                                | Group                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| FILLMODE                                                                                                                        | [**D3D11 \_ 填滿 \_ 模式**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CULLMODE                                                                                                                        | [**D3D11 的 \_ 挑選 \_ 模式**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | D3D11 轉譯器 [ **\_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>取樣器狀態



| 效果狀態                                                                                                    | Group                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc 邊框 MinLOD MaxLOD | [ **D3D11 取樣器 \_ \_ DESC** 的成員](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

如需範例，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) 。

## <a name="effect-object-state"></a>效果物件狀態



| 此效果物件                          | 對應至                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | 轉譯器 [狀態](#rasterizer-state) 狀態物件。               |
| DEPTHSTENCILSTATE                           | [深度和樣板狀態](#depth-and-stencil-state)狀態物件。 |
| BLENDSTATE                                  | [Blend 狀態](#blend-state)狀態物件。                         |
| VERTEXSHADER                                | 已編譯的頂點著色器物件。                                    |
| 無效                                 | 編譯的圖元著色器物件。                                     |
| GEOMETRYSHADER                              | 已編譯的幾何著色器物件。                                  |
| DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK | [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)的成員。          |



 

## <a name="defining-and-using-state-objects"></a>定義和使用狀態物件

系統會以下列格式在 FX 檔案中宣告狀態物件。 StateObjectType 是上面所列的其中一個狀態，而成員名稱則是任何將具有非預設值的成員名稱。


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



例如，若要設定 AlphaToCoverageEnable，並將 BlendEnable \[ 0 \] 設為 **FALSE** 的 blend 狀態物件，則會使用下列程式碼。


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



使用 [ (Direct3D 11) 的效果技巧語法 ](d3d11-effect-technique-syntax.md)中所述的其中一個 SetStateGroup 函式，將狀態物件套用至技術傳遞。 例如，若要套用上面所述的 BlendState 物件，則會使用下列程式碼。


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果技巧語法](d3d11-effect-technique-syntax.md)
</dt> <dt>

[ (Direct3D 11) 的效果格式 ](d3d11-effect-format.md)
</dt> </dl>

 

 
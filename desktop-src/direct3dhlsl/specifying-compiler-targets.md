---
title: 指定編譯器目標
description: 在這裡，我們會列出 D3DCompile \ 函式和 HLSL 編譯器支援之各種設定檔的目標。
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d020edaabf4c618b1fa911a91bc4cc0e8b37e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481834"
---
# <a name="specifying-compiler-targets"></a>指定編譯器目標

當您呼叫 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)、 [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)或 [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) 函式時，您需要指定著色器目標（著色器的組合）來進行編譯。 在這裡，我們會列出 **D3DCompile \*** 函式和 HLSL 編譯器支援之各種設定檔的目標。

-   [Direct3D 11.0 和11.1 功能等級](#direct3d-110-and-111-feature-levels)
-   [Direct3D 10.1 功能等級](#direct3d-101-feature-level)
-   [Direct3D 10.0 功能等級](#direct3d-100-feature-level)
-   [Direct3D 9.1、9.2 和9.3 功能等級](#direct3d-91-92-and-93-feature-levels)
-   [舊版 Direct3D 9 著色器模型3。0](#legacy-direct3d-9-shader-model-30)
-   [舊版 Direct3D 9 著色器模型2。0](#legacy-direct3d-9-shader-model-20)
-   [舊版 Direct3D 9 著色器模型1。x](#legacy-direct3d-9-shader-model-1x)
-   [舊版效果](#legacy-effects)
-   [注意事項](#notes)
-   [相關主題](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Direct3D 11.0 和11.1 功能等級

以下是 Direct3D 11.0 和 11.1 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。



| 目標   | Description                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 5 \_ 0 | DirectCompute 5.0 ([計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                               |
| ds \_ 5 \_ 0 | [網域著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| gs \_ 5 \_ 0 | [幾何著色器](/previous-versions//bb205146(v=vs.85)) |
| hs \_ 5 \_ 0 | [輪廓著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| ps \_ 5 \_ 0 | [像素著色器](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [頂點著色器](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Direct3D 10.1 功能等級

以下是 Direct3D 10.1 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。



| 目標   | Description                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 1 | DirectCompute 4.1 ([計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| gs \_ 4 \_ 1 | [幾何著色器](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 1 | [像素著色器](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [頂點著色器](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Direct3D 10.0 功能等級

以下是 Direct3D 10.0 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。



| 目標   | Description                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 0 | DirectCompute 4.0 ([計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| gs \_ 4 \_ 0 | [幾何著色器](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 0 | [像素著色器](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [頂點著色器](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Direct3D 9.1、9.2 和9.3 功能等級

以下是 Direct3D 9.1、9.2 和 9.3 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 所支援的著色器目標。

> [!Note]  
> 當您使用 \* \_ 4 個 \_ \_ 層級 \_ 9 \_ x HLSL 著色器設定檔時，會隱含地使用[著色器模型](dx-graphics-hlsl-sm2.md)2.x 設定檔來支援具有 Direct3D 9 功能的硬體。 著色器模型2.x 設定檔支援的流程式控制制行為比 [著色器模型](dx-graphics-hlsl-sm4.md) 4.x 和更新版本設定檔更受限。

 




| 目標 | Description | 
|--------|-------------|
| ps_4_0_level_9_1 | 9.1 和9.2 的[圖元著色器](/previous-versions//bb205146(v=vs.85)) (ps_2_0) 的類似限制<ul><li>64算術和32材質指示</li><li>12個臨時暫存器</li><li>4個相依讀取層級</li></ul> | 
| ps_4_0_level_9_3 | 9.3 的<a href="/previous-versions//bb205146(v=vs.85)">圖元著色器</a> (ps_2_x ²與額外著色器功能的類似限制) <ul><li>512指示</li><li>32臨時暫存器</li><li>靜態流量控制 (最大深度 4) </li><li>動態流量控制 (最大深度 24) </li><li>D3DPS20CAPS_ARBITRARYSWIZZLE</li><li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li><li>D3DPS20CAPS_PREDICATION</li><li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li><li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li></ul> | 
| vs_4_0_level_9_1 | 9.1 和 9.2 (的<a href="/previous-versions//bb205146(v=vs.85)">頂點著色器</a>類似于 vs_2_0) <ul><li>256指示</li><li>12個臨時暫存器</li><li>靜態流量控制 (最大深度為 1) </li></ul> | 
| vs_4_0_level_9_3 | 9.3 (的<a href="/previous-versions//bb205146(v=vs.85)">頂點著色器</a>類似于 vs_2_a ²與其他著色器功能和實例) <ul><li>256指示</li><li>32臨時暫存器</li><li>靜態流量控制 (最大深度 4) </li><li>D3DVS20CAPS_PREDICATION</li></ul> | 




 

## <a name="legacy-direct3d-9-shader-model-30"></a>舊版 Direct3D 9 著色器模型3。0

以下是舊版 Direct3D 9 著色器模型3.0 ³的著色器目標。



| 目標    | Description                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 3 \_ 0  | [圖元著色器](/previous-versions//bb205146(v=vs.85)) 3。0               |
| ps \_ 3 \_ sw | [圖元著色器](/previous-versions//bb205146(v=vs.85)) 3.0 (軟體)     |
| vs \_ 3 \_ 0  | [頂點著色器](/previous-versions//bb205146(v=vs.85)) 3。0            |
| vs \_ 3 \_ sw | [頂點著色器](/previous-versions//bb205146(v=vs.85)) 3.0 (軟體)  |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>舊版 Direct3D 9 著色器模型2。0

以下是舊版 Direct3D 9 著色器模型2.0 ³的著色器目標。



| 目標    | Description                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 2 \_ 0  | [圖元著色器](/previous-versions//bb205146(v=vs.85)) 2。0             |
| ps \_ 2 \_ a  | [圖元著色器](/previous-versions//bb205146(v=vs.85)) 2a              |
| ps \_ 2 \_ b  | [圖元著色器](/previous-versions//bb205146(v=vs.85)) 2b              |
| ps \_ 2 \_ sw | [圖元著色器](/previous-versions//bb205146(v=vs.85)) 2.0 軟體    |
| vs \_ 2 \_ 0  | [頂點著色器](/previous-versions//bb205146(v=vs.85)) 2。0          |
| vs \_ 2 \_ a  | [頂點著色器](/previous-versions//bb205146(v=vs.85)) 2a           |
| vs \_ 2 \_ sw | [頂點著色器](/previous-versions//bb205146(v=vs.85)) 2.0 軟體 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>舊版 Direct3D 9 著色器模型1。x

以下是舊版 Direct3D 9 著色器模型1.x ⁴的著色器目標。



| 目標   | Description                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 德克薩斯州 \_ 1 \_ 0 | 舊版 D3DX9 ⁵函式 [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) 和 [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) 使用的材質著色器設定檔 |
| vs \_ 1 \_ 1 | [頂點著色器](/previous-versions//bb205146(v=vs.85)) 1。1                                                            |



 

## <a name="legacy-effects"></a>舊版效果

以下是舊版效果的效果目標。



| 目標   | Description                               |
|----------|-------------------------------------------|
| fx \_ 2 \_ 0 | 在 D3DX9 ⁵中，Direct3D 9 的 (FX) 效果     |
| fx \_ 4 \_ 0 | D3DX10 ⁵中 Direct3D 10.0 的效果 (FX)  |
| fx \_ 4 \_ 1 | D3DX10 ⁵中 Direct3D 10.1 的效果 (FX)  |
| fx \_ 5 \_ 0 | 適用于 Direct3D 11 ⁵的 (FX) 效果             |



 

## <a name="notes"></a>備註

以下是上述各節所指的一些注意事項：

1.  [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 和10.1 裝置可選擇性地支援 DirectCompute。 若要驗證支援，請使用 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) 搭配 [**D3D11 \_ 功能 \_ D3D10 \_ X \_ 硬體 \_ 選項**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature)。
2.  [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 實際上需要符合 [舊版 Direct3D 9 著色器模型 3.0](#legacy-direct3d-9-shader-model-30)需求的硬體，但此功能層級不會使用 vs \_ 3 \_ 0 或 ps \_ 3 \_ 0 目標。
3.  只搭配 Direct3D 9 API 使用舊版 Direct3D 9 著色器模型。 相反地，請將2.x 設定檔與 Direct3D 2.x 和 11. x API 搭配使用。
4.  目前的 HLSL 著色 **器 \* D3DCompile** 函數不支援舊版1.x 圖元著色器。 HLSL 支援這些目標的最新版本已于2006年10月版本的 DirectX SDK 中 D3DX9。
5.  所有版本的 D3DX 和 DirectX SDK 均已淘汰。 如需詳細資訊，請參閱 [什麼是 DIRECTX SDK？](/windows/desktop/directx-sdk--august-2009-)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 

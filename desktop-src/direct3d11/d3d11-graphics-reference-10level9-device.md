---
title: 10Level9 ID3D11Device 方法
description: 本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 ID3D11Device 方法功能層級之間的差異。
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467e47d7ba623f1c28111cf3bf7cc6a07da8317
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475784"
---
# <a name="10level9-id3d11device-methods"></a>10Level9 ID3D11Device 方法

本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 方法功能層級之間的差異。

-   [ID3D11Device::CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device::CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device::CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device::CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device::CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device::CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device::CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device::CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device::CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device::CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device::CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device::CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device::CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device::CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device::CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device：： CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device::CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device::CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device::CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device::CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device::CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device::CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device::CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device::CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device::CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device::OpenSharedResource](#id3d11deviceopensharedresource)
-   [相關主題](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device::CheckCounter




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 選擇性地支援裝置相依的計數器。 使用 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device：： CheckCounterInfo</strong></a> 來判斷支援。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device::CheckFormatSupport




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 請參閱依 <a href="overviews-direct3d-11-devices-downlevel-intro.md">功能等級</a>的格式支援 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device::CheckMultisampleQualityLevels




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 功能層級對 MSAA 支援沒有任何保證。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device::CreateBlendState



| 功能層級              | 行為差異                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1  | AlphaToCoverageEnable 必須是 **FALSE**。<br/> 前四個 BlendEnables 必須有相同的值。<br/> \_ \_ 不支援 D3D11 BLEND SRC \_ ALPHASAT。<br/> 不支援雙重來源色彩 blend (名稱中有 SRC1 的任何 SrcBlend 或 DestBlend) <br/>                                                                                |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2  | AlphaToCoverageEnable 必須是 **FALSE**。<br/> 前四個 BlendEnables 必須有相同的值。<br/> 前四個 RenderTargetWriteMasks 必須有相同的值。<br/> \_ \_ 不支援 D3D11 BLEND SRC \_ ALPHASAT。<br/> 不支援雙重來源色彩 blend (名稱中有 SRC1 的任何 SrcBlend 或 DestBlend) <br/> |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3  | AlphaToCoverageEnable 必須是 **FALSE**。<br/> 前四個 BlendEnables 必須有相同的值。<br/> \_ \_ 不支援 D3D11 BLEND SRC \_ ALPHASAT。<br/> 不支援雙重來源色彩 blend (名稱中有 SRC1 的任何 SrcBlend 或 DestBlend) <br/>                                                                                |
| D3D \_ 功能 \_ 等級 \_ 10 \_ 0 | 新增 Alpha 到涵蓋範圍                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device::CreateBlendState1



| 功能層級              | 行為差異                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1  | 不支援<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2  | 不支援<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3  | 不支援<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ 功能 \_ 等級 \_ 10 \_ 0 | *OutputMergerLogicOp* 成員已新增至 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)，以判斷 (圖元著色器輸出和轉譯目標內容之間的位邏輯運算支援邏輯作業，請參閱 [**D3D11 轉譯 \_ \_ 目標 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)) 。 |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device::CreateBuffer




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 緩衝區不能有呈現目標視圖。<br /> 緩衝區必須剛好有其中一個 D3D11_BIND_VERTEX_BUFFER、D3D11_BIND_INDEX_BUFFER 或 D3D11_BIND_CONSTANT_BUFFER。<br /> 只允許具有 DXGI_FORMAT_R16_UINT 格式的索引緩衝區。 <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  緩衝區不能有呈現目標視圖。<br /> 緩衝區必須剛好有其中一個 D3D11_BIND_VERTEX_BUFFER、D3D11_BIND_INDEX_BUFFER 或 D3D11_BIND_CONSTANT_BUFFER。<br /> 允許具有 DXGI_FORMAT_R16_UINT 的索引緩衝區，以及 D3D_FEATURE_LEVEL_10_0 和更高版本的 DXGI_FORMAT_R32_UINT 格式。 <br /> $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device::CreateCounter




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device::CreateDepthStencilView




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援雙面樣板。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device::CreateDomainShader




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device::CreateGeometryShader




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device::CreateGeometryShaderWithStreamOutput




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device::CreateHullShader




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device::CreateInputLayout



| 功能層級             | 行為差異                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 不支援 \_ \_ 每個 \_ 實例 \_ 資料的 D3D11 輸入                                                                |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 不支援 \_ \_ 每個 \_ 實例 \_ 資料的 D3D11 輸入                                                                |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | \_ \_ \_ \_ 如果任何資料流程的 \_ \_ 每個頂點 \_ \_ 資料都有 D3D11 輸入，則頂點資料流程零必須有 D3D11 輸入 |



 

如需可在每個功能層級上使用哪些格式的詳細資料，請參閱依 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 的格式支援圖表。

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device::CreatePixelShader



| 功能層級             | 行為差異                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 必須使用 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1                          |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 必須使用 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1                          |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 必須使用 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 3 或 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device::CreatePredicate




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatequery"></a>ID3D11Device：： CreateQuery



| 功能層級             | 行為差異                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 支援事件查詢。 時間戳記查詢是選擇性的：呼叫 [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) 以判斷支援。               |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 支援事件和遮蔽查詢。 時間戳記查詢是選擇性的：呼叫 [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) 以判斷支援。 |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 支援事件和遮蔽查詢。 時間戳記查詢是選擇性的：呼叫 [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) 以判斷支援。 |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device::CreateRasterizerState




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | DepthClipEnable 必須是 <strong>TRUE</strong>。 DepthBiasClamp 必須設定為 0. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device::CreateRenderTargetView




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 只能支援 Texture2D 物件的呈現目標視圖。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device::CreateSamplerState




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援比較篩選。<br /> 框線色彩必須在 [0，1] 內<br /> 最小」 LOD 不可為小數<br /> 」 LOD 上限必須是 FLT_MAX<br /> 最大 anisotropy 為2。<br /> 不支援 D3D11_TEXTURE_ADDRESS_MIRRORONCE。<br /> | 
| D3D_FEATURE_LEVEL_9_2 |  不支援比較篩選。<br /> 框線色彩必須在 [0，1] 內<br /> 最小」 LOD 不可為小數<br /> 」 LOD 上限必須是 FLT_MAX<br /> 最大 anisotropy 為16。<br /> $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device::CreateShaderResourceView



| 功能層級             | MostDetailedMip plus MipLevels 必須包含最低的」 LOD (最小 subresource | View 必須包含所有資源陣列元素 |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 是                                                                          | 是                                           |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 是                                                                          | 是                                           |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 是                                                                          | 是                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device::CreateTexture1D




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device::CreateTexture2D

Texture2D 資源的寬度和高度會有不同于各 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)的限制。 在功能層級 9 \_ 3 中，以下是保證最小值的，而個別的執行可能會超出需求。



| 功能層級             | 如果 MipCount > 1，維度必須是兩個的整數乘冪 | 支援的最小材質維度 | Cube 紋理維度必須是2的乘冪 | 如果設定了其他 \_ TEXTURECUBE，則 ArraySize 為： | 如果 \_ 未設定其他 TEXTURECUBE，則 ArraySize 為。 |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 是                                                          | 2048                                | 是                                           | 6                                              | 1                                                  |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 是                                                          | 2048                                | 是                                           | 6                                              | 1                                                  |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 是                                                          | 4096                                | 是                                           | 6                                              | 1                                                  |



 

在上表中， **其他 \_ TEXTURECUBE** 的完整名稱是 [**D3D11 \_ 資源 \_ 其他 \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)。

以下是所有9個 \_ \* [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)的條件：

-   使用 D3D11 \_ usage \_ DEFAULT 或 D3D11 \_ usage \_ 不可變時，BindFlags 不可以是零。
-   使用 D3D11 系結深度樣板時 \_ \_ \_ ，MipLevels 必須是1。
-   使用 D3D11 \_ BIND \_ 著色器 \_ 資源時，SampleDesc 必須是1。
-   當目前使用 D3D11 系結時 \_ \_ ，資源無法具有 D3D11 系結 \_ \_ 著色器 \_ 資源。
-   使用 D3D10 \_ DDI \_ 資源 \_ 的其他 \_ 共用時，格式不能是 DXGI 格式 \_ \_ R8G8B8A8 \_ UNORM 或 dxgi \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB。

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device::CreateTexture3D



| 功能層級             | 任何軸) 的最大維度 ( | 維度必須是2的乘冪 |
|---------------------------|------------------------------|---------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 256                          | 是                             |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 512                          | 是                             |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 512                          | 是                             |



 

如果資源是 D3D11 \_ 使用 \_ 預設值，或 D3D11 \_ 使用方式 \_ 不變，則 BindFlags 不可以是零。

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device::CreateUnorderedAccessView




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | 不支援任何 9. * 功能等級。 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device::CreateVertexShader



| 功能層級             | 行為差異                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 必須使用 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1                          |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 必須使用 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1                          |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 必須使用 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 3 或 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device::OpenSharedResource




| 功能層級 | 行為差異 | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  使用 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device：： CheckFeatureSupport</strong></a> 搭配 <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> 值和 <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> 結構，以判斷是否可以共用格式。 如果可以共用格式， <strong>CheckFeatureSupport</strong> 會傳回 <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> 旗標。<br /><blockquote>[!Note]<br />使用功能層級9時， [<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)和<strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong>永遠無法共用，即使裝置指出<strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>的選擇性功能支援。 除非10_0 或更高的功能等級，否則嘗試以 DXGI 格式建立共用資源 <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> 和 <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> 一律會失敗。</blockquote><br /> $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[10Level9 參考](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 


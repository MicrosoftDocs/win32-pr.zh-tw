---
title: 遷移至 Direct3D 11
description: 本節提供從舊版 Direct3D 遷移至 Direct3D 11 的資訊。
ms.assetid: 3ec8b5c2-01e6-4fbe-ada7-43898db63bbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ade0a0d32d3f8b5c07e6653955c0c407c8fa8f
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316624"
---
# <a name="migrating-to-direct3d-11"></a>遷移至 Direct3D 11

本節提供從舊版 Direct3D 遷移至 Direct3D 11 的資訊。

-   [Direct3D 9 至 Direct3D 11](#direct3d-9-to-direct3d-11)
-   [Direct3D 10 到 Direct3D 11](#direct3d-10-to-direct3d-11)
    -   [列舉和定義](#enumerations-and-defines)
    -   [結構](#structures)
    -   [介面](#interfaces)
    -   [其他相關技術](#other-related-technologies)
-   [Direct3D 10.1 至 Direct3D 11](#direct3d-101-to-direct3d-11)
    -   [列舉和定義](#enumerations-and-defines)
    -   [結構](#structures)
    -   [介面](#interfaces)
-   [Direct3D 11 的新功能](#new-features-for-direct3d-11)
-   [DirectX 11.1 的新功能](#new-features-for-directx-111)
-   [DirectX 11.2 的新功能](#new-features-for-directx-112)
-   [相關主題](#related-topics)

## <a name="direct3d-9-to-direct3d-11"></a>Direct3D 9 至 Direct3D 11

Direct3D 11 API 是以 Direct3D 10 和10.1 中所做的基礎結構改進為基礎。 從 Direct3D 9 移植至 Direct3D 11 類似于從 Direct3D 9 移至 Direct3D 10。 以下是這項工作的主要挑戰。

-   移除所有固定函式管線使用方式，以改用以 (HLSL 編譯的可程式化著色器，而不是 D3DX9) 。
-   狀態管理是以不可變的物件為基礎，而不是個別狀態切換。
-   更新以符合頂點緩衝區輸入配置和著色器簽章的嚴格連結需求。
-   將著色器資源檢視與所有材質資源產生關聯。
-   將所有影像內容對應至 DXGI \_ 格式，包括移除所有的16位色彩格式 (5/5/5/1、5/6/5、4/4/4/4) 、移除所有24位色彩格式 (8/8/8) 和嚴格的 RGB 色彩順序。
-   將全域常數狀態使用方式細分為數個小型、更有效率的常數緩衝區。

如需從 Direct3D 9 移至 Direct3D 10 的詳細資訊，請參閱 [direct3d 9 至 direct3d 10 考慮](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations)。

## <a name="direct3d-10-to-direct3d-11"></a>Direct3D 10 到 Direct3D 11

轉換撰寫為使用 Direct3D 10 或 10.1 API 的程式，是一個簡單的程式，因為 Direct3D 11 是現有 API 的延伸。 只有一個次要例外狀況 (記下以下的單色文字篩選) ，Direct3D 10/10.1 中的所有方法和功能都可在 Direct3D 11 中使用。 下列大綱說明兩個 Api 之間的差異，以協助更新現有的程式碼。 此處的主要差異包括：

-   轉譯作業 (繪製、狀態等 ) 不再是裝置介面的一部分，而是新 DeviceCoNtext 介面的一部分，以及資源對應/取消對應和裝置查詢方法。
-   Direct3D 11 包含 Direct3D 10.0 和10.1 之間的所有增強功能和變更

### <a name="enumerations-and-defines"></a>列舉和定義



| Direct3D 10                            | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DXGI \_ 格式                           | [**DXGI \_已定義數個**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)新的 DXGI 格式。<br/>                                                                                                                                                                                                                                                                                                                                |
| D3D10 \_ 建立 \_ 裝置 \_ 切換 \_ 至 \_ 參考 | [**D3D11 \_Direct3D 11 不支援建立 \_ 裝置 \_ 交換器 \_ 以 \_ 參照**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)切換至參考功能。<br/>                                                                                                                                                                                                                                                                        |
| D3D10 \_ 驅動程式 \_ 類型                    | [**D3D \_驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)請注意， [**D3D \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) 中的列舉識別碼是從 [**D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)中的識別碼重新定義。 因此，您應該確定使用列舉識別碼，而不是常值。<br/> [**D3D \_驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) 定義于 D3Dcommon 中。<br/> |
| D3D10 \_ 資源 \_ 其他 \_ 旗標            | [**D3D11 \_資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)標請注意，其中有許多旗標已重新定義，因此請務必使用列舉識別碼而非常值。<br/>                                                                                                                                                                                                                                |
| D3D10 \_ 篩選                          | [**D3D11 \_篩選**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)，請注意文字篩選 D3D10 \_ 篩選 \_ 文字 \_ 1BIT 已從 Direct3D 11 移除。 請參閱 DirectWrite。<br/>                                                                                                                                                                                                                                                                            |
| D3D11 \_ 計數器                         | [**D3D11 \_請注意**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_counter)，因為很少支援 Direct3D 11，所以已移除廠商中立的計數器。<br/>                                                                                                                                                                                                                                                                          |
| D3D10 \_ x                               | D3D11 \_ x 許多列舉和定義相同、擁有較大的限制，或有額外的值。<br/>                                                                                                                                                                                                                                                                                                               |



 

### <a name="structures"></a>結構



| Direct3D 10                              | Direct3D 11                                                                                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ 宣告 \_ \_ 專案            | [**D3D11 \_因此，宣告 \_ \_ 專案**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)會新增 Stream。<br/>                                                                  |
| D3D10 \_ BLEND \_ DESC                       | [**D3D11 \_BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)注意此結構從10個變更為10.1，以提供每個轉譯目標 blend 狀態<br/> |
| D3D10 \_ 緩衝區 \_ DESC                      | [**D3D11 \_緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)新增用於計算著色器資源的 StructureByteStride<br/>                                 |
| D3D10 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC      | [**D3D11 \_著色器 \_ 資源 \_ 視圖 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)注意：此結構已為10.1 新增了其他聯集成員<br/>    |
| D3D10 \_ 深度 \_ 樣板 \_ 視圖 \_ DESC        | [**D3D11 \_深度 \_ 樣板 \_ 視圖 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)有新的旗標成員。<br/>                                                |
| D3D10 \_ 查詢 \_ 資料 \_ 管線 \_ 統計資料 | [**D3D11 \_查詢 \_ 資料 \_ 管線 \_ 統計資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics)會加入數個新的著色器階段計數器。<br/>                  |
| D3D10 \_ x                                 | D3D11 \_ x 許多結構在這兩個 api 之間是相同的。<br/>                                                                                     |



 

### <a name="interfaces"></a>介面



| Direct3D 10        | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device       | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)和 [ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> 裝置介面分為兩個部分。 您可以使用 [**ID3D11Device：： GetImmediateCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext)來進行快速移植。<br/> "ID3D10Device：： GetTextFilterSize" 和 "SetTextFilerSize" 方法不再存在。 請參閱 DirectWrite。<br/> Create \* 著色器會為 [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)採用額外的選擇性參數。<br/> \*SetShader 和 \* GetShader 會針對 [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) (s) 取得額外的選擇性參數。<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) 會採用陣列，並計算多個輸出資料流程的進展。<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)的 NumEntries 參數限制已增加至 D3D11 \_ ，因此 \_ STREAM \_ COUNT \* D3D11 \_ 讓 \_ \_ \_ Direct3D 11 中的輸出元件計數。<br/> |
| ID3D10Buffer       | [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10SwitchToRef  | [**ID3D11SwitchToRef**](/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref)Direct3D 11 不支援切換至 ref 功能。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ID3D10Texture1D    | [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture2D    | [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture3D    | [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)地圖和取消對應方法已移至 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)，而所有對應方法都使用 [**D3D11 \_ 對應的 \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) ，而不是 void \* \* 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ID3D10Asynchronous | [**ID3D11Asynchronous**](/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous)Begin、End 和 >id3d11devicecoNtext 已移至 [](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10x            | 在這兩個 Api 之間 ID3D11x 許多介面相同。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="other-related-technologies"></a>其他相關技術



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>10/10.1 解決方案</th>
<th>11個解決方案</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HLSL 編譯器 (D3D10Compile *、D3DX10Compile*) 和著色器反映 api</td>
<td>D3DCompiler (參閱 D3DCompiler) 
<blockquote>
[!Note]<br />
針對 Windows Store 應用程式， <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">D3DCompiler api</a> 僅支援開發，不支援部署。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>效果10</td>
<td><a href="https://github.com/Microsoft/FX11">效果 11</a> 可作為共用來源上線。
<blockquote>
[!Note]<br />
此解決方案不適合 Windows Store 應用程式，因為它需要在執行時間 (部署) 的 <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">D3DCompiler api</a> 。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DX9/D3DX10 數學</td>
<td><a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a></td>
</tr>
<tr class="even">
<td>D3DX10</td>
<td>舊版 DirectX SDK <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a>、 <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a>和 <a href="https://github.com/Microsoft/DirectXMesh">DirectXMesh</a> 中的 D3DX11 提供舊版 D3DX10 和 D3DX11 程式庫中許多技術的替代方案。<br/> <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> 和 <a href="/windows/desktop/DirectWrite/direct-write-portal">DirectWrite</a> 為轉譯樣式的線條和字型提供高品質的支援。<br/></td>
</tr>
</tbody>
</table>



 

如需舊版 DirectX SDK 的詳細資訊，請參閱 [什麼是 DIRECTX sdk？](/windows/desktop/directx-sdk--august-2009-)。

## <a name="direct3d-101-to-direct3d-11"></a>Direct3D 10.1 至 Direct3D 11

Direct3D 10.1 是 Direct3D 10 介面的延伸模組，而且 direct3d 10.1 的所有功能都可在 Direct3D 11 中使用。 從10.1 到11的大部分移植都已在上述從10移至11的程式中解決。

### <a name="enumerations-and-defines"></a>列舉和定義



| Direct3D 10。1          | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 功能 1-1 \_ \_ | [**D3D \_功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)完全相同，但定義于 D3DCommon 中，加上 \_ \_ 適用于11類別硬體的 d3d 功能等級 \_ 11 0 和 \_ d3d \_ 功能 \_ 層級 \_ 9 \_ 1、D3D \_ 功能 \_ 層級 \_ 9 \_ 2，以及 \_ \_ 10level9 的 d3d 功能等級 \_ 9 \_ 3<br/>  (D3D10 \_ 功能 \_ 層級 \_ 9 \_ 1、D3D10 \_ 功能 \_ 等級 \_ 9 \_ 2，以及 D3D10 \_ 功能 \_ 等級 \_ 9 3，也已 \_ 新增至10.1 至 D3D10 \_ 1 .h) <br/> |



 

### <a name="structures"></a>結構



| Direct3D 10。1                        | Direct3D 11                                                                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ BLEND \_ DESC1                  | [**D3D11 \_BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)11 版等同于10.1。<br/>                                 |
| D3D10 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC1 | [**D3D11 \_著色器 \_ 資源 \_ 視圖 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)：11版本等同于10.1。<br/> |



 

### <a name="interfaces"></a>介面



| Direct3D 10。1             | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device1             | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)和 [ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> 裝置介面分為兩個部分。 您可以使用 [**ID3D11Device：： GetImmediateCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext)來進行快速移植。<br/> "ID3D10Device：： GetTextFilterSize" 和 "SetTextFilerSize" 方法不再存在。 請參閱 DirectWrite。<br/> Create \* 著色器會為 [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)採用額外的選擇性參數。<br/> \*SetShader 和 \* GetShader 會針對 [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) (s) 取得額外的選擇性參數。<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) 會採用陣列，並計算多個輸出資料流程的進展。<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)的 NumEntries 參數限制已增加至 D3D11 \_ ，因此 \_ STREAM \_ COUNT \* D3D11 \_ 讓 \_ \_ \_ Direct3D 11 中的輸出元件計數。<br/> |
| ID3D10BlendState1         | [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ID3D10ShaderResourceView1 | [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="new-features-for-direct3d-11"></a>Direct3D 11 的新功能

當您的程式碼更新為使用 Direct3D 11 API 時，有許多 [新功能](direct3d-11-features.md) 需要考慮。

-   透過命令清單和多個內容進行多執行緒轉譯
-   使用計算著色器 (使用4.0、4.1 或5.0 著色器設定檔來執行 advanced 演算法) 
-   新的11類別硬體功能：
    -   HLSL 著色器模型5。0
    -   動態著色器連結
    -   鑲嵌式和網域著色器
    -   新的區塊壓縮格式：適用于 HDR 映射的 BC6H，適用于高精確度標準影像的 BC7
-   透過適用于 Windows Vista 和 Windows 7 的低端影片硬體支援的 DIrect3D 11 API，利用 [10level9 技術](overviews-direct3d-11-devices-downlevel.md) 在許多著色器模型2.0 和著色器模型3.0 裝置上呈現。
-   利用變形軟體轉譯裝置。

## <a name="new-features-for-directx-111"></a>DirectX 11.1 的新功能

Windows 8 包含在實作為 DirectX 圖形程式碼時要考慮的進一步 DirectX 圖形增強功能，其中包括 [Direct3D 11.1](direct3d-11-features.md)、 [DXGI 1.2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)、 [Windows 顯示驅動程式模型 (WDDM) 1.2](/windows-hardware/drivers/display/wddm-in-windows-8)、 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 11.1 硬體、Direct2D 裝置內容，以及其他改善。

在 windows 7 上，也可以透過 windows 7 的平臺更新（可透過[windows 7 的平臺更新](https://support.microsoft.com/kb/2670838)[取得）來](/windows/desktop/direct3darticles/platform-update-for-windows-7)取得[Direct3D 11.1](direct3d-11-features.md)的部分支援。

## <a name="new-features-for-directx-112"></a>DirectX 11.2 的新功能

Windows 8.1 包括 [Direct3D 11.2](direct3d-11-2-features.md)、 [DXGI 1.3](/windows/desktop/direct3ddxgi/dxgi-1-3-improvements)及其他改良功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的程式設計指南](dx-graphics-overviews.md)
</dt> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>


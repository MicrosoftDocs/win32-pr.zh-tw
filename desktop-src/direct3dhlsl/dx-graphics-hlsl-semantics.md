---
title: 語意
description: 語義是附加至著色器輸入或輸出的字串，該字串會傳達有關參數之使用用途的資訊。
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- " (DirectX HLSL) 的 BINORMAL、語義"
- " (DirectX HLSL) 的 BLENDINDICES、語義"
- " (DirectX HLSL) 的 BLENDWEIGHT、語義"
- " (DirectX HLSL) 的色彩、語義"
- " (DirectX HLSL) 的霧化、語義"
- " (DirectX HLSL) 的 POSITIONT、語義"
- " (DirectX HLSL) 的 PSIZE、語義"
- " (DirectX HLSL) 的正切函數、語義"
- " (DirectX HLSL) 的 TESSFACTOR、語義"
- " (DirectX HLSL) 的 TEXCOORD、語義"
- " (DirectX HLSL) 的 VFACE、語義"
- " (DirectX HLSL) 的 VPOS、語義"
- System-Value 語義
- 系統值語義
- " (DirectX HLSL) 的 ClipDistance、語義"
- " (DirectX HLSL) 的涵蓋範圍、語義"
- " (DirectX HLSL) 的 CullDistance、語義"
- " (DirectX HLSL) 的深度、語義"
- 'InstanceID、語義 (DirectX HLSL) '
- " (DirectX HLSL) 的 IsFrontFace、語義"
- " (DirectX HLSL 的位置、語義) "
- " (DirectX HLSL) 的 PrimitiveID、語義"
- " (DirectX HLSL) 的 RenderTargetArrayIndex、語義"
- " (DirectX HLSL) 的目標、語義"
- " (DirectX HLSL) 的 SampleIndex、語義"
- " (DirectX HLSL) 的 VertexID、語義"
- " (DirectX HLSL) 的 ViewportArrayIndex、語義"
- SV_ClipDistance， (DirectX HLSL) 的語義
- SV_CullDistance， (DirectX HLSL) 的語義
- SV_Depth， (DirectX HLSL) 的語義
- SV_DepthGreaterEqual， (DirectX HLSL) 的語義
- SV_DepthLessEqual， (DirectX HLSL) 的語義
- SV_IsFrontFace， (DirectX HLSL) 的語義
- SV_Position， (DirectX HLSL) 的語義
- SV_RenderTargetArrayIndex， (DirectX HLSL) 的語義
- SV_Target， (DirectX HLSL) 的語義
- SV_ViewportArrayIndex， (DirectX HLSL) 的語義
- SV_InstanceID， (DirectX HLSL) 的語義
- SV_PrimitiveID， (DirectX HLSL) 的語義
- SV_VertexID， (DirectX HLSL) 的語義
- SV_Coverage， (DirectX HLSL) 的語義
- SV_SampleIndex， (DirectX HLSL) 的語義
- 'SV_InnerCoverage，semanitcs (DirectX HLSL) '
- SV_StencilRef， (DirectX HLSL) 的語義
- SV_GroupID， (DirectX HLSL) 的語義
- SV_GroupThreadID， (DirectX HLSL) 的語義
- SV_DispatchThreadID (DirectX HLSL) 的語義
- SV_GroupIndex， (DirectX HLSL) 的語義
- SV_OutputControlPointID， (DirectX HLSL) 的語義
- SV_TessFactor， (DirectX HLSL) 的語義
- SV_InsideTessFactor， (DirectX HLSL) 的語義
- SV_DomainLocation， (DirectX HLSL) 的語義
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 510f718608363c547c8333279826cc8bac141358
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195799"
---
# <a name="semantics"></a>語意

語義是附加至著色器輸入或輸出的字串，該字串會傳達有關參數之使用用途的資訊。 在著色器階段之間傳遞的所有變數都需要有語義。 將語義新增至著色器變數的語法如下所示 ([變數語法 (DIRECTX HLSL) ](dx-graphics-hlsl-variable-syntax.md)) 。

一般情況下，管線階段之間傳遞的資料會完全是泛型，且不會由系統唯一解釋;允許使用無特殊意義的任意語義。 在 Direct3D 10 和更新版本中 (的參數) 包含這些特殊的語法，稱為 [系統值的語法](#system-value-semantics)。

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>Direct3D 9 和 Direct3D 10 和更新版本中支援的語義

Direct3D 9 和 Direct3D 10 和更新版本都支援下列類型的語法。

- [頂點著色器語義](#vertex-shader-semantics)
- [圖元著色器語義](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>頂點著色器語義

這些語義在附加至頂點著色器參數時有意義。 Direct3D 9 和 Direct3D 10 和更新版本都支援這些語義。

| 輸入 | 描述 | 類型 |
|-|-|-|
| BINORMAL \[ n\] | Binormal | float4 |
| BLENDINDICES \[ n\] | Blend 索引 | uint |
| BLENDWEIGHT \[ n\] | Blend 加權 | FLOAT |
| 色彩 \[ n\] | 擴散和反射色彩 | float4 |
| 一般 \[ n\] | 一般向量 | float4 |
| 位置 \[ n\] | 物件空間中的頂點位置。 | float4 |
| POSITIONT | 已轉換的頂點位置。 | float4 |
| PSIZE \[ n\] | 點大小 | FLOAT |
| 正切函數 \[ n\] | 正切值 | float4 |
| TEXCOORD \[ n\] | 材質座標 | float4 |
| 輸出 | 描述 | 類型 |
| 色彩 \[ n\] | 擴散或反射色彩 | float4 |
| 霧 | 頂點霧化 | FLOAT |
| 位置 \[ n\] | 頂點在同質空間中的位置。 藉由將 (x、y、z) 除以 w 來計算螢幕空間中的位置。 每個頂點著色器都必須寫出具有此語義的參數。 | float4 |
| PSIZE | 點大小 | FLOAT |
| TESSFACTOR \[ n\] | 鑲嵌因數 | FLOAT |

`n` 這是介於0和支援的資源數目之間的選擇性整數。 例如，POSITION0、TEXCOORD1 等。

### <a name="pixel-shader-semantics"></a>圖元著色器語義

附加至圖元著色器輸入參數時，這些語義具有意義。 Direct3D 9 和 Direct3D 10 和更新版本都支援這些語義。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>輸入</th>
<th>描述</th>
<th>類型</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>色彩 [n]</td>
<td>擴散或反射色彩。</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD [n]</td>
<td>材質座標</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>浮點純量，表示後端的基本。 負數值會向後往上，而正值則會朝相機表示。
<blockquote>
[!Note]<br />
此語義適用于 <a href="dx-graphics-hlsl-sm3.md">Direct3D 9 著色器模型 3.0</a>。 針對 Direct3D 10 和更新版本，請改用 <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace</a> 。
</blockquote>
<br/></td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>圖元位置 (x，y) 在螢幕空間中。 若要將使用此語義) 的 Direct3D 9 著色器 (轉換為 Direct3D 10 和更新版本的著色器，請參閱 <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">direct3d 9 VPOS 和 direct3d 10 SV_Position</a>) </td>
<td>float2</td>
</tr>
<tr class="odd">
<td>輸出</td>
<td>描述</td>
<td>類型</td>
</tr>
<tr class="even">
<td>色彩 [n]</td>
<td>輸出色彩</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>深度 [n]</td>
<td>輸出深度</td>
<td>FLOAT</td>
</tr>
</tbody>
</table>

`n` 這是介於0和支援的資源數目之間的選擇性整數。 例如，PSIZE0、COLOR1 等。

色彩語義僅適用于著色器相容性模式， (也就是使用 D3D10 著色器建立著色器時，會 \_ \_ 啟用回溯 \_ \_ 相容性) 。

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>僅支援 Direct3D 10 和更新版本的語義。

下列類型的語義是針對 Direct3D 10 新引進的，無法供 Direct3D 9 使用。

- [系統值語義](#system-value-semantics)

### <a name="system-value-semantics"></a>System-Value 語義

系統值的語法是 Direct3D 10 的新手。 所有系統值的開頭都是 SV \_ 前置詞，一般範例是 sv \_ 位置，它是由轉譯器階段所解讀。 系統值在管線的其他部分是有效的。 例如，您 \_ 可以將 SV 位置指定為頂點著色器和輸出的輸入。 圖元著色器只能寫入具有 SV \_ Depth 和 sv \_ 目標系統值語義的參數。

其他系統值 (SV \_ VertexID、sv \_ INSTANCEID、sv \_ IsFrontFace) 只能輸入至管線中可解讀特定值的第一個使用中著色器，之後著色器函式必須將這些值傳遞至後續階段。

SV \_ PrimitiveID 是此規則的例外狀況，只是要在管線中可解讀特定值的第一個使用中著色器中輸入，硬體可以提供與輪廓著色器階段、網域著色器階段的輸入相同的識別碼值，以及在該階段為第一個啟用：幾何著色器階段或圖元著色器階段。

如果已啟用鑲嵌，則會顯示輪廓著色器階段和網域著色器階段。 針對特定的修補程式，相同的 PrimitiveID 適用于修補程式的輪廓著色器調用，以及所有鑲嵌的網域著色器調用。 相同的 PrimitiveID 也會傳播至下一個作用中階段;幾何-著色器階段或圖元著色器階段（若已啟用）。

如果幾何著色器輸入 SV \_ PrimitiveID，而且它可以輸出零或一個或多個每個調用的基本類型，則 \_ 如果後續的圖元著色器輸入 sv PrimtiveID，著色器就必須為每個輸出基本型別設計其 SV PrimitiveID 值的選項 \_ 。

另一個範例是， \_ 在頂點著色器階段無法解讀 SV PrimitiveID，因為頂點可以是多個基本專案的成員。

這些語義已新增至 Direct3D 10;Direct3D 9 不提供這些功能。

轉譯器階段的系統值語義。

| System-Value 語義 | 描述 | 類型 |
|-|-|-|
| SV \_ ClipDistance \[ n\] | 剪輯距離資料。 SV \_ ClipDistance 值都假設為與平面之間的 float32 帶正負號距離。 基本設定只會叫用以圖元為單位的點陣化，其中的插補平面距離 (s) >= 0。 您可以將一個或多個頂點專案的多個元件 () 為 SV ClipDistance，以同時實作為多個剪輯平面 \_ 。 合併的剪輯和挑選距離值最多隻是 D3D 剪輯或挑選距離 \# \_ 元素計數暫存器中最多的 d3d 剪輯 \_ 或 \_ 挑選 \_ 距離 \_ 計陣列件 \# \_ \_ \_ \_ \_ \_ 。 適用于所有要讀取或寫入的著色器，但可以寫入值但不會將它視為輸入的頂點著色器除外。<br/> **Clipplanes** 屬性的運作方式類似 SV \_ ClipDistance，但適用于所有硬體 [功能層級](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)9 \_ x 和更高。 如需詳細資訊，請參閱「 [功能等級9硬體上的使用者剪輯平面](./user-clip-planes-on-10level9.md)」。<br/> | FLOAT |
| SV \_ CullDistance \[ n\] | 挑選距離資料。 當 () s 的頂點元素) 元件 (時，若有此標籤，則這些值會假設為與平面之間的 float32 簽署距離。 如果基本專案中的所有頂點的平面距離 () < 0，則會完全捨棄基本專案。 您可以將多個元件 () 一個或多個頂點元素作為 SV CullDistance，來同時使用多個挑選平面 \_ 。 合併的剪輯和挑選距離值最多隻是 D3D 剪輯或挑選距離 \# \_ 元素計數暫存器中最多的 d3d 剪輯 \_ 或 \_ 挑選 \_ 距離 \_ 計陣列件 \# \_ \_ \_ \_ \_ \_ 。 適用于所有要讀取或寫入的著色器，但可以寫入值但不會將它視為輸入的頂點著色器除外。<br/> | FLOAT |
| SV \_ 涵蓋範圍 | 可以在輸入、輸出或兩個圖元著色器上指定的遮罩。 <br/> 針對 \_ 圖元著色器的 SV 涵蓋範圍，在 ps \_ 4 \_ 1 或更高版本上支援輸出。 <br/> 針對 \_ 圖元著色器的 SV 涵蓋範圍，輸入需要 ps \_ 5 \_ 0 或更高的版本。 <br/> | uint |
| SV \_ 深度 | 深度緩衝區資料。 可以透過圖元著色器寫入。 | FLOAT |
| SV \_ DepthGreaterEqual | 在圖元著色器中，只要輸出深度大於或等於轉譯器所決定的值，就會允許輸出深度。 啟用調整深度，而不停用早期 Z。 | FLOAT |
| SV \_ DepthLessEqual | 在圖元著色器中，只要輸出深度小於或等於轉譯器所決定的值，就會允許輸出深度。 啟用調整深度，而不停用早期 Z。 | FLOAT |
| [SV \_ DispatchThreadID](sv-dispatchthreadid.md) | 針對群組的每個維度，定義分派呼叫內的全域執行緒位移。 可作為計算著色器的輸入。  (唯讀)  | uint3 |
| [SV \_ DomainLocation](sv-domainlocation.md) | 定義要評估之目前網域點的輪廓上的位置。 可作為網域著色器的輸入。  (唯讀)  | float2 \| 3 |
| [SV \_ GroupID](sv-groupid.md) | 定義分派呼叫內的群組位移，每個分派呼叫的維度。 可作為計算著色器的輸入。  (唯讀)  | uint3 |
| [SV \_ GroupIndex](sv-groupindex.md) | 為指定群組內的指定執行緒提供壓平合併索引。 可作為計算著色器的輸入。  (唯讀)  | uint |
| [SV \_ GroupThreadID](sv-groupthreadid.md) | 定義群組中的執行緒位移（每個群組的維度）。 可作為計算著色器的輸入。  (唯讀)  | uint3 |
| [SV \_ GSInstanceID](sv-gsinstanceid.md) | 定義幾何著色器的實例。 可作為幾何著色器的輸入。 需要實例，因為幾何著色器可以在相同幾何基本型別上叫用最多32次。 | uint |
| SV \_ InnerCoverage | 代表低估的保守式柵格化資訊 (亦即，是否保證可完全涵蓋) 的圖元。 圖元著色器可以讀取或寫入。 | |
| [SV \_ InsideTessFactor](sv-insidetessfactor.md) | 定義修補程式介面內的鑲嵌量。 可在用於撰寫的輪廓著色器中使用，並可在用於讀取的網域著色器中使用。 | float \| float \[ 2\] |
| SV \_ InstanceID | 執行時間自動產生的每個實例識別碼 (請參閱 [使用 System-Generated 值 (Direct3D 10) ](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)) 。 適用于所有著色器。 | |
| SV \_ IsFrontFace | 指定三角形是否為前方。 對於線條和點而言，IsFrontFace 的值為 true。 例外狀況是繪製出三角形 (線框模式) 的線條，其設定 IsFrontFace 的方式與在固態模式中將三角形進行柵格化的方式相同。 可由幾何著色器撰寫，並由圖元著色器讀取。 | bool |
| [SV \_ OutputControlPointID](sv-outputcontrolpointid.md) | 藉由對輪廓著色器的主要進入點叫用來定義所要操作的控制點識別碼索引。 只能由輪廓著色器讀取。 | uint |
| SV \_ 位置 | \_針對著色器的輸入宣告 SV 位置時，它可以有兩個指定的插補模式之一： linearNoPerspective 或 linearNoPerspectiveCentroid，後者會在進行多取樣消除鋸齒時，提供距心的貼齊 xyzw 值。 在著色器中使用時，SV \_ 位置會描述圖元位置。 適用于所有著色器，以取得具有0.5 位移的圖元中心。 | float4 |
| SV \_ PrimitiveID | 執行時間自動產生的每個基本識別碼 (請參閱 [使用 System-Generated 值 (Direct3D 10) ](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)) 。 可以由幾何或圖元著色器寫入，然後由幾何、圖元、輪廓或網域著色器讀取。 | uint |
| SV \_ RenderTargetArrayIndex | 呈現目標陣列索引。 套用至幾何著色器輸出，並指出圖元著色器將繪製基本的轉譯目標陣列配量。 SV \_ RenderTargetArrayIndex 只有在轉譯目標是陣列資源時才有效。 此語義只適用于基本類型;如果基本型別有一個以上的頂點，則會使用來自前置頂點的值。 此值也會指出深度/樣板視圖的哪個陣列配量用於讀/寫用途。<br/> 可以從幾何著色器撰寫，並由圖元著色器讀取。<br/> 如果 [D3D11_FEATURE_DATA_D3D11_OPTIONS3：： VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) 為 `true` ，則 SV \_ RenderTargetArrayIndex 會套用至任何饋送于轉譯器的著色器。 | uint |
| SV \_ SampleIndex | 範例頻率索引資料。 只有圖元著色器可以讀取或寫入。 | uint |
| SV \_ StencilRef | 表示目前的圖元著色器樣板參考值。 只能由圖元著色器寫入。 | uint |
| SV \_ 目標 \[ n \] ，其中 0 <= n <= 7 | 將儲存在轉譯目標中的輸出值。 索引會指出要寫入8個可能系結的轉譯目標。 此值適用于所有著色器。 | float \[ 2 \| 3 \| 4\] |
| [SV \_ TessFactor](sv-tessfactor.md) | 在修補程式的每個邊緣上定義鑲嵌量。 可在輪廓著色器中撰寫，並在網域著色器中讀取。 | float \[ 2 \| 3 \| 4\] |
| SV \_ VertexID | 執行時間自動產生的每個頂點識別碼 (請參閱 [使用 System-Generated 值 (Direct3D 10) ](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)) 。 僅可作為頂點著色器的輸入。 | uint |
| SV \_ ViewportArrayIndex | 視口陣列索引。 套用至幾何著色器輸出，並指出要針對目前寫出的基本物件使用哪些區。圖元著色器可以讀取。 在傳遞給轉譯器之前，將會針對索引所指定的視口來轉換和裁剪基本物件。 此語義只適用于基本類型;如果基本型別有一個以上的頂點，則會使用來自前置頂點的值。 <br/> 如果 [D3D11_FEATURE_DATA_D3D11_OPTIONS3：： VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) 為 `true` ，則 SV \_ ViewportArrayIndex 會套用至任何饋送于轉譯器的著色器。 | uint |
| SV \_ ShadingRate | 透過陰影比率 [值](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)，定義由一個圖元著色器叫用的圖元數，用於 [變數網底比例第2層](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) 或更高的裝置。 可以從圖元著色器讀取。 可以從頂點或幾何著色器寫入。 | uint |

### <a name="limitations-when-writing-sv_depth"></a>寫入 SV 深度時的限制 \_ ：

- 當您在 D3D10 轉譯器 [**\_ \_ DESC**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)中 (MultisampleEnable 為 **TRUE** 時，) 和使用圖元著色器) 寫入深度 (值時，會在 [深度測試](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md)中使用寫出的單一值; 因此，在取樣時，以較高解析度轉譯基本邊緣的能力會遺失。
- 使用動態流程式控制制時，無法在編譯時期判斷在某些路徑中寫入 SV 深度的著色器是否 \_ 保證 \_ 在每次執行時都寫入 sv 深度。 \_當宣告的結果為未定義的行為時，無法寫入 SV 深度 (可能會包括捨棄圖元) 。
- 任何包含 +/-INF 和 NaN 的 float32 值都可以寫入 SV \_ 深度。
- \_執行雙重來源色彩混合時，寫入 SV 深度仍是有效的。

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>從 Direct3D 9 遷移至 Direct3D 10 和更新版本

將程式碼從 Direct3D 9 遷移至 Direct3D 10 和更新版本時，應考慮下列問題：

### <a name="mapping-to-direct3d-9-semantics"></a>對應至 Direct3D 9 語義

其中一些 Direct3D 10 和更新版本的語義會直接對應至 Direct3D 9 語義。

| Direct3D 10 語義 | Direct3D 9 對等語義 |
|-|-|
| SV \_ 深度 | DEPTH |
| SV \_ 位置 | POSITION |
| SV \_ 目標 | 顏色 |

> [!]Direct3D 9 開發人員注意事項：針對 Direct3D 9 目標，著色器語義必須對應到有效的 Direct3D 9 語義。 針對回溯相容性 POSITION0 (及其 variant 名稱) 被視為 SV \_ 位置，會將色彩視為 sv \_ 目標。

- [對應至 Direct3D 9 語義](#mapping-to-direct3d-9-semantics)
- [Direct3D 9 VPOS 和 Direct3D 10 SV \_ 位置](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [HLSL 中的使用者剪輯平面](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Direct3D 9 VPOS 和 Direct3D 10 SV \_ 位置

D3D10 語義 SV \_ 位置提供類似于 Direct3D 9 著色器模型 3 VPOS 語義的功能。 比方說，在 Direct3D 9 中，使用螢幕空間座標的圖元著色器會使用下列語法：

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

已為著色器模型3支援新增 VPOS，以指定螢幕空間座標，因為位置語義適用于物件空間座標。

在 Direct3D 10 和更新版本中，在 \_ 圖元著色器的內容中使用時，SV 位置語義 () 指定螢幕空間座標 (位移 0.5) 。 因此，Direct3D 9 著色器大致上是相等的 (而不會計入0.5 位移) 如下所示：

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

從 Direct3D 9 遷移至 Direct3D 10 和更新版本時，您必須在轉譯著色器時留意到此情況。

### <a name="user-clip-planes-in-hlsl"></a>HLSL 中的使用者剪輯平面

從 Windows 8 開始，您可以 [在 HLSL 函](dx-graphics-hlsl-function-syntax.md)式宣告（而不是 SV ClipDistance）中使用 **clipplanes** 函式屬性， \_ 讓您的著色器能在 [功能層級](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)9 \_ x 以及功能層級10和更高版本上運作。 如需詳細資訊，請參閱「 [功能等級9硬體上的使用者剪輯平面](./user-clip-planes-on-10level9.md)」。

## <a name="related-topics"></a>相關主題

* [語言語法](dx-graphics-hlsl-language-syntax.md)
* [ (DirectX HLSL) 的變數 ](dx-graphics-hlsl-variables.md)
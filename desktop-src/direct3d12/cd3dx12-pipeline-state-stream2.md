---
title: 'CD3DX12_PIPELINE_STATE_STREAM2 結構 (D3dx12 .h) '
description: 協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。
keywords:
- CD3DX12_PIPELINE_STATE_STREAM2 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM2
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: 18b662217f5e2a59c7925e0f401a9288ea710e8a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812338"
---
# <a name="cd3dx12_pipeline_state_stream2-structure"></a>CD3DX12_PIPELINE_STATE_STREAM2 結構

協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。 請參閱 [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 和 [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)。

**CD3DX12_PIPELINE_STATE_STREAM2** 支援作業系統組建 19041 + (，其中有) 的網格著色器管線。

## <a name="syntax"></a>語法

```cpp
struct CD3DX12_PIPELINE_STATE_STREAM2
{
    CD3DX12_PIPELINE_STATE_STREAM2();
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS Flags;
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK NodeMask;
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE pRootSignature;
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT InputLayout;
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE IBStripCutValue;
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY PrimitiveTopologyType;
    CD3DX12_PIPELINE_STATE_STREAM_VS VS;
    CD3DX12_PIPELINE_STATE_STREAM_GS GS;
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT StreamOutput;
    CD3DX12_PIPELINE_STATE_STREAM_HS HS;
    CD3DX12_PIPELINE_STATE_STREAM_DS DS;
    CD3DX12_PIPELINE_STATE_STREAM_PS PS;
    CD3DX12_PIPELINE_STATE_STREAM_AS AS;
    CD3DX12_PIPELINE_STATE_STREAM_MS MS;
    CD3DX12_PIPELINE_STATE_STREAM_CS CS;
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC BlendState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 DepthStencilState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT DSVFormat;
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER RasterizerState;
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC SampleDesc;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK SampleMask;
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO CachedPSO;
    CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING ViewInstancingDesc;
    D3D12_GRAPHICS_PIPELINE_STATE_DESC GraphicsDescV0() const noexcept;
    D3D12_COMPUTE_PIPELINE_STATE_DESC ComputeDescV0() const noexcept;
};
```

## <a name="members"></a>成員

`CD3DX12_PIPELINE_STATE_STREAM2`

預設建構函式。 建立新的、未初始化的 **CD3DX12_PIPELINE_STATE_STREAM2** 實例。

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC&)`

建立新實例的函式， **CD3DX12_PIPELINE_STATE_STREAM2** 以 [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 結構的內容初始化。

然後，您必須手動設定網格和放大著色器，因為它們沒有 **D3D12_GRAPHICS_PIPELINE_STATE_DESC** 的標記法。

`CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC&)`

建立新實例的函式， **CD3DX12_PIPELINE_STATE_STREAM2** 以 [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) 結構的內容初始化。

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC&)`

建立新實例的函式， **CD3DX12_PIPELINE_STATE_STREAM2** 以 [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) 結構的內容初始化。

`Flags`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_FLAGS](cd3dx12-pipeline-state-stream-flags.md)**

例如， (旗標，表示應使用其他資訊來編譯管線狀態，以協助進行) 的偵錯工具。

`NodeMask`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK](cd3dx12-pipeline-state-stream-node-mask.md)**

描述管線狀態節點遮罩，用來識別在多個介面卡案例中，PSO 適用之裝置)  (實體介面卡的節點;遮罩中的每個位都對應至單一節點。 若為單一介面卡案例，請使用0。

`pRootSignature`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE](cd3dx12-pipeline-state-stream-root-signature.md)**

描述根簽章。

`InputLayout`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT](cd3dx12-pipeline-state-stream-input-layout.md)**

描述輸入組合語言階段的輸入緩衝區格式

`IBStripCutValue`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)**

描述輸入緩衝區的特殊索引值，這個值表示使用三角形區域間拓撲時，剪下的 (不連續) 。

`PrimitiveTopologyType`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY](cd3dx12-pipeline-state-stream-primitive-topology.md)**

描述基本拓撲及其順序。

`VS`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_VS](cd3dx12-pipeline-state-stream-vs.md)**

描述頂點著色器。

`GS`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_GS](cd3dx12-pipeline-state-stream-gs.md)**

描述幾何著色器。

`StreamOutput`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT](cd3dx12-pipeline-state-stream-stream-output.md)**

描述串流輸出緩衝區。

`HS`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_HS](cd3dx12-pipeline-state-stream-hs.md)**

描述輪廓著色器。

`DS`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_DS](cd3dx12-pipeline-state-stream-ds.md)**

描述網域著色器。

`PS`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_PS](cd3dx12-pipeline-state-stream-ps.md)**

描述圖元著色器。

`AS`

類型： **CD3DX12_PIPELINE_STATE_STREAM_AS**

描述放大著色器。

`MS`

類型： **CD3DX12_PIPELINE_STATE_STREAM_MS**

描述網格著色器。

`CS`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_CS](cd3dx12-pipeline-state-stream-cs.md)**

描述計算著色器。

`BlendState`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC](cd3dx12-pipeline-state-stream-blend-desc.md)**

描述 blend 狀態。

`DepthStencilState`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1](cd3dx12-pipeline-state-stream-depth-stencil1.md)**

描述深度範本的狀態。

`DSVFormat`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT](cd3dx12-pipeline-state-stream-depth-stencil-format.md)**

描述深度樣板格式。

`RasterizerState`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER](cd3dx12-pipeline-state-stream-rasterizer.md)**

描述轉譯器的狀態。

`RTVFormats`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS](cd3dx12-pipeline-state-stream-render-target-formats.md)**

描述呈現目標格式。

`SampleDesc`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC](cd3dx12-pipeline-state-stream-sample-desc.md)**

描述範例計數和品質。

`SampleMask`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK](cd3dx12-pipeline-state-stream-sample-mask.md)**

描述搭配 blend 狀態使用的範例遮罩。

`CachedPSO`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO](cd3dx12-pipeline-state-stream-cached-pso.md)**

描述快取的 PSO。

`ViewInstancingDesc`

類型： **[CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING](cd3dx12-pipeline-state-stream-view-instancing.md)**

描述視圖實例設定。

`GraphicsDescV0`

傳回 [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)。

以傳值方式將 **CD3DX12_PIPELINE_STATE_STREAM2** 物件的內容傳回為 **D3D12_GRAPHICS_PIPELINE_STATE_DESC** 結構。 **D3D12_GRAPHICS_PIPELINE_STATE_DESC** 不包含 *CS* 成員，因此該值會在轉換時遺失。

`ComputeDescV0`

傳回 [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)。

以傳值方式將 **CD3DX12_PIPELINE_STATE_STREAM2** 物件的內容傳回為 **D3D12_COMPUTE_PIPELINE_STATE_DESC** 結構。 **D3D12_COMPUTE_PIPELINE_STATE_DESC** 不包含 *InputLayout*、 *IBStripCutValue*、 *PrimitiveTopologyType*、 *VS*、 *GS*、 *>streamoutput*、 *HS*、 *DS*、 *PS*、 *BlendState*、 *DepthStencilState*、 *DSVFormat*、 *RasterizerState*、 *NumRootSignature*、RTVFormats、 ** SampleDesc 和 *SampleMask* 等成員，因此這些值會在轉換時遺失。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)

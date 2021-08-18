---
title: 'CD3DX12_PIPELINE_STATE_STREAM 結構 (D3dx12 .h) '
description: '協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。 請參閱 D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ desc 和 D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ desc。 |CD3DX12_PIPELINE_STATE_STREAM 結構 (D3dx12 .h) '
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- CD3DX12_PIPELINE_STATE_STREAM 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e45c46c39a21aaeb53a2980fa3c082947e92cd5bb4ab3eccbbb225001a6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733980"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程結構

協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。 請參閱 [**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 和 [**D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)。

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程支援 Windows 10 Creators Update 和更新版本，但不支援秋季建立者更新的新功能，例如 view 實例。 若要支援秋季建立者更新的功能，請改用 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) 。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 ()**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 (const D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ desc& desc)**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程的新實例 \_ \_ ，並以從 **CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程** 結構複製的值進行初始化。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 (const D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ desc& DESC)**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程的新實例 \_ \_ ，並以從 **CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程** 結構複製的值進行初始化。

</dd> <dt>

**GraphicsDescV0 ()**
</dt> <dd>

以傳值方式將 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程物件的內容傳回為 D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC 結構。 請注意，D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC 不包含 **CS** 成員，因此此值會在轉換時遺失。

</dd> <dt>

**ComputeDescV0 ()**
</dt> <dd>

以傳值方式將 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程物件的內容傳回為 D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ DESC 結構。 請注意， \_ D3D12 \_ 計算 \_ 管線狀態 \_ DESC 不包含 **InputLayout**、 **IBStripCutValue**、 **PrimitiveTopologyType**、 **VS**、 **GS**、 **>streamoutput**、 **HS**、 **DS**、 **PS**、 **BlendState**、 **DepthStencilState**、 **DSVFormat**、 **RasterizerState**、 **NumRootSignature**、 **RTVFormats**、SampleDesc 或 **SampleMask** 成員，因此這些值會在轉換時遺失。

</dd> <dt>

**旗標**
</dt> <dd>

描述管線狀態旗標，這些旗標可控制功能，例如「工具調試」。

</dd> <dt>

**NodeMask**
</dt> <dd>

描述管線狀態節點遮罩，用來識別在多個介面卡案例中，PSO 適用之裝置)  (實體介面卡的節點;遮罩中的每個位都對應至單一節點。 若為單一介面卡案例，請將此值設定為0。

</dd> <dt>

**pRootSignature**
</dt> <dd>

描述根簽章。

</dd> <dt>

**InputLayout**
</dt> <dd>

描述輸入組合語言階段的輸入緩衝區格式

</dd> <dt>

**IBStripCutValue**
</dt> <dd>

描述輸入緩衝區的特殊索引值，這個值表示使用三角形區域間拓撲時，剪下的 (不連續) 。

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

描述基本拓撲及其順序。

</dd> <dt>

**與**
</dt> <dd>

描述頂點著色器。

</dd> <dt>

**GS**
</dt> <dd>

描述幾何著色器。

</dd> <dt>

**>streamoutput**
</dt> <dd>

描述串流輸出緩衝區。

</dd> <dt>

**房 協**
</dt> <dd>

描述輪廓著色器。

</dd> <dt>

**DS**
</dt> <dd>

描述網域著色器。

</dd> <dt>

**PS**
</dt> <dd>

描述圖元著色器。

</dd> <dt>

**CS**
</dt> <dd>

描述計算著色器。

</dd> <dt>

**BlendState**
</dt> <dd>

描述 blend 狀態。

</dd> <dt>

**DepthStencilState**
</dt> <dd>

描述深度範本的狀態。

</dd> <dt>

**DSVFormat**
</dt> <dd>

描述深度樣板格式。

</dd> <dt>

**RasterizerState**
</dt> <dd>

描述轉譯器的狀態。

</dd> <dt>

**RTVFormats**
</dt> <dd>

描述呈現目標格式。

</dd> <dt>

**SampleDesc**
</dt> <dd>

描述範例計數和品質。

</dd> <dt>

**SampleMask**
</dt> <dd>

描述搭配 blend 狀態使用的範例遮罩。

</dd> <dt>

**CachedPSO**
</dt> <dd>

描述快取的 PSO。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程支援 Windows 10 Creators Update 和更新版本，但不支援在 Windows 10 中加入的子物件類型（例如針對 view 實例）。 若要支援在秋季建立者更新中新增的子物件類型，請改用 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) 。

此結構的可存取成員變數是 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程子物件範本的 typedef，它會將 \_ 子物件類型標記和子物件資料結合成適合資料流程描述的單一物件。

這些 typedef 包括：

<dl> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 






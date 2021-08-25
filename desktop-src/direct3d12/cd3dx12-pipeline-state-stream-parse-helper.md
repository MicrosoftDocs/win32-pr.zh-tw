---
title: 'CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER 結構 (D3dx12 .h) '
description: '\_ \_ \_ 從傳遞至對應成員函式的物件詳細資料，建立內部 CD3DX12 管線狀態資料流程物件。 此結構會實 ID3DX12PipelineParserCallbacks 介面。'
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d20c34fb2c32cc588a12ac820cd80083d3c3139fa85cbf36810379a21618e80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851248"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 剖析協助程式 \_ 結構

\_ \_ \_ 從傳遞至對應成員函式的物件詳細資料，建立內部 CD3DX12 管線狀態資料流程物件。 此結構會實 [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) 介面。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a>成員

<dl> <dt>

**PipelineStream**
</dt> <dd>

內部 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)。 其目前的狀態代表已在此物件上呼叫之回呼方法的累積效果。

</dd> <dt>

**FlagsCb (D3D12 \_ 管線 \_ 狀態 \_ 旗標旗標)**
</dt> <dd>

使用 *flags* 參數的值，初始化 **PipelineStream** 的 **旗標** 成員。

</dd> <dt>

**NodeMaskCb (UINT NodeMask)**
</dt> <dd>

使用 *NodeMask* 參數的值，初始化 **PipelineStream** 的 **NodeMask** 成員。

</dd> <dt>

**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

使用 *pRootSignature* 參數的值，初始化 **PipelineStream** 的 **pRootSignature** 成員。

</dd> <dt>

**InputLayoutCb (const D3D12 \_ 輸入 \_ 版面配置 \_ DESC& InputLayout)**
</dt> <dd>

使用 *InputLayout* 參數的值，初始化 **PipelineStream** 的 **InputLayout** 成員。

</dd> <dt>

**IBStripCutValueCb (D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值 IBStripCutValue)**
</dt> <dd>

使用 *IBStripCutValue* 參數的值，初始化 **PipelineStream** 的 **IBStripCutValue** 成員。

</dd> <dt>

**PrimitiveTopologyTypeCb (D3D12 \_ 基本 \_ 拓撲 \_ 類型 PrimitiveTopologyType)**
</dt> <dd>

使用 *PrimitiveTopologyType* 參數的值，初始化 **PipelineStream** 的 **PrimitiveTopologyType** 成員。

</dd> <dt>

**VSCb (const D3D12 \_ 著色器 \_ 位元組& VS)**
</dt> <dd>

使用 *vs* 參數的值，初始化 **vs** (頂點著色器) **PipelineStream** 成員。

</dd> <dt>

**GSCb (const D3D12 \_ 著色器 \_ 位元組& GS)**
</dt> <dd>

使用 *gs* 參數的值，初始化 **PipelineStream** 的) 成員的 **gs** (幾何著色器。

</dd> <dt>

**StreamOutputCb (const D3D12 \_ STREAM \_ OUTPUT \_ DESC& >streamoutput)**
</dt> <dd>

使用 *>streamoutput* 參數的值，初始化 **PipelineStream** 的 **>streamoutput** 成員。

</dd> <dt>

**HSCb (const D3D12 \_ 著色器 \_ 位元組& HS)**
</dt> <dd>

使用 *hs* 參數的值，將 **hs** (輪廓著色器) 成員 **PipelineStream** 。

</dd> <dt>

**DSCb (const D3D12 \_ 著色器 \_ 位元組& DS)**
</dt> <dd>

使用 *ds* 參數的值，初始化 **PipelineStream** 的 **ds** (網域著色器) 成員。

</dd> <dt>

**PSCb (const D3D12 \_ 著色器 \_ 位元組& PS)**
</dt> <dd>

使用 *ps* 參數的值，初始化 **PipelineStream** 的 **ps** (圖元著色器) 成員。

</dd> <dt>

**CSCb (const D3D12 \_ 著色器 \_ 位元組& CS)**
</dt> <dd>

使用 *cs* 參數的值，初始化 **PipelineStream** 的 **cs** 成員。

</dd> <dt>

**BlendStateCb (const D3D12 \_ BLEND \_ DESC& BlendState)**
</dt> <dd>

使用 *BlendState* 參數的值，初始化 **PipelineStream** 的 **BlendState** 成員。

</dd> <dt>

**DepthStencilStateCb (const D3D12 \_ DEPTH \_ 樣板 \_ DESC& DepthStencilState)**
</dt> <dd>

使用 *DepthStencilState* 參數的值（ [**D3D12 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)），初始化 **PipelineStream** 的 **DepthStencilState** 成員。

</dd> <dt>

**DepthStencilState1Cb (const D3D12 \_ DEPTH \_ 樣板 \_ DESC1& DepthStencilState)**
</dt> <dd>

使用 *DepthStencilState* 參數的值（ [**D3D12 \_ 深度樣板 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)），初始化 **PipelineStream** 的 **DepthStencilState** 成員。

</dd> <dt>

**DSVFormatCb (DXGI \_ FORMAT DSVFormat)**
</dt> <dd>

使用 *DSVFormat* 參數的值，初始化 **PipelineStream** 的 **DSVFormat** 成員。

</dd> <dt>

**RasterizerStateCb (const D3D12 轉譯器 \_ \_ DESC& RasterizerState)**
</dt> <dd>

使用 *RasterizerState* 參數的值，初始化 **PipelineStream** 的 **RasterizerState** 成員。

</dd> <dt>

**RTVFormatsCb (const D3D12 \_ RT \_ 格式 \_ 陣列& RTVFormats)**
</dt> <dd>

使用 *RTVFormats* 參數的值，初始化 **PipelineStream** 的 **RTVFormats** 成員。

</dd> <dt>

**SampleDescCb (const DXGI \_ 範例 \_ DESC& SampleDesc)**
</dt> <dd>

使用 *SampleDesc* 參數的值，初始化 **PipelineStream** 的 **SampleDesc** 成員。

</dd> <dt>

**SampleMaskCb (UINT SampleMask)**
</dt> <dd>

使用 *SampleMask* 參數的值，初始化 **PipelineStream** 的 **SampleMask** 成員。

</dd> <dt>

**ViewInstancingCb (const D3D12 \_ VIEW \_ 實例 \_ DESC& ViewInstancingDesc)**
</dt> <dd>

使用 *ViewInstancingDesc* 參數的值，初始化 **PipelineStream** 的 **ViewInstancingDesc** 成員。

</dd> <dt>

**CachedPSOCb (const D3D12 快取 \_ \_ 管線 \_ 狀態& CachedPSO)**
</dt> <dd>

使用 *CachedPSO* 參數的值，初始化 **PipelineStream** 的 **CachedPSO** 成員。

</dd> <dt>

**ErrorBadInputParameter (UINT)**
</dt> <dd>

不執行任何動作。

</dd> <dt>

**ErrorDuplicateSubobject (D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型)**
</dt> <dd>

不執行任何動作。

</dd> <dt>

**ErrorUnknownSubobject (UINT)**
</dt> <dd>

不執行任何動作。

</dd> </dl>

## <a name="remarks"></a>備註

以第二個參數形式傳遞至 [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md)函式時，會從做為第一個參數傳遞的 [**D3D12 \_ 管線 \_ 狀態 \_ 資料流程 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)複製內部 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)物件的詳細資料。 此進程會驗證來來源資料流描述。 如果 D3DX12ParsePipelineStream 傳回 **S \_ OK**，則來來源資料流描述和產生的 **CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1PipelineStream** 都是有效的，否則兩者都無效。 不正確資料流程和其他錯誤只會透過 D3DX12ParsePipelineStream 的傳回值回報;此結構會執行錯誤回呼來執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 






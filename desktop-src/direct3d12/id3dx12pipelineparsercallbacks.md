---
title: 'ID3DX12PipelineParserCallbacks 介面 (D3DX12 .h) '
description: 表示 D3DX12parsePipelineStream helper 函式所使用之剖析器和錯誤回呼集合的介面。
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，說明
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0061746da589c30e4745dfa3e4dc573f7b5d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986112"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>ID3DX12PipelineParserCallbacks 介面

表示 [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) helper 函式所使用之剖析器和錯誤回呼集合的介面。

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX12PipelineParserCallbacks** 介面具有這些方法。



| 方法                                                                                    | 描述                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | 呼叫物件的 blend 狀態原因子物件回呼，該物件會執行這個介面。<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | 呼叫 (管線狀態物件的快取 PSO，) 執行此介面之物件的子物件回呼。<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | 呼叫物件的計算著色器子物件回呼，該物件會執行這個介面。<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | 呼叫物件的深度樣板狀態 ([**D3D12 深度樣板) \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) ，此物件會執行這個介面。<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | 呼叫物件的深度樣板值格式物件回呼，該物件會執行這個介面。<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | 呼叫物件的深度樣板狀態子物件回呼，該物件會執行這個介面。<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | 呼叫物件的網域著色器子物件回呼，該物件會執行這個介面。<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | 呼叫實此介面之物件的錯誤輸入參數錯誤回呼。<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | 呼叫物件的重複子物件錯誤回呼，該物件會執行這個介面。<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | 呼叫物件的未知子物件錯誤回呼，該物件會執行這個介面。<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | 呼叫物件的旗標子物件回呼，該物件會執行這個介面。<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | 呼叫物件的幾何著色器子物件回呼，該物件會執行這個介面。<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | 呼叫物件的輪廓著色器子物件回呼，該物件會執行這個介面。<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | 呼叫物件的索引緩衝區帶剪值子物件回呼，該物件會執行這個介面。<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | 呼叫物件的輸入版面配置子物件回呼，該物件會執行這個介面。<br/>                                                                            |
| [**NodemaskCb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | 呼叫物件的 nodemask 子物件回呼，該物件會執行這個介面。<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | 呼叫基底拓撲類型物件的子物件回呼，該物件會執行這個介面。<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | 呼叫物件的圖元著色器子物件回呼，該物件會執行這個介面。<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | 呼叫執行此介面之物件的轉譯器狀態原因子物件回呼。<br/>                                                            |
| [**RootSignatureCB**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | 呼叫物件的根簽章子物件回呼，該物件會執行這個介面。<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | 呼叫物件的呈現目標格式陣列子物件回呼，該物件會執行這個介面。<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | 呼叫物件的範例描述子物件回呼，該物件會執行這個介面。<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | 呼叫物件的範例遮罩子物件回呼，該物件會執行這個介面。<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | 呼叫物件的資料流程輸出描述子物件回呼，該物件會執行這個介面。<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | 呼叫物件的頂點著色器子物件回呼，該物件會執行這個介面。<br/>                                                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 的 Helper 介面](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 






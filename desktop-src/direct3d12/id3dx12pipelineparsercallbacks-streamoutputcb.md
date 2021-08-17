---
title: 'ID3DX12PipelineParserCallbacks StreamOutputCb 方法 (D3DX12 .h) '
description: 呼叫物件的資料流程輸出描述子物件回呼，該物件會執行這個介面。
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- StreamOutputCb 方法
- StreamOutputCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，StreamOutputCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1e484d044bc4de2be3d40c6080e77b62aa57b59f0161c2021b8696316970542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632348"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>ID3DX12PipelineParserCallbacks：： StreamOutputCb 方法

呼叫物件的資料流程輸出描述子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>Streamoutput* \[裁判\]
</dt> <dd>

Type： **Const [**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

從管線狀態資料流程剖析之資料流程輸出描述子物件的詳細資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

不傳回任何專案。

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

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 






---
title: 'ID3DX12PipelineParserCallbacks IBStripCutValueCb 方法 (D3DX12 .h) '
description: 呼叫物件的索引緩衝區帶剪值子物件回呼，該物件會執行這個介面。
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- IBStripCutValueCb 方法
- IBStripCutValueCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，IBStripCutValueCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992334"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>ID3DX12PipelineParserCallbacks：： IBStripCutValueCb 方法

呼叫物件的索引緩衝區帶剪值子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IBStripCutValue* 
</dt> <dd>

類型： **[ **D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

從管線狀態資料流程剖析的索引緩衝區區域/剪下值子物件的詳細資料。

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

[**D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 






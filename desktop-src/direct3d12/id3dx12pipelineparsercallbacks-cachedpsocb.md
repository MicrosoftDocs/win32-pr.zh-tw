---
title: 'ID3DX12PipelineParserCallbacks CachedPSOCb 方法 (D3DX12 .h) '
description: 呼叫 (管線狀態物件的快取 PSO，) 執行此介面之物件的子物件回呼。
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- CachedPSOCb 方法
- CachedPSOCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，CachedPSOCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998213"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a>ID3DX12PipelineParserCallbacks：： CachedPSOCb 方法

呼叫 (管線狀態物件的快取 PSO，) 執行此介面之物件的子物件回呼。

## <a name="syntax"></a>語法


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CachedPSO* \[裁判\]
</dt> <dd>

類型： **Const D3D12 快取的 [**\_ \_ 管線 \_ 狀態**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

快取的 PSO (管線狀態物件的詳細資料，) 從管線狀態資料流程剖析的子物件。

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

[**D3D12 快取的 \_ \_ 管線 \_ 狀態**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 






---
title: 'ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb 方法 (D3DX12 .h) '
description: 呼叫基底拓撲類型物件的子物件回呼，該物件會執行這個介面。
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- PrimitiveTopologyTypeCb 方法
- PrimitiveTopologyTypeCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，PrimitiveTopologyTypeCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999973"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a>ID3DX12PipelineParserCallbacks：:P rimitiveTopologyTypeCb 方法

呼叫基底拓撲類型物件的子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PrimitiveTopologyType* 
</dt> <dd>

類型： **[ **D3D12 \_ 基本 \_ 拓撲 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

從管線狀態資料流程剖析之基本拓撲類型子物件的詳細資料。

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

[**D3D12 \_ 基本 \_ 拓撲 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 






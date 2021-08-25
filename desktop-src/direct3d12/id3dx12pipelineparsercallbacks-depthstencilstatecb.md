---
title: 'ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h) '
description: 呼叫物件的深度樣板狀態子物件回呼，該物件會執行這個介面。
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- DepthStencilStateCb 方法
- DepthStencilStateCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，DepthStencilStateCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1086156fcaa6b8736c049c93bacc5dfd1f5e915ba8a7006b3c71e654ba65f52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894578"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h) 

呼叫物件的深度樣板狀態子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DepthStencilState* \[裁判\]
</dt> <dd>

類型：**常數 [**D3D12 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**

從管線狀態資料流程剖析的深度樣板狀態子物件詳細資料。

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

[**D3D12 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 






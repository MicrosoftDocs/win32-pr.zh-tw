---
title: 'ID3DX12PipelineParserCallbacks DepthStencilState1Cb 方法 (D3DX12 .h) '
description: 呼叫物件的深度樣板狀態 (D3D12 \_ 深度樣板 \_ \_) DESC1，此物件會執行這個介面。
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- DepthStencilState1Cb 方法
- DepthStencilState1Cb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，DepthStencilState1Cb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97deca53ffc4de474896b89993f84cebf359acd9045956243c5ece4e215e31cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528966"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a>ID3DX12PipelineParserCallbacks：:D epthStencilState1Cb 方法

呼叫物件的深度樣板狀態 ([**D3D12 深度樣板) \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) ，此物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DepthStencilState* \[裁判\]
</dt> <dd>

Type： **Const [**D3D12 \_ DEPTH \_ 樣板 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**

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

[**D3D12 \_ 深度 \_ 樣板 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 






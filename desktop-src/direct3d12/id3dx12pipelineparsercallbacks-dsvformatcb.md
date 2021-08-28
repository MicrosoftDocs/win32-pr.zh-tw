---
title: 'ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h)  (DSV) '
description: 呼叫物件的深度樣板值格式物件回呼，該物件會執行這個介面。
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
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
ms.openlocfilehash: d72a7501c57af515a9c9e26a435aaae02ae3ebd4cdb260f37800fda1be3d720e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096413"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a>ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h) 取得深度樣板值

呼叫物件的深度樣板值格式物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DepthStencilState* 
</dt> <dd>

類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

從管線狀態資料流程剖析的深度樣板值格式子物件詳細資料。

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

[**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 


---
title: 'ID3DX12PipelineParserCallbacks BlendStateCb 方法 (D3DX12 .h) '
description: 呼叫物件的 blend 狀態原因子物件回呼，該物件會執行這個介面。
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- BlendStateCb 方法
- BlendStateCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，BlendStateCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a9d84e3648a54668211b8b9e590c653111c93553115aba43b5353f9549bfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528976"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>ID3DX12PipelineParserCallbacks：： BlendStateCb 方法

呼叫物件的 blend 狀態原因子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BlendState* \[裁判\]
</dt> <dd>

Type： **Const [**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

從管線狀態資料流程剖析的 blend 狀態原因子物件詳細資料。

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

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 






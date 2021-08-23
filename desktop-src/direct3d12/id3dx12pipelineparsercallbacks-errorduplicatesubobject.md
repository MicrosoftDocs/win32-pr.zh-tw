---
title: 'ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject 方法 (D3DX12 .h) '
description: 呼叫物件的重複子物件錯誤回呼，該物件會執行這個介面。
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- ErrorDuplicateSubobject 方法
- ErrorDuplicateSubobject 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，ErrorDuplicateSubobject 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33724b1fdfec4951ce2efb31d4916ce210dc2b73858a5ef250c14a8744646bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045466"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a>ID3DX12PipelineParserCallbacks：： ErrorDuplicateSubobject 方法

呼叫物件的重複子物件錯誤回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DuplicateType* 
</dt> <dd>

類型： **[ **D3D12 \_ 管線 \_ 狀態 \_ \_** 子物件類型](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**

已複製的子物件類型。

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

[**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 


---
title: 'ID3DX12PipelineParserCallbacks SampleMaskCb 方法 (D3DX12 .h) '
description: 呼叫物件的範例遮罩子物件回呼，該物件會執行這個介面。
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- SampleMaskCb 方法
- SampleMaskCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，SampleMaskCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64acc7e969f52e78250cde9bc4c693ce3eae06ae3edd08e7f18c65dc0ff6fa8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069588"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>ID3DX12PipelineParserCallbacks：： SampleMaskCb 方法

呼叫物件的範例遮罩子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SampleMask* 
</dt> <dd>

類型： **UINT**

從管線狀態資料流程剖析的範例遮罩子物件詳細資料。

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
</dt> </dl>

 

 






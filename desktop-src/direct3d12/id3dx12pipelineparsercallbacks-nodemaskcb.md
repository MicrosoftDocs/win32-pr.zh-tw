---
title: 'ID3DX12PipelineParserCallbacks NodemaskCb 方法 (D3DX12 .h) '
description: 呼叫物件的 nodemask 子物件回呼，該物件會執行這個介面。
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- NodemaskCb 方法
- NodemaskCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，NodemaskCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356ddf6ea86980ee882ad7544096811db420ae0cf8224f315801b708b95ae98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045446"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a>ID3DX12PipelineParserCallbacks：： NodemaskCb 方法

呼叫物件的 nodemask 子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Nodemask* 
</dt> <dd>

類型： **UINT**

從管線狀態資料流程剖析的 nodemask 子物件詳細資料。

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

 

 






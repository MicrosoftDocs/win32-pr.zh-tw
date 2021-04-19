---
title: 'ID3DX12PipelineParserCallbacks ErrorUnknownSubobject 方法 (D3DX12 .h) '
description: 呼叫物件的未知子物件錯誤回呼，該物件會執行這個介面。
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- ErrorUnknownSubobject 方法
- ErrorUnknownSubobject 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，ErrorUnknownSubobject 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988203"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a>ID3DX12PipelineParserCallbacks：： ErrorUnknownSubobject 方法

呼叫物件的未知子物件錯誤回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*UnknownTypeValue* 
</dt> <dd>

類型： **UINT**

所嘗試子物件的無法辨識的子物件類型。

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

 

 






---
title: 'ID3DX12PipelineParserCallbacks ErrorBadInputParameter 方法 (D3DX12 .h) '
description: 呼叫實此介面之物件的錯誤輸入參數錯誤回呼。
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- ErrorBadInputParameter 方法
- ErrorBadInputParameter 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，ErrorBadInputParameter 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fb00490fc2c2710207e7bdd01f7be900996452f34b379a2c883ef2a99dfcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096416"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a>ID3DX12PipelineParserCallbacks：： ErrorBadInputParameter 方法

呼叫實此介面之物件的錯誤輸入參數錯誤回呼。

## <a name="syntax"></a>語法


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ParameterIndex* 
</dt> <dd>

類型： **UINT**

包含不正確輸入之參數的位置。 最左邊的參數位於位置1，而不是位置0。

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

 

 






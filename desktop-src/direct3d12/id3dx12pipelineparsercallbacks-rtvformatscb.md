---
title: 'ID3DX12PipelineParserCallbacks RTVFormatsCb 方法 (D3DX12 .h) '
description: 呼叫物件的呈現目標格式陣列子物件回呼，該物件會執行這個介面。
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- RTVFormatsCb 方法
- RTVFormatsCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，RTVFormatsCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d826bd2c2f3c5f1c0783a4be2cba132e4874f5a54776c227590dd87f5365d347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045436"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>ID3DX12PipelineParserCallbacks：： RTVFormatsCb 方法

呼叫物件的呈現目標格式陣列子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RTVFormats* \[裁判\]
</dt> <dd>

Type： **Const [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

從管線狀態資料流程剖析之轉譯目標格式陣列子物件的詳細資料。

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

[**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 






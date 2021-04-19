---
title: 'D3DX12ParsePipelineStream 函式 (D3dx12) '
description: 剖析管線狀態資料流程描述，針對每個已剖析的子物件實例呼叫使用者定義的回呼。
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream 函式
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997613"
---
# <a name="d3dx12parsepipelinestream-function"></a>D3DX12ParsePipelineStream 函式

剖析管線狀態資料流程描述，針對每個已剖析的子物件實例呼叫使用者定義的回呼。

## <a name="syntax"></a>語法


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Desc* \[裁判\]
</dt> <dd>

類型： **Const [**D3D12 \_ 管線 \_ 狀態 \_ 資料流程 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

要剖析的管線狀態資料流程描述。

</dd> <dt>

*pCallbacks* 
</dt> <dd>

類型： **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

結構，指定要針對每個子物件類型呼叫的回呼，以及在發生剖析錯誤時呼叫的其他回呼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果遇到不明的子物件類型，這個方法會傳回 HRESULT 成功 (**S \_ OK** 或 **E \_ INVALIDARG** 錯誤，如果資料流程描述是空的、null 或包含重複的子物件 (包括衍生子物件) 或 *pCallbacks* 為 null。 在傳回電子 INVALIDARG 的每個案例中 \_ ，會先呼叫相對應的回呼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> </dl>

 

 






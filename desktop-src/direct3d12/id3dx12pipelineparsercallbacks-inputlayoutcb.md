---
title: 'ID3DX12PipelineParserCallbacks InputLayoutCb 方法 (D3DX12 .h) '
description: 呼叫物件的輸入版面配置子物件回呼，該物件會執行這個介面。
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- InputLayoutCb 方法
- InputLayoutCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，InputLayoutCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f7012686c85b38e94f8f3d2400cf406d614fc83ff0ba25e746ac0433b2e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528770"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>ID3DX12PipelineParserCallbacks：： InputLayoutCb 方法

呼叫物件的輸入版面配置子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*InputLayout* \[裁判\]
</dt> <dd>

類型： **Const [**D3D12 \_ 輸入 \_ 版面配置 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

從管線狀態資料流程剖析之輸入版面配置子物件的詳細資料。

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

[**D3D12 \_ 輸入 \_ 版面配置 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 






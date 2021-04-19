---
title: 'ID3DX12PipelineParserCallbacks RasterizerStateCb 方法 (D3DX12 .h) '
description: 呼叫執行此介面之物件的轉譯器狀態原因子物件回呼。
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- RasterizerStateCb 方法
- RasterizerStateCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，RasterizerStateCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985896"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>ID3DX12PipelineParserCallbacks：： RasterizerStateCb 方法

呼叫執行此介面之物件的轉譯器狀態原因子物件回呼。

## <a name="syntax"></a>語法


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RasterizerState* \[裁判\]
</dt> <dd>

類型： **Const [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)** 轉譯器 DESC

從管線狀態資料流程剖析的轉譯器狀態原因子物件詳細資料。

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

[**D3D12 轉譯器 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 






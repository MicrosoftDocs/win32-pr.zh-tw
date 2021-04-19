---
title: 'ID3DX12PipelineParserCallbacks VSCb 方法 (D3DX12 .h) '
description: 呼叫物件的頂點著色器子物件回呼，該物件會執行這個介面。
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- VSCb 方法
- VSCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，VSCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988607"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a>ID3DX12PipelineParserCallbacks：： VSCb 方法

呼叫物件的頂點著色器子物件回呼，該物件會執行這個介面。

## <a name="syntax"></a>語法


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VS* \[裁判\]
</dt> <dd>

Type： **Const [**D3D12 \_ 著色器 \_ 位元組的位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

從管線狀態資料流程剖析之頂點著色器子物件的詳細資料。

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

[**D3D12 \_ 著色器 \_ 位元組碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 






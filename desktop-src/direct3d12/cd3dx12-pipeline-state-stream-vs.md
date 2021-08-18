---
title: 'CD3DX12_PIPELINE_STATE_STREAM_VS 結構 (D3dx12 .h) '
description: 協助程式結構，用來將頂點著色器描述為適合資料流程描述的單一物件。
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VS 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4361cf50a97cd3d7bf2abc6995182e9ca24bad6b824505408aca98bd4b3ead42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045726"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 與結構的比較

協助程式結構，用來將頂點著色器描述為適合資料流程描述的單一物件。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 與**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ 管線 \_ 狀態資料流程實例 \_ \_ 與

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 與 (D3D12 \_ 著色器 \_ 位元組位元組常數 &i)**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程的新實例 \_ ， \_ 並 \_ 以 **D3D12 管線狀態子物件類型的 \_ 管線狀態子物件 \_ \_ \_ 類型 \_ 與** 子物件資料（  [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)程式碼結構）進行初始化。

</dd> <dt>

**operator = (D3D12 \_ 著色器 \_ 位元組位元組常數& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**運算子 D3D12 \_ 著色器 \_ 位元組 () 常數**
</dt> <dd>

隱含轉換成 [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 與 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化比較，且定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 


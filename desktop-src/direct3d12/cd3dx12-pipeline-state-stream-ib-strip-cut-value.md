---
title: 'CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE 結構 (D3dx12 .h) '
description: 協助程式結構，用來將索引緩衝區區域剪下值描述為適合資料流程描述的單一物件。
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976461"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 帶 \_ 剪下 \_ 值結構

協助程式結構，用來將索引緩衝區區域剪下值描述為適合資料流程描述的單一物件。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 帶 \_ 剪 \_ 值**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ IB \_ 帶 \_ 剪 \_ 值的新、未初始化的實例。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ IB \_ 區域 \_ 剪下 \_ 值 (D3D12 \_ 索引 \_ 緩衝區 \_ 帶剪下 \_ \_ 值 const &i)**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ IB 區域 \_ 剪下值的新 \_ 實例 \_ ，並以 **D3D12 管線狀態子物件類型的 \_ 管線狀態子物件 \_ \_ \_ 類型 \_ IB 區域剪下 \_ \_ \_ 值** 和子物件資料（ [**D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)結構）進行初始化。

</dd> <dt>

**operator = (D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪下 \_ 值 const& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**運算子 D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ () 常數的剪下 \_ 值**
</dt> <dd>

隱含轉換成 [**D3D12 \_ 索引 \_ 緩衝區帶的剪下 \_ \_ \_ 值**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 區域 \_ 剪下 \_ 值是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 


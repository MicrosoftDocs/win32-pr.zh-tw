---
title: 'CD3DX12_PIPELINE_STATE_STREAM_FLAGS 結構 (D3dx12 .h) '
description: 用來將管線狀態旗標描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986128"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 旗標結構

用來將管線狀態旗標描述為適用于資料流程描述之單一物件的 helper 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 旗標**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 旗標的新、未初始化的實例。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 旗標 (D3D12 \_ 管線 \_ 狀態 \_ 旗標 const &i)**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程旗標的新實例 \_ ，並使用 **D3D12 \_ 管線狀態子物件 \_ \_ \_ 類型 \_ 旗標** 和從 *i* 複製的子物件資料（ [**D3D12 \_ 管線 \_ 狀態 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) 結構）進行初始化。

</dd> <dt>

**operator = (D3D12 \_ 管線 \_ 狀態 \_ 旗標 const& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**運算子 D3D12 \_ 管線 \_ 狀態 \_ 旗標 () 常數**
</dt> <dd>

隱含轉換成 [**D3D12 \_ 管線 \_ 狀態 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 旗標是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 


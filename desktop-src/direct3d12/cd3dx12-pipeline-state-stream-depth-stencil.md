---
title: 'CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL 結構 (D3dx12 .h) '
description: '用來將深度樣板描述描述為適用于資料流程描述之單一物件的 helper 結構。 |CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL 結構 (D3dx12 .h) '
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0b9cc7ba6b37858ae355d9470f321f991e8329f5fbf7aabd23b6f8bcfe7d8fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858178"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度樣板 \_ 結構

用來將深度樣板描述描述為適用于資料流程描述之單一物件的 helper 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度樣板的新、未初始化的實例 \_ 。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度樣板 \_ (CD3DX12 \_ 深度 \_ 樣板 \_ DESC const &i)**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程深度樣板的新實例 \_ \_ \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 深度 \_** 樣板的子物件類型和從 *i* 複製的子物件資料（ [**CD3DX12 \_ 深度 \_ 樣板 \_ DESC**](cd3dx12-depth-stencil-desc.md) 結構）進行初始化。

</dd> <dt>

**operator = (CD3DX12 \_ 深度 \_ 樣板 \_ DESC const& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**運算子 CD3DX12 \_ 深度 \_ 樣板 \_ DESC () const**
</dt> <dd>

隱含轉換成 [**CD3DX12 \_ 深度樣板 \_ \_ DESC**](cd3dx12-depth-stencil-desc.md) 的結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度樣板 \_ 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 


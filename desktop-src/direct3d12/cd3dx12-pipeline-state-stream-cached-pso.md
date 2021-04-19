---
title: 'CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO 結構 (D3dx12 .h) '
description: 用來將快取的 PSO 描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988171"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程快取 \_ \_ PSO 結構

用來將快取的 PSO 描述為適用于資料流程描述之單一物件的 helper 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程快取 \_ \_ PSO**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程快取 PSO 的新、未初始化的實例 \_ \_ \_ \_ 。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態資料流程快取的 \_ PSO (D3D12 快取的 \_ \_ \_ \_ 管線 \_ 狀態 const &i)**
</dt> <dd>

建立 CD3DX12 管線狀態資料流程快取 PSO 的新實例，此實例 \_ \_ \_ \_ \_ 是以 **D3D12 管線狀態子物件類型的管線狀態子物件類型快取的 \_ \_ \_ \_ \_ \_ PSO** 和子物件資料（D3D12 快取的 [**\_ \_ 管線 \_ 狀態**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)結構 *）進行* 初始化。

</dd> <dt>

**operator = (D3D12 快取的 \_ \_ 管線 \_ 狀態 const& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**operator D3D12 快取的 \_ \_ 管線 \_ 狀態 () 常數**
</dt> <dd>

隱含轉換成 D3D12 快取的 [**\_ \_ 管線 \_ 狀態**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程快取 \_ \_ PSO 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 


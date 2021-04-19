---
title: 'CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS 結構 (D3dx12 .h) '
description: 協助程式結構，用來將轉譯目標格式描述為適合資料流程描述的單一物件。
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991443"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式結構

協助程式結構，用來將轉譯目標格式描述為適合資料流程描述的單一物件。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程轉譯 \_ \_ 目標 \_ 格式的新、未初始化的實例。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式 (D3D12 \_ RT \_ 格式 \_ 陣列 const &i)**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態資料流程轉譯目標格式的新實例 \_ \_ \_ \_ ，並以 **D3D12 管線狀態子物件類型的 \_ 管線狀態子物件類型轉譯 \_ \_ \_ \_ \_ 目標 \_ 格式** 和子物件資料（ [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)結構）進行初始化。 

</dd> <dt>

**operator = (D3D12 \_ RT \_ 格式 \_ 陣列 const& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**運算子 D3D12 \_ RT \_ 格式 \_ 陣列 () 常數**
</dt> <dd>

隱含轉換成 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
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

 


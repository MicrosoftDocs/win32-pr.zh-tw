---
title: 'CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT 結構 (D3dx12 .h) '
description: 用來將輸入配置描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991445"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置結構

用來將輸入配置描述為適用于資料流程描述之單一物件的 helper 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入配置的新、未初始化的實例 \_ 。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置 (D3D12 \_ 輸入 \_ 版面配置 \_ DESC const &i)**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程輸入配置的新實例 \_ \_ \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 輸入 \_** 配置和從 *i* 複製的子物件資料（ [**D3D12 輸入配置 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) 結構）進行初始化。

</dd> <dt>

**operator = (D3D12 \_ 輸入 \_ 版面配置 \_ DESC const& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**operator D3D12 \_ 輸入 \_ 版面配置 \_ DESC () const**
</dt> <dd>

隱含轉換成 [**D3D12 \_ 輸入版面 \_ 配置 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入配置 \_ 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 


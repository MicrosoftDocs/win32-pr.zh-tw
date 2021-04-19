---
title: 'CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER 結構 (D3dx12 .h) '
description: 協助程式結構，用來將轉譯器描述描述為適合資料流程描述的單一物件。
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989184"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程轉譯器 \_ 結構

協助程式結構，用來將轉譯器描述描述為適合資料流程描述的單一物件。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 轉譯器**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程轉譯器的新、未初始化的實例 \_ \_ \_ 。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 串流轉譯器 (CD3DX12 轉譯器 \_ \_ \_ DESC const &i)**
</dt> <dd>

建立 CD3DX12 管線狀態資料流程轉譯器的新實例 \_ \_ \_ \_ ，並使用 **D3D12 \_ 管線狀態子物件 \_ \_ \_ 類型 \_** 轉譯器和從 *i* 複製的子物件資料（CD3DX12 的轉譯器 [**\_ \_ DESC**](cd3dx12-rasterizer-desc.md) 結構）進行初始化。

</dd> <dt>

**operator = (CD3DX12 轉譯器 \_ \_ DESC const& i)**
</dt> <dd>

複製指派運算子。

</dd> <dt>

**運算子 CD3DX12 轉譯器 \_ \_ DESC () const**
</dt> <dd>

隱含轉換成 [**CD3DX12 的 \_ 光柵器 \_ DESC**](cd3dx12-rasterizer-desc.md) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 串流轉譯器 \_ 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ \_ 資料流程**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
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

 


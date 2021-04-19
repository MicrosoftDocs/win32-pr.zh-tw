---
title: 'CD3DX12_PIPELINE_STATE_STREAM_GS 結構 (D3dx12 .h) '
description: 用來將幾何著色器描述為適合資料流程描述之單一物件的 helper 結構。
ms.assetid: EAE81688-DAEE-4F7C-A80D-E33B364B2E8C
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_GS 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_GS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5ab5854ceddfb1a969742924c8063450e611bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993863"
---
# <a name="cd3dx12_pipeline_state_stream_gs-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ GS 結構

用來將幾何著色器描述為適合資料流程描述之單一物件的 helper 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_GS {
                                   CD3DX12_PIPELINE_STATE_STREAM_GS;
                                   CD3DX12_PIPELINE_STATE_STREAM_GS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_GS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ GS**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 GS 的新、未初始化的實例 \_ 。

</dd> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ GS (D3D12 \_ 著色器 \_ 位元組位元組常數 &i)**
</dt> <dd>

建立 CD3DX12 \_ 管線 \_ 狀態資料流程 GS 的新實例 \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ GS** 和從 *i* 複製的子物件資料（ [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 程式化結構）進行初始化。

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

CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ GS 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ \_ 資料流程**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_GS>
    CD3DX12_PIPELINE_STATE_STREAM_GS;
          
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

 


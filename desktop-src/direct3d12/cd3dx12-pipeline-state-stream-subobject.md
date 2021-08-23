---
title: 'CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT 結構 (D3dx12 .h) '
description: 樣板化的 helper 結構，用來將子物件類型和子物件資料組封裝成適合資料流程描述的單一物件。
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d945296ae4ee09710b74b9fdf2259251632d25fb309ede2983858c0c59be72d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729478"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程子物件 \_ 結構

樣板化的 helper 結構，用來將子物件類型和子物件資料組封裝成適合資料流程描述的單一物件。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**
</dt> <dd>

建立 CD3DX12 \_ 管線狀態資料流程子物件的新、未初始化的實例 \_ \_ \_ 。

</dd> <dt>

**CD3DX12 \_管線 \_ 狀態 \_ 資料流程 \_** 子物件 (InnerStructType * * const &i) * *
</dt> <dd>

建立新的 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程子物件 \_ 範本實例，並以 [**D3D12 \_ 管線狀態子物件 \_ \_ \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) 的子物件類型和從 *i* 複製的子物件資料進行初始化。 子物件類型和子物件資料類型分別會指定為範本參數、 **類型** 和 **InnerStructType**。 如需詳細資訊，請參閱下面的備註。

</dd> <dt>

**運算子 = (** InnerStructType * * const& i) * *
</dt> <dd>

複製指派運算子。

</dd> <dt>

**operator **InnerStructType** () const**
</dt> <dd>

隱含轉換成 **InnerStructType** 樣板參數所指定的子物件資料類型。

</dd> </dl>

## <a name="remarks"></a>備註

CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件是定義如下的範本：


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



範本參數 **InnerStructType** 會指定子物件資料類型;亦即，要編碼成資料流程的子物件詳細資料。 範本參數 **類型** 會指定子物件類型;也就是範本參數所指定之結構的型別 **InnerStructType**。 樣板參數 **operators.defaultarg** 會指定選擇性的值，當對應的範本具現化的實例為預設架構時，子物件資料將會初始化為。例如，使用 [**CD3DX12 \_ default**](cd3dx12-default.md)，將 [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)初始化為使用一般 BLEND 狀態預設值的預設結構。

以下是已定義的範本具現化：

-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 旗標**](cd3dx12-pipeline-state-stream-flags.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 節點 \_ 遮罩**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 根 \_ 簽章**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 帶 \_ 剪 \_ 值**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 基本 \_ 拓撲**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 與**](cd3dx12-pipeline-state-stream-vs.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ \_ 輸出**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ DS**](cd3dx12-pipeline-state-stream-ds.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板 \_ 格式**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 轉譯器**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ DESC**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ 遮罩**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程快取 \_ \_ PSO**](cd3dx12-pipeline-state-stream-cached-pso.md)

[**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)、 [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 深度 \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)樣板、CD3DX12 管線狀態串流 [**\_ \_ \_ \_ 深度 \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)，以及 [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_**](cd3dx12-pipeline-state-stream-rasterizer.md)轉譯器結構，會定義為使用 [**CD3DX12 \_ 預設**](cd3dx12-default.md)值以一般預設值初始化其子物件資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 


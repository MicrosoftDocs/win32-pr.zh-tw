---
title: 'CD3DX12_PIPELINE_STATE_STREAM_PS 結構 (D3dx12 .h) '
description: 協助程式結構，用來描述圖元著色器，做為適合資料流程描述的單一物件。
ms.assetid: A71E2ABE-5B52-41B4-ACE0-25CA63EF2565
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PS 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f3b49328ad85bc68147ad58b043459c223e6a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982194"
---
# <a name="cd3dx12_pipeline_state_stream_ps-structure"></a><span data-ttu-id="8f5c5-104">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ PS 結構</span><span class="sxs-lookup"><span data-stu-id="8f5c5-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PS structure</span></span>

<span data-ttu-id="8f5c5-105">協助程式結構，用來描述圖元著色器，做為適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="8f5c5-105">A helper structure used to describe a pixel shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f5c5-106">語法</span><span class="sxs-lookup"><span data-stu-id="8f5c5-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PS {
                                   CD3DX12_PIPELINE_STATE_STREAM_PS;
                                   CD3DX12_PIPELINE_STATE_STREAM_PS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="8f5c5-107">成員</span><span class="sxs-lookup"><span data-stu-id="8f5c5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f5c5-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ PS**</span><span class="sxs-lookup"><span data-stu-id="8f5c5-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>
</dt> <dd>

<span data-ttu-id="8f5c5-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 串流 PS 的新、未初始化的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8f5c5-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PS.</span></span>

</dd> <dt>

<span data-ttu-id="8f5c5-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ PS (D3D12 \_ 著色器 \_ 位元組位元組常數 &i)**</span><span class="sxs-lookup"><span data-stu-id="8f5c5-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="8f5c5-111">建立 CD3DX12 \_ 管線 \_ 狀態串流 PS 的新實例 \_ \_ ，並以 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ PS** 的子物件類型和從 *i* 複製的子物件資料（ [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 程式碼的結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="8f5c5-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8f5c5-112">**operator = (D3D12 \_ 著色器 \_ 位元組位元組常數& i)**</span><span class="sxs-lookup"><span data-stu-id="8f5c5-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="8f5c5-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="8f5c5-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="8f5c5-114">**運算子 D3D12 \_ 著色器 \_ 位元組 () 常數**</span><span class="sxs-lookup"><span data-stu-id="8f5c5-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="8f5c5-115">隱含轉換成 [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 結構。</span><span class="sxs-lookup"><span data-stu-id="8f5c5-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f5c5-116">備註</span><span class="sxs-lookup"><span data-stu-id="8f5c5-116">Remarks</span></span>

<span data-ttu-id="8f5c5-117">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ PS 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ \_ 資料流程**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="8f5c5-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PS>
    CD3DX12_PIPELINE_STATE_STREAM_PS;
          
```



## <a name="requirements"></a><span data-ttu-id="8f5c5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f5c5-118">Requirements</span></span>



| <span data-ttu-id="8f5c5-119">需求</span><span class="sxs-lookup"><span data-stu-id="8f5c5-119">Requirement</span></span> | <span data-ttu-id="8f5c5-120">值</span><span class="sxs-lookup"><span data-stu-id="8f5c5-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5c5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8f5c5-121">Header</span></span><br/> | <dl> <span data-ttu-id="8f5c5-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f5c5-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f5c5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f5c5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f5c5-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="8f5c5-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8f5c5-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="8f5c5-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="8f5c5-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="8f5c5-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 


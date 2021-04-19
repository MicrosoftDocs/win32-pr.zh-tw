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
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985912"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a><span data-ttu-id="e7fcc-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程子物件 \_ 結構</span><span class="sxs-lookup"><span data-stu-id="e7fcc-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT structure</span></span>

<span data-ttu-id="e7fcc-105">樣板化的 helper 結構，用來將子物件類型和子物件資料組封裝成適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-105">A templated helper structure used to encapsulate subobject type and subobject data pairs as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7fcc-106">語法</span><span class="sxs-lookup"><span data-stu-id="e7fcc-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a><span data-ttu-id="e7fcc-107">成員</span><span class="sxs-lookup"><span data-stu-id="e7fcc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7fcc-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="e7fcc-109">建立 CD3DX12 \_ 管線狀態資料流程子物件的新、未初始化的實例 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT.</span></span>

</dd> <dt>

<span data-ttu-id="e7fcc-110">**CD3DX12 \_管線 \_ 狀態 \_ 資料流程 \_** 子物件 (InnerStructType \* \* const &i) \* \*</span><span class="sxs-lookup"><span data-stu-id="e7fcc-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT(** InnerStructType\*\* const &i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="e7fcc-111">建立新的 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程子物件 \_ 範本實例，並以 [**D3D12 \_ 管線狀態子物件 \_ \_ \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) 的子物件類型和從 *i* 複製的子物件資料進行初始化。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-111">Creates a new CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template instance, initialized with a subobject type of [**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) and subobject data copied from *i*.</span></span> <span data-ttu-id="e7fcc-112">子物件類型和子物件資料類型分別會指定為範本參數、 **類型** 和 **InnerStructType**。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-112">Both the subobject type and subobject data type are given as template parameters, **Type** and **InnerStructType**, respectively.</span></span> <span data-ttu-id="e7fcc-113">如需詳細資訊，請參閱下面的備註。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-113">For more information, see Remarks below.</span></span>

</dd> <dt>

<span data-ttu-id="e7fcc-114">**運算子 = (** InnerStructType \* \* const& i) \* \*</span><span class="sxs-lookup"><span data-stu-id="e7fcc-114">**operator=(** InnerStructType\*\* const& i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="e7fcc-115">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-115">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="e7fcc-116">**operator **InnerStructType** () const**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-116">**operator **InnerStructType**() const**</span></span>
</dt> <dd>

<span data-ttu-id="e7fcc-117">隱含轉換成 **InnerStructType** 樣板參數所指定的子物件資料類型。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-117">Implicit conversion to the subobject data type given by the **InnerStructType** template parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7fcc-118">備註</span><span class="sxs-lookup"><span data-stu-id="e7fcc-118">Remarks</span></span>

<span data-ttu-id="e7fcc-119">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件是定義如下的範本：</span><span class="sxs-lookup"><span data-stu-id="e7fcc-119">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT is a template defined as follows:</span></span>


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



<span data-ttu-id="e7fcc-120">範本參數 **InnerStructType** 會指定子物件資料類型;亦即，要編碼成資料流程的子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-120">The template parameter **InnerStructType** specifies the subobject data type; that is, the subobject details to be encoded into a stream.</span></span> <span data-ttu-id="e7fcc-121">範本參數 **類型** 會指定子物件類型;也就是範本參數所指定之結構的型別 **InnerStructType**。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-121">The template parameter **Type** specifies the subobject type; that is, the type of the structure specified by the template parameter **InnerStructType**.</span></span> <span data-ttu-id="e7fcc-122">樣板參數 **operators.defaultarg** 會指定選擇性的值，當對應的範本具現化的實例為預設架構時，子物件資料將會初始化為。例如，使用 [**CD3DX12 \_ default**](cd3dx12-default.md)，將 [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)初始化為使用一般 BLEND 狀態預設值的預設結構。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-122">The template parameter **DefaultArg** specifies an optional value that the subobject data will be initialized to when an instance of the corresponding template instantiation is default-constructed; for example, to default-construct a [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) initialized with common blend-state defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

<span data-ttu-id="e7fcc-123">以下是已定義的範本具現化：</span><span class="sxs-lookup"><span data-stu-id="e7fcc-123">Here are the template instantiations that are defined:</span></span>

-   [<span data-ttu-id="e7fcc-124">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-124">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>](cd3dx12-pipeline-state-stream-flags.md)
-   [<span data-ttu-id="e7fcc-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 節點 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-node-mask.md)
-   [<span data-ttu-id="e7fcc-126">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 根 \_ 簽章**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>](cd3dx12-pipeline-state-stream-root-signature.md)
-   [<span data-ttu-id="e7fcc-127">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-127">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>](cd3dx12-pipeline-state-stream-input-layout.md)
-   [<span data-ttu-id="e7fcc-128">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 帶 \_ 剪 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-128">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [<span data-ttu-id="e7fcc-129">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 基本 \_ 拓撲**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-129">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [<span data-ttu-id="e7fcc-130">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 與**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-130">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>](cd3dx12-pipeline-state-stream-vs.md)
-   [<span data-ttu-id="e7fcc-131">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ GS**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-131">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>](cd3dx12-pipeline-state-stream-gs.md)
-   [<span data-ttu-id="e7fcc-132">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-132">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>](cd3dx12-pipeline-state-stream-stream-output.md)
-   [<span data-ttu-id="e7fcc-133">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ HS**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-133">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>](cd3dx12-pipeline-state-stream-hs.md)
-   [<span data-ttu-id="e7fcc-134">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ DS**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-134">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>](cd3dx12-pipeline-state-stream-ds.md)
-   [<span data-ttu-id="e7fcc-135">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ PS**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-135">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>](cd3dx12-pipeline-state-stream-ps.md)
-   [<span data-ttu-id="e7fcc-136">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ CS**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-136">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>](cd3dx12-pipeline-state-stream-cs.md)
-   [<span data-ttu-id="e7fcc-137">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-137">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [<span data-ttu-id="e7fcc-138">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-138">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [<span data-ttu-id="e7fcc-139">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-139">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [<span data-ttu-id="e7fcc-140">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-140">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [<span data-ttu-id="e7fcc-141">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 轉譯器**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-141">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [<span data-ttu-id="e7fcc-142">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-142">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [<span data-ttu-id="e7fcc-143">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-143">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [<span data-ttu-id="e7fcc-144">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-144">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [<span data-ttu-id="e7fcc-145">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程快取 \_ \_ PSO**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-145">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>](cd3dx12-pipeline-state-stream-cached-pso.md)

<span data-ttu-id="e7fcc-146">[**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)、 [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 深度 \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)樣板、CD3DX12 管線狀態串流 [**\_ \_ \_ \_ 深度 \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)，以及 [**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_**](cd3dx12-pipeline-state-stream-rasterizer.md)轉譯器結構，會定義為使用 [**CD3DX12 \_ 預設**](cd3dx12-default.md)值以一般預設值初始化其子物件資料。</span><span class="sxs-lookup"><span data-stu-id="e7fcc-146">The [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md), and [**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) structures are defined to initialize their subobject data with common defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7fcc-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7fcc-147">Requirements</span></span>



| <span data-ttu-id="e7fcc-148">需求</span><span class="sxs-lookup"><span data-stu-id="e7fcc-148">Requirement</span></span> | <span data-ttu-id="e7fcc-149">值</span><span class="sxs-lookup"><span data-stu-id="e7fcc-149">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fcc-150">標頭</span><span class="sxs-lookup"><span data-stu-id="e7fcc-150">Header</span></span><br/> | <dl> <span data-ttu-id="e7fcc-151"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7fcc-151"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7fcc-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7fcc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fcc-153">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="e7fcc-153">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e7fcc-154">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e7fcc-154">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 


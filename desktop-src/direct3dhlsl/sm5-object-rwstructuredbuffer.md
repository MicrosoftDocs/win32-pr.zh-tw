---
title: RWStructuredBuffer
description: 可採用結構的 T 類型的讀取/寫入緩衝區。
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- RWStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375676"
---
# <a name="rwstructuredbuffer"></a><span data-ttu-id="b5406-104">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="b5406-104">RWStructuredBuffer</span></span>

<span data-ttu-id="b5406-105">可採用結構的 T 類型的讀取/寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b5406-105">A read/write buffer that can take a T type that is a structure.</span></span>



| <span data-ttu-id="b5406-106">方法</span><span class="sxs-lookup"><span data-stu-id="b5406-106">Method</span></span>                                                                     | <span data-ttu-id="b5406-107">描述</span><span class="sxs-lookup"><span data-stu-id="b5406-107">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="b5406-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="b5406-108">**DecrementCounter**</span></span>](sm5-object-rwstructuredbuffer-decrementcounter.md) | <span data-ttu-id="b5406-109">遞減物件的隱藏計數器。</span><span class="sxs-lookup"><span data-stu-id="b5406-109">Decrements the object's hidden counter.</span></span> |
| [<span data-ttu-id="b5406-110">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="b5406-110">**GetDimensions**</span></span>](sm5-object-rwstructuredbuffer-getdimensions.md)       | <span data-ttu-id="b5406-111">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="b5406-111">Gets the resource dimensions.</span></span>           |
| [<span data-ttu-id="b5406-112">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="b5406-112">**IncrementCounter**</span></span>](sm5-object-rwstructuredbuffer-incrementcounter.md) | <span data-ttu-id="b5406-113">遞增物件的隱藏計數器。</span><span class="sxs-lookup"><span data-stu-id="b5406-113">Increments the object's hidden counter.</span></span> |
| [<span data-ttu-id="b5406-114">**載入**</span><span class="sxs-lookup"><span data-stu-id="b5406-114">**Load**</span></span>](rwstructuredbuffer-load.md)                                    | <span data-ttu-id="b5406-115">讀取緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="b5406-115">Reads buffer data.</span></span>                      |
| <span data-ttu-id="b5406-116">[**運算子\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b5406-116">[**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span></span>        | <span data-ttu-id="b5406-117">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="b5406-117">Returns a resource variable.</span></span>            |



 

<span data-ttu-id="b5406-118">資源變數也可以傳遞至任何未排序或連鎖的作業。</span><span class="sxs-lookup"><span data-stu-id="b5406-118">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="b5406-119">RWStructuredBuffer 物件的前面可以加上儲存類別 **globallycoherent**。</span><span class="sxs-lookup"><span data-stu-id="b5406-119">RWStructuredBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="b5406-120">此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。</span><span class="sxs-lookup"><span data-stu-id="b5406-120">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="b5406-121">如果沒有這個規範，記憶體屏障或同步只會清除目前群組內的 UAV。</span><span class="sxs-lookup"><span data-stu-id="b5406-121">Without this specifier, a memory barrier or sync will only flush a UAV within the current group.</span></span>

<span data-ttu-id="b5406-122">系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。</span><span class="sxs-lookup"><span data-stu-id="b5406-122">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="b5406-123">若要瞭解 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)的詳細資訊，請參閱總覽材質。</span><span class="sxs-lookup"><span data-stu-id="b5406-123">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="b5406-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b5406-124">Minimum Shader Model</span></span>

<span data-ttu-id="b5406-125">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="b5406-125">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="b5406-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b5406-126">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="b5406-127">支援</span><span class="sxs-lookup"><span data-stu-id="b5406-127">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b5406-128">[著色器模型 5](d3d11-graphics-reference-sm5.md)及更高的著色器模型 [著色器模型 4](dx-graphics-hlsl-sm4.md) (可透過 Direct3D 11 API 取得，方法是在支援計算著色器的裝置上，使用10.0 或10.1 功能等級 ([**D3D \_ 功能 \_ 等級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) 。</span><span class="sxs-lookup"><span data-stu-id="b5406-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="b5406-129">如需舊版硬體上計算著色器支援的詳細資訊，請參閱 [下層硬體上的計算](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)著色器 ) 。</span><span class="sxs-lookup"><span data-stu-id="b5406-129">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="b5406-130">是</span><span class="sxs-lookup"><span data-stu-id="b5406-130">yes</span></span>       |



 

<span data-ttu-id="b5406-131">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="b5406-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b5406-132">頂點</span><span class="sxs-lookup"><span data-stu-id="b5406-132">Vertex</span></span> | <span data-ttu-id="b5406-133">船體</span><span class="sxs-lookup"><span data-stu-id="b5406-133">Hull</span></span> | <span data-ttu-id="b5406-134">網域</span><span class="sxs-lookup"><span data-stu-id="b5406-134">Domain</span></span> | <span data-ttu-id="b5406-135">幾何</span><span class="sxs-lookup"><span data-stu-id="b5406-135">Geometry</span></span> | <span data-ttu-id="b5406-136">像素</span><span class="sxs-lookup"><span data-stu-id="b5406-136">Pixel</span></span> | <span data-ttu-id="b5406-137">計算</span><span class="sxs-lookup"><span data-stu-id="b5406-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b5406-138">x</span><span class="sxs-lookup"><span data-stu-id="b5406-138">x</span></span>     | <span data-ttu-id="b5406-139">x</span><span class="sxs-lookup"><span data-stu-id="b5406-139">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b5406-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5406-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5406-141">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="b5406-141">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


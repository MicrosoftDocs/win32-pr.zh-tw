---
title: Direct3D 12 raytracing HLSL 系統值內建函式
description: 下列 HLSL 著色器支援 Direct3D 12 raytracing 管線。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a20282e7bc0e9e4898fd361b0959cd6b6f32253
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2020
ms.locfileid: "106965261"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="1bd06-103">Direct3D 12 raytracing HLSL 系統值內建函式</span><span class="sxs-lookup"><span data-stu-id="1bd06-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="1bd06-104">系統值是使用特殊內建函式來抓取，而不是在著色器函式簽章中包含具有特殊語義的參數。</span><span class="sxs-lookup"><span data-stu-id="1bd06-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="1bd06-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="1bd06-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="1bd06-106">光線分派系統值</span><span class="sxs-lookup"><span data-stu-id="1bd06-106">Ray dispatch system values</span></span>

| <span data-ttu-id="1bd06-107">主題</span><span class="sxs-lookup"><span data-stu-id="1bd06-107">Topic</span></span> | <span data-ttu-id="1bd06-108">描述</span><span class="sxs-lookup"><span data-stu-id="1bd06-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="1bd06-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="1bd06-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="1bd06-110">取得以 **DispatchRaysDimensions** 系統值內建的寬度和高度取得的目前 x 和 y 位置。</span><span class="sxs-lookup"><span data-stu-id="1bd06-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="1bd06-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="1bd06-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="1bd06-112">原始 **DispatchRays** 呼叫中所指定之 **D3D12 \_ 分派 \_ 放射放射 \_** 值結構的寬度、高度和深度值。</span><span class="sxs-lookup"><span data-stu-id="1bd06-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="1bd06-113">光線系統值</span><span class="sxs-lookup"><span data-stu-id="1bd06-113">Ray system values</span></span>

| <span data-ttu-id="1bd06-114">主題</span><span class="sxs-lookup"><span data-stu-id="1bd06-114">Topic</span></span> | <span data-ttu-id="1bd06-115">描述</span><span class="sxs-lookup"><span data-stu-id="1bd06-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="1bd06-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="1bd06-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="1bd06-117">目前光線的世界空間原點。</span><span class="sxs-lookup"><span data-stu-id="1bd06-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="1bd06-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="1bd06-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="1bd06-119">目前光線的世界空間方向。</span><span class="sxs-lookup"><span data-stu-id="1bd06-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="1bd06-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="1bd06-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="1bd06-121">表示光線目前參數起點的 float。</span><span class="sxs-lookup"><span data-stu-id="1bd06-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="1bd06-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="1bd06-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="1bd06-123">浮點數，代表光線目前的參數結束點。</span><span class="sxs-lookup"><span data-stu-id="1bd06-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="1bd06-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="1bd06-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="1bd06-125">包含目前 **ray_flag** 旗標的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="1bd06-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="1bd06-126">基本/物件空間系統值</span><span class="sxs-lookup"><span data-stu-id="1bd06-126">Primitive/object space system values</span></span>

| <span data-ttu-id="1bd06-127">主題</span><span class="sxs-lookup"><span data-stu-id="1bd06-127">Topic</span></span> | <span data-ttu-id="1bd06-128">描述</span><span class="sxs-lookup"><span data-stu-id="1bd06-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="1bd06-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="1bd06-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="1bd06-130">最上層 raytracing 加速結構中目前實例的自動產生索引。</span><span class="sxs-lookup"><span data-stu-id="1bd06-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="1bd06-131">**Id**</span><span class="sxs-lookup"><span data-stu-id="1bd06-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="1bd06-132">最上層結構中最下層加速結構實例上實例的使用者提供識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bd06-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="1bd06-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="1bd06-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="1bd06-134">下層加速結構實例內幾何內的基本類型自動產生索引。</span><span class="sxs-lookup"><span data-stu-id="1bd06-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="1bd06-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="1bd06-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="1bd06-136">目前光線的物件空間原點。</span><span class="sxs-lookup"><span data-stu-id="1bd06-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="1bd06-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="1bd06-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="1bd06-138">目前光線的物件空間方向。</span><span class="sxs-lookup"><span data-stu-id="1bd06-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="1bd06-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="1bd06-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="1bd06-140">從物件空間轉換成世界空間的矩陣。</span><span class="sxs-lookup"><span data-stu-id="1bd06-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="1bd06-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="1bd06-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="1bd06-142">從物件空間轉換成世界空間的矩陣。</span><span class="sxs-lookup"><span data-stu-id="1bd06-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="1bd06-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="1bd06-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="1bd06-144">從世界空間轉換成物件空間的矩陣</span><span class="sxs-lookup"><span data-stu-id="1bd06-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="1bd06-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="1bd06-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="1bd06-146">從世界空間轉換成物件空間的矩陣</span><span class="sxs-lookup"><span data-stu-id="1bd06-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="1bd06-147">點擊特定系統值</span><span class="sxs-lookup"><span data-stu-id="1bd06-147">Hit-specific system values</span></span>

| <span data-ttu-id="1bd06-148">主題</span><span class="sxs-lookup"><span data-stu-id="1bd06-148">Topic</span></span> | <span data-ttu-id="1bd06-149">描述</span><span class="sxs-lookup"><span data-stu-id="1bd06-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="1bd06-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="1bd06-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="1bd06-151">傳回作為 **HitKind** 參數傳遞至 [**ReportHit**](reporthit-function.md)的值。</span><span class="sxs-lookup"><span data-stu-id="1bd06-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="1bd06-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="1bd06-152">Related topics</span></span>

* [<span data-ttu-id="1bd06-153">核心參考</span><span class="sxs-lookup"><span data-stu-id="1bd06-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="1bd06-154">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="1bd06-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)

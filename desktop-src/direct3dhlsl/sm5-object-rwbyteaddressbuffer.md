---
title: RWByteAddressBuffer
description: 以位元組為單位索引的讀取/寫入緩衝區。
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- RWByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375372"
---
# <a name="rwbyteaddressbuffer"></a><span data-ttu-id="d4a3e-104">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="d4a3e-104">RWByteAddressBuffer</span></span>

<span data-ttu-id="d4a3e-105">以位元組為單位索引的讀取/寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-105">A read/write buffer that indexes in bytes.</span></span>



| <span data-ttu-id="d4a3e-106">方法</span><span class="sxs-lookup"><span data-stu-id="d4a3e-106">Method</span></span>                                                                                          | <span data-ttu-id="d4a3e-107">描述</span><span class="sxs-lookup"><span data-stu-id="d4a3e-107">Description</span></span>                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="d4a3e-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-108">**GetDimensions**</span></span>](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | <span data-ttu-id="d4a3e-109">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="d4a3e-110">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-110">**InterlockedAdd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | <span data-ttu-id="d4a3e-111">以不可部分完成的方式加入。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-111">Adds, atomically.</span></span>                   |
| [<span data-ttu-id="d4a3e-112">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-112">**InterlockedAnd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | <span data-ttu-id="d4a3e-113">以不可部分完成的方式 And。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-113">ANDs, atomically.</span></span>                   |
| [<span data-ttu-id="d4a3e-114">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-114">**InterlockedCompareExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | <span data-ttu-id="d4a3e-115">以不可部分完成的方式比較和交換。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-115">Compares and exchanges, atomically.</span></span> |
| [<span data-ttu-id="d4a3e-116">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-116">**InterlockedCompareStore**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | <span data-ttu-id="d4a3e-117">以不可部分完成的方式比較和儲存。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-117">Compares and stores, atomically.</span></span>    |
| [<span data-ttu-id="d4a3e-118">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-118">**InterlockedExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | <span data-ttu-id="d4a3e-119">以不可部分完成的方式交換。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-119">Exchanges, atomically.</span></span>              |
| [<span data-ttu-id="d4a3e-120">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-120">**InterlockedMax**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | <span data-ttu-id="d4a3e-121">以不可部分完成的方式尋找最大值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-121">Finds the max, atomically.</span></span>          |
| [<span data-ttu-id="d4a3e-122">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-122">**InterlockedMin**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | <span data-ttu-id="d4a3e-123">以不可部分完成的方式尋找最小值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-123">Find the min, atomically.</span></span>           |
| [<span data-ttu-id="d4a3e-124">**InterlockedOr**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-124">**InterlockedOr**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | <span data-ttu-id="d4a3e-125">以不可部分完成的方式 Or。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-125">ORs, atomically.</span></span>                    |
| [<span data-ttu-id="d4a3e-126">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-126">**InterlockedXor**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | <span data-ttu-id="d4a3e-127">以不可部分完成的方式執行 xor。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-127">XORs, atomically.</span></span>                   |
| [<span data-ttu-id="d4a3e-128">**載入**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-128">**Load**</span></span>](rwbyteaddressbuffer-load.md)                                                        | <span data-ttu-id="d4a3e-129">取得一個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-129">Gets one value.</span></span>                     |
| [<span data-ttu-id="d4a3e-130">**Load2**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-130">**Load2**</span></span>](rwbyteaddressbuffer-load2.md)                                                      | <span data-ttu-id="d4a3e-131">取得兩個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-131">Gets two values.</span></span>                    |
| [<span data-ttu-id="d4a3e-132">**Load3**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-132">**Load3**</span></span>](rwbyteaddressbuffer-load3.md)                                                      | <span data-ttu-id="d4a3e-133">取得三個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-133">Gets three values.</span></span>                  |
| [<span data-ttu-id="d4a3e-134">**Load4**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-134">**Load4**</span></span>](rwbyteaddressbuffer-load4.md)                                                      | <span data-ttu-id="d4a3e-135">取得四個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-135">Gets four values.</span></span>                   |
| [<span data-ttu-id="d4a3e-136">**市集**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-136">**Store**</span></span>](sm5-object-rwbyteaddressbuffer-store.md)                                           | <span data-ttu-id="d4a3e-137">設定一個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-137">Sets one value.</span></span>                     |
| [<span data-ttu-id="d4a3e-138">**Store2**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-138">**Store2**</span></span>](sm5-object-rwbyteaddressbuffer-store2.md)                                         | <span data-ttu-id="d4a3e-139">設定兩個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-139">Sets two values.</span></span>                    |
| [<span data-ttu-id="d4a3e-140">**Store3**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-140">**Store3**</span></span>](sm5-object-rwbyteaddressbuffer-store3.md)                                         | <span data-ttu-id="d4a3e-141">設定三個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-141">Sets three values.</span></span>                  |
| [<span data-ttu-id="d4a3e-142">**Store4**</span><span class="sxs-lookup"><span data-stu-id="d4a3e-142">**Store4**</span></span>](sm5-object-rwbyteaddressbuffer-store4.md)                                         | <span data-ttu-id="d4a3e-143">設定四個值。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-143">Sets four values.</span></span>                   |



 

<span data-ttu-id="d4a3e-144">RWByteAddressBuffer 物件的前面可以加上儲存類別 **globallycoherent**。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-144">RWByteAddressBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="d4a3e-145">此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-145">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="d4a3e-146">如果沒有這個規範，記憶體屏障或同步將只會在目前群組內排清 UAV。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-146">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="d4a3e-147">系結到此資源的 UAV 格式必須以 DXGI 格式 R32 無型別格式來建立 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-147">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_R32\_TYPELESS format.</span></span>

<span data-ttu-id="d4a3e-148">系結至此資源的 UAV 必須已建立 [**D3D11 \_ 緩衝區 \_ UAV \_ 旗標 \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-148">The UAV bound to this resource must have been created with the [**D3D11\_BUFFER\_UAV\_FLAG\_RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="d4a3e-149">當您使用原始緩衝區時，可以使用 **RWByteAddressBuffer** 物件類型。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-149">You can use the **RWByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="d4a3e-150">如需有關原始的緩衝區查看的詳細資訊，請參閱 [緩衝區的原始視圖](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro)。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-150">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d4a3e-151">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d4a3e-151">Minimum Shader Model</span></span>

<span data-ttu-id="d4a3e-152">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-152">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d4a3e-153">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d4a3e-153">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="d4a3e-154">支援</span><span class="sxs-lookup"><span data-stu-id="d4a3e-154">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d4a3e-155">[著色器模型 5](d3d11-graphics-reference-sm5.md)及更高的著色器模型 [著色器模型 4](dx-graphics-hlsl-sm4.md) (可透過 Direct3D 11 API 取得，方法是在支援計算著色器的裝置上，使用10.0 或10.1 功能等級 ([**D3D \_ 功能 \_ 等級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) 。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="d4a3e-156">如需舊版硬體上計算著色器支援的詳細資訊，請參閱 [下層硬體上的計算](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)著色器 ) 。</span><span class="sxs-lookup"><span data-stu-id="d4a3e-156">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="d4a3e-157">是</span><span class="sxs-lookup"><span data-stu-id="d4a3e-157">yes</span></span>       |



 

<span data-ttu-id="d4a3e-158">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="d4a3e-158">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d4a3e-159">頂點</span><span class="sxs-lookup"><span data-stu-id="d4a3e-159">Vertex</span></span> | <span data-ttu-id="d4a3e-160">船體</span><span class="sxs-lookup"><span data-stu-id="d4a3e-160">Hull</span></span> | <span data-ttu-id="d4a3e-161">網域</span><span class="sxs-lookup"><span data-stu-id="d4a3e-161">Domain</span></span> | <span data-ttu-id="d4a3e-162">幾何</span><span class="sxs-lookup"><span data-stu-id="d4a3e-162">Geometry</span></span> | <span data-ttu-id="d4a3e-163">像素</span><span class="sxs-lookup"><span data-stu-id="d4a3e-163">Pixel</span></span> | <span data-ttu-id="d4a3e-164">計算</span><span class="sxs-lookup"><span data-stu-id="d4a3e-164">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d4a3e-165">x</span><span class="sxs-lookup"><span data-stu-id="d4a3e-165">x</span></span>     | <span data-ttu-id="d4a3e-166">x</span><span class="sxs-lookup"><span data-stu-id="d4a3e-166">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d4a3e-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4a3e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a3e-168">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="d4a3e-168">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


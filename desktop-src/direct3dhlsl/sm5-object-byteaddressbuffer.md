---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- ByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971785"
---
# <a name="byteaddressbuffer"></a><span data-ttu-id="1545a-104">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="1545a-104">ByteAddressBuffer</span></span>

<span data-ttu-id="1545a-105">以位元組為單位編制索引的唯讀緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1545a-105">A read-only buffer that is indexed in bytes.</span></span>



| <span data-ttu-id="1545a-106">方法</span><span class="sxs-lookup"><span data-stu-id="1545a-106">Method</span></span>                                                              | <span data-ttu-id="1545a-107">描述</span><span class="sxs-lookup"><span data-stu-id="1545a-107">Description</span></span>                   |
|---------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="1545a-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="1545a-108">**GetDimensions**</span></span>](sm5-object-byteaddressbuffer-getdimensions.md) | <span data-ttu-id="1545a-109">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="1545a-109">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="1545a-110">**載入**</span><span class="sxs-lookup"><span data-stu-id="1545a-110">**Load**</span></span>](byteaddressbuffer-load.md)                              | <span data-ttu-id="1545a-111">取得一個值。</span><span class="sxs-lookup"><span data-stu-id="1545a-111">Gets one value.</span></span>               |
| [<span data-ttu-id="1545a-112">**Load2**</span><span class="sxs-lookup"><span data-stu-id="1545a-112">**Load2**</span></span>](byteaddressbuffer-load2.md)                            | <span data-ttu-id="1545a-113">取得兩個值。</span><span class="sxs-lookup"><span data-stu-id="1545a-113">Gets two values.</span></span>              |
| [<span data-ttu-id="1545a-114">**Load3**</span><span class="sxs-lookup"><span data-stu-id="1545a-114">**Load3**</span></span>](byteaddressbuffer-load3.md)                            | <span data-ttu-id="1545a-115">取得三個值。</span><span class="sxs-lookup"><span data-stu-id="1545a-115">Gets three values.</span></span>            |
| [<span data-ttu-id="1545a-116">**Load4**</span><span class="sxs-lookup"><span data-stu-id="1545a-116">**Load4**</span></span>](byteaddressbuffer-load4.md)                            | <span data-ttu-id="1545a-117">取得四個值。</span><span class="sxs-lookup"><span data-stu-id="1545a-117">Gets four values.</span></span>             |



 

<span data-ttu-id="1545a-118">當您使用原始緩衝區時，可以使用 **ByteAddressBuffer** 物件類型。</span><span class="sxs-lookup"><span data-stu-id="1545a-118">You can use the **ByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="1545a-119">如需有關原始的緩衝區查看的詳細資訊，請參閱 [緩衝區的原始視圖](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro)。</span><span class="sxs-lookup"><span data-stu-id="1545a-119">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="1545a-120">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1545a-120">Minimum Shader Model</span></span>

<span data-ttu-id="1545a-121">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="1545a-121">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="1545a-122">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1545a-122">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="1545a-123">支援</span><span class="sxs-lookup"><span data-stu-id="1545a-123">Supported</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1545a-124">[著色器模型 5](d3d11-graphics-reference-sm5.md)及更高的著色器模型 [著色器模型 4](dx-graphics-hlsl-sm4.md) (可透過 Direct3D 11 API 取得，方法是在支援計算著色器的裝置上，使用10.0 或10.1 功能等級 ([**D3D \_ 功能 \_ 等級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) 。</span><span class="sxs-lookup"><span data-stu-id="1545a-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="1545a-125">如需舊版硬體上計算著色器支援的詳細資訊，請參閱 [下層硬體上的計算](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)著色器 ) 。</span><span class="sxs-lookup"><span data-stu-id="1545a-125">For more info about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="1545a-126">是</span><span class="sxs-lookup"><span data-stu-id="1545a-126">yes</span></span>       |



 

<span data-ttu-id="1545a-127">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="1545a-127">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1545a-128">頂點</span><span class="sxs-lookup"><span data-stu-id="1545a-128">Vertex</span></span> | <span data-ttu-id="1545a-129">船體</span><span class="sxs-lookup"><span data-stu-id="1545a-129">Hull</span></span> | <span data-ttu-id="1545a-130">網域</span><span class="sxs-lookup"><span data-stu-id="1545a-130">Domain</span></span> | <span data-ttu-id="1545a-131">幾何</span><span class="sxs-lookup"><span data-stu-id="1545a-131">Geometry</span></span> | <span data-ttu-id="1545a-132">像素</span><span class="sxs-lookup"><span data-stu-id="1545a-132">Pixel</span></span> | <span data-ttu-id="1545a-133">計算</span><span class="sxs-lookup"><span data-stu-id="1545a-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1545a-134">x</span><span class="sxs-lookup"><span data-stu-id="1545a-134">x</span></span>      | <span data-ttu-id="1545a-135">x</span><span class="sxs-lookup"><span data-stu-id="1545a-135">x</span></span>    | <span data-ttu-id="1545a-136">x</span><span class="sxs-lookup"><span data-stu-id="1545a-136">x</span></span>      | <span data-ttu-id="1545a-137">x</span><span class="sxs-lookup"><span data-stu-id="1545a-137">x</span></span>        | <span data-ttu-id="1545a-138">x</span><span class="sxs-lookup"><span data-stu-id="1545a-138">x</span></span>     | <span data-ttu-id="1545a-139">x</span><span class="sxs-lookup"><span data-stu-id="1545a-139">x</span></span>       |



 

<span data-ttu-id="1545a-140">如需有關位元組位址緩衝區的詳細資訊，請參閱 [位元組可定址的資源類型](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)。</span><span class="sxs-lookup"><span data-stu-id="1545a-140">For more info about a byte address buffer, see the [byte addressable resource type](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

<span data-ttu-id="1545a-141">著色器模型5也會實行 [讀寫位元組位址緩衝區](sm5-object-rwbyteaddressbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="1545a-141">Shader Model 5 also implements a [read-write byte address buffer](sm5-object-rwbyteaddressbuffer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1545a-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1545a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1545a-143">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="1545a-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


---
title: AppendStructuredBuffer
description: 輸出緩衝區，顯示為著色器可以附加的資料流程。 只有結構化緩衝區可以採用結構的 T 類型。
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- AppendStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682579"
---
# <a name="appendstructuredbuffer"></a><span data-ttu-id="be748-105">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="be748-105">AppendStructuredBuffer</span></span>

<span data-ttu-id="be748-106">輸出緩衝區，顯示為著色器可以附加的資料流程。</span><span class="sxs-lookup"><span data-stu-id="be748-106">Output buffer that appears as a stream the shader may append to.</span></span> <span data-ttu-id="be748-107">只有結構化緩衝區可以採用結構的 T 類型。</span><span class="sxs-lookup"><span data-stu-id="be748-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="be748-108">方法</span><span class="sxs-lookup"><span data-stu-id="be748-108">Method</span></span>                                                                   | <span data-ttu-id="be748-109">描述</span><span class="sxs-lookup"><span data-stu-id="be748-109">Description</span></span>                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="be748-110">**附加**</span><span class="sxs-lookup"><span data-stu-id="be748-110">**Append**</span></span>](sm5-object-appendstructuredbuffer-append.md)               | <span data-ttu-id="be748-111">將值附加至緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="be748-111">Appends a value to the end of the buffer.</span></span> |
| [<span data-ttu-id="be748-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="be748-112">**GetDimensions**</span></span>](sm5-object-appendstructuredbuffer-getdimensions.md) | <span data-ttu-id="be748-113">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="be748-113">Gets the resource dimensions.</span></span>             |



 

<span data-ttu-id="be748-114">系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。</span><span class="sxs-lookup"><span data-stu-id="be748-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="be748-115">系結至此資源的 UAV 必須使用 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 附加**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)來建立。</span><span class="sxs-lookup"><span data-stu-id="be748-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="be748-116">如需有關附加結構化緩衝區的詳細資訊，請參閱這兩個區段： [附加和使用緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) 和 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)。</span><span class="sxs-lookup"><span data-stu-id="be748-116">For more information about an append structured buffer, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="be748-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="be748-117">Minimum Shader Model</span></span>

<span data-ttu-id="be748-118">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="be748-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="be748-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="be748-119">Shader Model</span></span>                                                                | <span data-ttu-id="be748-120">支援</span><span class="sxs-lookup"><span data-stu-id="be748-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="be748-121">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="be748-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="be748-122">是</span><span class="sxs-lookup"><span data-stu-id="be748-122">yes</span></span>       |



 

<span data-ttu-id="be748-123">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="be748-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="be748-124">頂點</span><span class="sxs-lookup"><span data-stu-id="be748-124">Vertex</span></span> | <span data-ttu-id="be748-125">船體</span><span class="sxs-lookup"><span data-stu-id="be748-125">Hull</span></span> | <span data-ttu-id="be748-126">網域</span><span class="sxs-lookup"><span data-stu-id="be748-126">Domain</span></span> | <span data-ttu-id="be748-127">幾何</span><span class="sxs-lookup"><span data-stu-id="be748-127">Geometry</span></span> | <span data-ttu-id="be748-128">像素</span><span class="sxs-lookup"><span data-stu-id="be748-128">Pixel</span></span> | <span data-ttu-id="be748-129">計算</span><span class="sxs-lookup"><span data-stu-id="be748-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="be748-130">x</span><span class="sxs-lookup"><span data-stu-id="be748-130">x</span></span>     | <span data-ttu-id="be748-131">x</span><span class="sxs-lookup"><span data-stu-id="be748-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="be748-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be748-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be748-133">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="be748-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 
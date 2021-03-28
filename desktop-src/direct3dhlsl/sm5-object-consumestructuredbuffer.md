---
title: ConsumeStructuredBuffer
description: 顯示為數據流的輸入緩衝區，表示著色器可能從中提取值。 只有結構化緩衝區可以採用結構的 T 類型。
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- ConsumeStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991022"
---
# <a name="consumestructuredbuffer"></a><span data-ttu-id="206f6-105">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="206f6-105">ConsumeStructuredBuffer</span></span>

<span data-ttu-id="206f6-106">顯示為數據流的輸入緩衝區，表示著色器可能從中提取值。</span><span class="sxs-lookup"><span data-stu-id="206f6-106">An input buffer that appears as a stream the shader may pull values from.</span></span> <span data-ttu-id="206f6-107">只有結構化緩衝區可以採用結構的 T 類型。</span><span class="sxs-lookup"><span data-stu-id="206f6-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="206f6-108">方法</span><span class="sxs-lookup"><span data-stu-id="206f6-108">Method</span></span>                                                                    | <span data-ttu-id="206f6-109">描述</span><span class="sxs-lookup"><span data-stu-id="206f6-109">Description</span></span>                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="206f6-110">**取用**</span><span class="sxs-lookup"><span data-stu-id="206f6-110">**Consume**</span></span>](sm5-object-consumestructuredbuffer-consume.md)             | <span data-ttu-id="206f6-111">從緩衝區的結尾移除值。</span><span class="sxs-lookup"><span data-stu-id="206f6-111">Removes a value from the end of the buffer.</span></span> |
| [<span data-ttu-id="206f6-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="206f6-112">**GetDimensions**</span></span>](sm5-object-consumestructuredbuffer-getdimensions.md) | <span data-ttu-id="206f6-113">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="206f6-113">Gets the resource dimensions.</span></span>               |



 

<span data-ttu-id="206f6-114">系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。</span><span class="sxs-lookup"><span data-stu-id="206f6-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="206f6-115">系結至此資源的 UAV 必須使用 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 附加**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)來建立。</span><span class="sxs-lookup"><span data-stu-id="206f6-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="206f6-116">如需使用結構化緩衝區的詳細資訊，請參閱這兩個區段： [附加和使用緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) 和 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)。</span><span class="sxs-lookup"><span data-stu-id="206f6-116">For more info about consume structured buffers, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="206f6-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="206f6-117">Minimum Shader Model</span></span>

<span data-ttu-id="206f6-118">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="206f6-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="206f6-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="206f6-119">Shader Model</span></span>                                                                | <span data-ttu-id="206f6-120">支援</span><span class="sxs-lookup"><span data-stu-id="206f6-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="206f6-121">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="206f6-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="206f6-122">是</span><span class="sxs-lookup"><span data-stu-id="206f6-122">yes</span></span>       |



 

<span data-ttu-id="206f6-123">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="206f6-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="206f6-124">頂點</span><span class="sxs-lookup"><span data-stu-id="206f6-124">Vertex</span></span> | <span data-ttu-id="206f6-125">船體</span><span class="sxs-lookup"><span data-stu-id="206f6-125">Hull</span></span> | <span data-ttu-id="206f6-126">網域</span><span class="sxs-lookup"><span data-stu-id="206f6-126">Domain</span></span> | <span data-ttu-id="206f6-127">幾何</span><span class="sxs-lookup"><span data-stu-id="206f6-127">Geometry</span></span> | <span data-ttu-id="206f6-128">像素</span><span class="sxs-lookup"><span data-stu-id="206f6-128">Pixel</span></span> | <span data-ttu-id="206f6-129">計算</span><span class="sxs-lookup"><span data-stu-id="206f6-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="206f6-130">x</span><span class="sxs-lookup"><span data-stu-id="206f6-130">x</span></span>     | <span data-ttu-id="206f6-131">x</span><span class="sxs-lookup"><span data-stu-id="206f6-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="206f6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="206f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206f6-133">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="206f6-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 
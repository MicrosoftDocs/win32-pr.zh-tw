---
title: StructuredBuffer
description: 唯讀緩衝區，它可以採用結構的 T 型別。
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- StructuredBuffer HLSL
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990927"
---
# <a name="structuredbuffer"></a><span data-ttu-id="377e6-104">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="377e6-104">StructuredBuffer</span></span>

<span data-ttu-id="377e6-105">唯讀緩衝區，它可以採用結構的 T 型別。</span><span class="sxs-lookup"><span data-stu-id="377e6-105">A read-only buffer, which can take a T type that is a structure.</span></span>



| <span data-ttu-id="377e6-106">方法</span><span class="sxs-lookup"><span data-stu-id="377e6-106">Method</span></span>                                                             | <span data-ttu-id="377e6-107">描述</span><span class="sxs-lookup"><span data-stu-id="377e6-107">Description</span></span>                            |
|--------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="377e6-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="377e6-108">**GetDimensions**</span></span>](sm5-object-structuredbuffer-getdimensions.md) | <span data-ttu-id="377e6-109">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="377e6-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="377e6-110">**載入**</span><span class="sxs-lookup"><span data-stu-id="377e6-110">**Load**</span></span>](structuredbuffer-load.md)                              | <span data-ttu-id="377e6-111">讀取緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="377e6-111">Reads buffer data.</span></span>                     |
| <span data-ttu-id="377e6-112">[**運算子\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="377e6-112">[**Operator\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="377e6-113">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="377e6-113">Returns a read-only resource variable.</span></span> |



 

<span data-ttu-id="377e6-114">系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。</span><span class="sxs-lookup"><span data-stu-id="377e6-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="377e6-115">若要瞭解 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)的詳細資訊，請參閱總覽材質。</span><span class="sxs-lookup"><span data-stu-id="377e6-115">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="377e6-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="377e6-116">Minimum Shader Model</span></span>

<span data-ttu-id="377e6-117">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="377e6-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="377e6-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="377e6-118">Shader Model</span></span>                                                                                                                                                                                                            | <span data-ttu-id="377e6-119">支援</span><span class="sxs-lookup"><span data-stu-id="377e6-119">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="377e6-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 4 (可用於某些 direct3d 10 裝置上 direct3d 11 中的計算和圖元著色 [器](dx-graphics-hlsl-sm4.md) 。 ) </span><span class="sxs-lookup"><span data-stu-id="377e6-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available for compute and pixel shaders in Direct3D 11 on some Direct3D 10 devices.)</span></span><br/> | <span data-ttu-id="377e6-121">是</span><span class="sxs-lookup"><span data-stu-id="377e6-121">yes</span></span>       |



 

<span data-ttu-id="377e6-122">下列著色器類型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="377e6-122">This object is supported for the following types of shaders.</span></span>



| <span data-ttu-id="377e6-123">頂點</span><span class="sxs-lookup"><span data-stu-id="377e6-123">Vertex</span></span> | <span data-ttu-id="377e6-124">船體</span><span class="sxs-lookup"><span data-stu-id="377e6-124">Hull</span></span> | <span data-ttu-id="377e6-125">網域</span><span class="sxs-lookup"><span data-stu-id="377e6-125">Domain</span></span> | <span data-ttu-id="377e6-126">幾何</span><span class="sxs-lookup"><span data-stu-id="377e6-126">Geometry</span></span> | <span data-ttu-id="377e6-127">像素</span><span class="sxs-lookup"><span data-stu-id="377e6-127">Pixel</span></span> | <span data-ttu-id="377e6-128">計算</span><span class="sxs-lookup"><span data-stu-id="377e6-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="377e6-129">x</span><span class="sxs-lookup"><span data-stu-id="377e6-129">x</span></span>      | <span data-ttu-id="377e6-130">x</span><span class="sxs-lookup"><span data-stu-id="377e6-130">x</span></span>    | <span data-ttu-id="377e6-131">x</span><span class="sxs-lookup"><span data-stu-id="377e6-131">x</span></span>      | <span data-ttu-id="377e6-132">x</span><span class="sxs-lookup"><span data-stu-id="377e6-132">x</span></span>        | <span data-ttu-id="377e6-133">x</span><span class="sxs-lookup"><span data-stu-id="377e6-133">x</span></span>     | <span data-ttu-id="377e6-134">x</span><span class="sxs-lookup"><span data-stu-id="377e6-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="377e6-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="377e6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="377e6-136">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="377e6-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


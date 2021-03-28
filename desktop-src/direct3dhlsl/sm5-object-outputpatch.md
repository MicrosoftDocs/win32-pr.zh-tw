---
title: OutputPatch
description: OutputPatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- OutputPatch HLSL
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022318"
---
# <a name="outputpatch"></a><span data-ttu-id="365ca-104">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="365ca-104">OutputPatch</span></span>

<span data-ttu-id="365ca-105">代表輸出控制點的陣列，這些點可供輪廓著色器的 patch 常數函式和網域著色器使用。</span><span class="sxs-lookup"><span data-stu-id="365ca-105">Represents an array of output control points that are available to the hull shader's patch-constant function as well as the domain shader.</span></span>



| <span data-ttu-id="365ca-106">方法</span><span class="sxs-lookup"><span data-stu-id="365ca-106">Method</span></span>                                                       | <span data-ttu-id="365ca-107">描述</span><span class="sxs-lookup"><span data-stu-id="365ca-107">Description</span></span>                         |
|--------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="365ca-108">[**運算子\[\]**](sm5-object-outputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="365ca-108">[**Operator\[\]**](sm5-object-outputpatch-operatorindex.md)</span></span> | <span data-ttu-id="365ca-109">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="365ca-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="365ca-110">此外，InputPatch 類別支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="365ca-110">In addition, the InputPatch class supports the following properties:</span></span>



| <span data-ttu-id="365ca-111">屬性</span><span class="sxs-lookup"><span data-stu-id="365ca-111">Properties</span></span> | <span data-ttu-id="365ca-112">類型</span><span class="sxs-lookup"><span data-stu-id="365ca-112">Type</span></span> | <span data-ttu-id="365ca-113">Description</span><span class="sxs-lookup"><span data-stu-id="365ca-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="365ca-114">長度</span><span class="sxs-lookup"><span data-stu-id="365ca-114">Length</span></span>     | <span data-ttu-id="365ca-115">uint</span><span class="sxs-lookup"><span data-stu-id="365ca-115">uint</span></span> | <span data-ttu-id="365ca-116">控制點的數目。</span><span class="sxs-lookup"><span data-stu-id="365ca-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="365ca-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="365ca-117">Minimum Shader Model</span></span>

<span data-ttu-id="365ca-118">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="365ca-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="365ca-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="365ca-119">Shader Model</span></span>                                                                | <span data-ttu-id="365ca-120">支援</span><span class="sxs-lookup"><span data-stu-id="365ca-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="365ca-121">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="365ca-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="365ca-122">是</span><span class="sxs-lookup"><span data-stu-id="365ca-122">yes</span></span>       |



 

<span data-ttu-id="365ca-123">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="365ca-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="365ca-124">頂點</span><span class="sxs-lookup"><span data-stu-id="365ca-124">Vertex</span></span> | <span data-ttu-id="365ca-125">船體</span><span class="sxs-lookup"><span data-stu-id="365ca-125">Hull</span></span> | <span data-ttu-id="365ca-126">網域</span><span class="sxs-lookup"><span data-stu-id="365ca-126">Domain</span></span> | <span data-ttu-id="365ca-127">幾何</span><span class="sxs-lookup"><span data-stu-id="365ca-127">Geometry</span></span> | <span data-ttu-id="365ca-128">像素</span><span class="sxs-lookup"><span data-stu-id="365ca-128">Pixel</span></span> | <span data-ttu-id="365ca-129">計算</span><span class="sxs-lookup"><span data-stu-id="365ca-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="365ca-130">x</span><span class="sxs-lookup"><span data-stu-id="365ca-130">x</span></span>    | <span data-ttu-id="365ca-131">x</span><span class="sxs-lookup"><span data-stu-id="365ca-131">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="365ca-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="365ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="365ca-133">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="365ca-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





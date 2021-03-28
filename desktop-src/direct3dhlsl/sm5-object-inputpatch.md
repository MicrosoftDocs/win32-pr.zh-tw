---
title: InputPatch
description: 代表可供輪廓著色器作為輸入的控制點陣列。
ms.assetid: a2eeb45a-85b2-4ed0-b071-fcbb8abf4f2d
keywords:
- InputPatch HLSL
topic_type:
- apiref
api_name:
- InputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a882d032133ccb7bc98a34b3ef99551aa18fa51b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990667"
---
# <a name="inputpatch"></a><span data-ttu-id="616d0-104">InputPatch</span><span class="sxs-lookup"><span data-stu-id="616d0-104">InputPatch</span></span>

<span data-ttu-id="616d0-105">代表可供輪廓著色器作為輸入的控制點陣列。</span><span class="sxs-lookup"><span data-stu-id="616d0-105">Represents an array of control points that are available to the hull shader as inputs.</span></span>



| <span data-ttu-id="616d0-106">方法</span><span class="sxs-lookup"><span data-stu-id="616d0-106">Method</span></span>                                                      | <span data-ttu-id="616d0-107">描述</span><span class="sxs-lookup"><span data-stu-id="616d0-107">Description</span></span>                         |
|-------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="616d0-108">[**運算子\[\]**](sm5-object-inputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="616d0-108">[**Operator\[\]**](sm5-object-inputpatch-operatorindex.md)</span></span> | <span data-ttu-id="616d0-109">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="616d0-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="616d0-110">InputPatch 類別也支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="616d0-110">The InputPatch class also supports the following properties:</span></span>



| <span data-ttu-id="616d0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="616d0-111">Properties</span></span> | <span data-ttu-id="616d0-112">類型</span><span class="sxs-lookup"><span data-stu-id="616d0-112">Type</span></span> | <span data-ttu-id="616d0-113">Description</span><span class="sxs-lookup"><span data-stu-id="616d0-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="616d0-114">長度</span><span class="sxs-lookup"><span data-stu-id="616d0-114">Length</span></span>     | <span data-ttu-id="616d0-115">uint</span><span class="sxs-lookup"><span data-stu-id="616d0-115">uint</span></span> | <span data-ttu-id="616d0-116">控制點的數目。</span><span class="sxs-lookup"><span data-stu-id="616d0-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="616d0-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="616d0-117">Minimum Shader Model</span></span>

<span data-ttu-id="616d0-118">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="616d0-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="616d0-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="616d0-119">Shader Model</span></span>                                                                | <span data-ttu-id="616d0-120">支援</span><span class="sxs-lookup"><span data-stu-id="616d0-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="616d0-121">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="616d0-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="616d0-122">是</span><span class="sxs-lookup"><span data-stu-id="616d0-122">yes</span></span>       |



 

<span data-ttu-id="616d0-123">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="616d0-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="616d0-124">頂點</span><span class="sxs-lookup"><span data-stu-id="616d0-124">Vertex</span></span> | <span data-ttu-id="616d0-125">船體</span><span class="sxs-lookup"><span data-stu-id="616d0-125">Hull</span></span> | <span data-ttu-id="616d0-126">網域</span><span class="sxs-lookup"><span data-stu-id="616d0-126">Domain</span></span> | <span data-ttu-id="616d0-127">幾何</span><span class="sxs-lookup"><span data-stu-id="616d0-127">Geometry</span></span> | <span data-ttu-id="616d0-128">像素</span><span class="sxs-lookup"><span data-stu-id="616d0-128">Pixel</span></span> | <span data-ttu-id="616d0-129">計算</span><span class="sxs-lookup"><span data-stu-id="616d0-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="616d0-130">x</span><span class="sxs-lookup"><span data-stu-id="616d0-130">x</span></span>    |        | <span data-ttu-id="616d0-131">x</span><span class="sxs-lookup"><span data-stu-id="616d0-131">x</span></span>        |       |         |



 

## <a name="see-also"></a><span data-ttu-id="616d0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="616d0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616d0-133">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="616d0-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





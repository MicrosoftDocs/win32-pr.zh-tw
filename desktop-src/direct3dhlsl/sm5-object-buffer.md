---
title: Buffer
description: Buffer
ms.assetid: 7f552b9b-c5fb-4bc2-a7ae-61983379db38
keywords:
- 緩衝區 HLSL
topic_type:
- apiref
api_name:
- Buffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1754272fd90cedc5a806543dd83a99cdcd9455
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373217"
---
# <a name="buffer"></a><span data-ttu-id="a3782-104">Buffer</span><span class="sxs-lookup"><span data-stu-id="a3782-104">Buffer</span></span>

<span data-ttu-id="a3782-105">存在於著色器模型4加上資源變數和緩衝區資訊中的緩衝區類型。</span><span class="sxs-lookup"><span data-stu-id="a3782-105">Buffer type as it exists in Shader Model 4 plus resource variables and buffer info.</span></span>



| <span data-ttu-id="a3782-106">方法</span><span class="sxs-lookup"><span data-stu-id="a3782-106">Method</span></span>                                                   | <span data-ttu-id="a3782-107">描述</span><span class="sxs-lookup"><span data-stu-id="a3782-107">Description</span></span>                         |
|----------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="a3782-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="a3782-108">**GetDimensions**</span></span>](sm5-object-buffer-getdimensions.md) | <span data-ttu-id="a3782-109">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="a3782-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="a3782-110">**載入**</span><span class="sxs-lookup"><span data-stu-id="a3782-110">**Load**</span></span>](buffer-load.md)                              | <span data-ttu-id="a3782-111">讀取緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="a3782-111">Reads buffer data.</span></span>                  |
| <span data-ttu-id="a3782-112">[**運算子\[\]**](sm5-object-buffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="a3782-112">[**Operator\[\]**](sm5-object-buffer-operatorindex.md)</span></span>  | <span data-ttu-id="a3782-113">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="a3782-113">Gets a read-only resource variable.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a3782-114">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a3782-114">Minimum Shader Model</span></span>

<span data-ttu-id="a3782-115">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="a3782-115">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="a3782-116">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a3782-116">Shader Model</span></span>                                                                | <span data-ttu-id="a3782-117">支援</span><span class="sxs-lookup"><span data-stu-id="a3782-117">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a3782-118">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="a3782-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a3782-119">是</span><span class="sxs-lookup"><span data-stu-id="a3782-119">yes</span></span>       |



 

<span data-ttu-id="a3782-120">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="a3782-120">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a3782-121">頂點</span><span class="sxs-lookup"><span data-stu-id="a3782-121">Vertex</span></span> | <span data-ttu-id="a3782-122">船體</span><span class="sxs-lookup"><span data-stu-id="a3782-122">Hull</span></span> | <span data-ttu-id="a3782-123">網域</span><span class="sxs-lookup"><span data-stu-id="a3782-123">Domain</span></span> | <span data-ttu-id="a3782-124">幾何</span><span class="sxs-lookup"><span data-stu-id="a3782-124">Geometry</span></span> | <span data-ttu-id="a3782-125">像素</span><span class="sxs-lookup"><span data-stu-id="a3782-125">Pixel</span></span> | <span data-ttu-id="a3782-126">計算</span><span class="sxs-lookup"><span data-stu-id="a3782-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a3782-127">x</span><span class="sxs-lookup"><span data-stu-id="a3782-127">x</span></span>      | <span data-ttu-id="a3782-128">x</span><span class="sxs-lookup"><span data-stu-id="a3782-128">x</span></span>    | <span data-ttu-id="a3782-129">x</span><span class="sxs-lookup"><span data-stu-id="a3782-129">x</span></span>      | <span data-ttu-id="a3782-130">x</span><span class="sxs-lookup"><span data-stu-id="a3782-130">x</span></span>        | <span data-ttu-id="a3782-131">x</span><span class="sxs-lookup"><span data-stu-id="a3782-131">x</span></span>     | <span data-ttu-id="a3782-132">x</span><span class="sxs-lookup"><span data-stu-id="a3782-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a3782-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3782-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3782-134">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="a3782-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





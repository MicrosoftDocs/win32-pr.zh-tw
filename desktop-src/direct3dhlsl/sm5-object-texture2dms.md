---
title: Texture2DMS
description: Texture2DMS 類型 (存在於著色器模型 4) 加上資源變數中。
ms.assetid: afda7324-680e-432a-a445-d90bd708e5e0
keywords:
- Texture2DMS HLSL
topic_type:
- apiref
api_name:
- Texture2DMS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c16c69a4fa0fd35ce7b12d69f880daa4b8345d02
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022358"
---
# <a name="texture2dms"></a><span data-ttu-id="8a634-104">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="8a634-104">Texture2DMS</span></span>

<span data-ttu-id="8a634-105">Texture2DMS 類型 (存在於著色器模型 4) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="8a634-105">Texture2DMS type (as it exists in Shader Model 4) plus resource variables.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a634-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="8a634-106">In this section</span></span>



| <span data-ttu-id="8a634-107">主題</span><span class="sxs-lookup"><span data-stu-id="8a634-107">Topic</span></span>                                                                                    | <span data-ttu-id="8a634-108">描述</span><span class="sxs-lookup"><span data-stu-id="8a634-108">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a634-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="8a634-109">**GetDimensions**</span></span>](sm5-object-texture2dms-getdimensions.md)<br/>                 | <span data-ttu-id="8a634-110">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="8a634-110">Returns the dimensions of the resource.</span></span><br/>                                          |
| [<span data-ttu-id="8a634-111">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="8a634-111">**GetSamplePosition**</span></span>](sm5-object-texture2dms-getsampleposition.md)<br/>         | <span data-ttu-id="8a634-112">傳回所提供之範例索引的範例位置。</span><span class="sxs-lookup"><span data-stu-id="8a634-112">Returns the sample position for the sample index provided.</span></span><br/>                       |
| [<span data-ttu-id="8a634-113">**載入方法**</span><span class="sxs-lookup"><span data-stu-id="8a634-113">**Load methods**</span></span>](texture2dms-load.md)<br/>                                      | <span data-ttu-id="8a634-114">在提供的位置和樣本索引上，抓取資源的值。</span><span class="sxs-lookup"><span data-stu-id="8a634-114">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="8a634-115">[**樣品。運算元\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="8a634-115">[**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span></span><br/> | <span data-ttu-id="8a634-116">在提供的位置和樣本索引上，抓取資源的值。</span><span class="sxs-lookup"><span data-stu-id="8a634-116">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="8a634-117">[**運算子\[\]**](sm5-object-texture2dms-operator1.md)</span><span class="sxs-lookup"><span data-stu-id="8a634-117">[**Operator\[\]**](sm5-object-texture2dms-operator1.md)</span></span><br/>                      | <span data-ttu-id="8a634-118">從位於範例索引0所提供位置的資源抓取值。</span><span class="sxs-lookup"><span data-stu-id="8a634-118">Retrieves a value from the resource at the location provided at sample index 0.</span></span> <br/> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8a634-119">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="8a634-119">Minimum Shader Model</span></span>

<span data-ttu-id="8a634-120">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="8a634-120">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="8a634-121">著色器模型</span><span class="sxs-lookup"><span data-stu-id="8a634-121">Shader Model</span></span>              | <span data-ttu-id="8a634-122">支援</span><span class="sxs-lookup"><span data-stu-id="8a634-122">Supported</span></span> |
|---------------------------|-----------|
| <span data-ttu-id="8a634-123">著色器模型4和更新版本</span><span class="sxs-lookup"><span data-stu-id="8a634-123">Shader model 4 and higher</span></span> | <span data-ttu-id="8a634-124">是</span><span class="sxs-lookup"><span data-stu-id="8a634-124">yes</span></span>       |



 

<span data-ttu-id="8a634-125">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="8a634-125">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8a634-126">頂點</span><span class="sxs-lookup"><span data-stu-id="8a634-126">Vertex</span></span> | <span data-ttu-id="8a634-127">船體</span><span class="sxs-lookup"><span data-stu-id="8a634-127">Hull</span></span> | <span data-ttu-id="8a634-128">網域</span><span class="sxs-lookup"><span data-stu-id="8a634-128">Domain</span></span> | <span data-ttu-id="8a634-129">幾何</span><span class="sxs-lookup"><span data-stu-id="8a634-129">Geometry</span></span> | <span data-ttu-id="8a634-130">像素</span><span class="sxs-lookup"><span data-stu-id="8a634-130">Pixel</span></span> | <span data-ttu-id="8a634-131">計算</span><span class="sxs-lookup"><span data-stu-id="8a634-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8a634-132">x</span><span class="sxs-lookup"><span data-stu-id="8a634-132">x</span></span>      | <span data-ttu-id="8a634-133">x</span><span class="sxs-lookup"><span data-stu-id="8a634-133">x</span></span>    | <span data-ttu-id="8a634-134">x</span><span class="sxs-lookup"><span data-stu-id="8a634-134">x</span></span>      | <span data-ttu-id="8a634-135">x</span><span class="sxs-lookup"><span data-stu-id="8a634-135">x</span></span>        | <span data-ttu-id="8a634-136">x</span><span class="sxs-lookup"><span data-stu-id="8a634-136">x</span></span>     | <span data-ttu-id="8a634-137">x</span><span class="sxs-lookup"><span data-stu-id="8a634-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8a634-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a634-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a634-139">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="8a634-139">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 






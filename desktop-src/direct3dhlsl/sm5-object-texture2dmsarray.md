---
title: Texture2DMSArray
description: Texture2DMSArray
ms.assetid: 4200eba8-a9e5-41ba-b04c-4ac7b20274d2
keywords:
- Texture2DMSArray HLSL
topic_type:
- apiref
api_name:
- Texture2DMSArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: effe4819c674a7909cc445b9e9f7b5322fae7676
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "104195702"
---
# <a name="texture2dmsarray"></a><span data-ttu-id="d03a5-104">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d03a5-104">Texture2DMSArray</span></span>

<span data-ttu-id="d03a5-105">Texture2DMSArray 類型 (存在於著色器模型 4) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="d03a5-105">Texture2DMSArray type (as it exists in Shader Model 4) plus resource variables.</span></span>



| <span data-ttu-id="d03a5-106">方法</span><span class="sxs-lookup"><span data-stu-id="d03a5-106">Method</span></span>                                                                             | <span data-ttu-id="d03a5-107">描述</span><span class="sxs-lookup"><span data-stu-id="d03a5-107">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d03a5-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="d03a5-108">**GetDimensions**</span></span>](sm5-object-texture2dmsarray-getdimensions.md)                  | <span data-ttu-id="d03a5-109">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="d03a5-109">Gets the resource dimensions.</span></span>                      |
| [<span data-ttu-id="d03a5-110">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="d03a5-110">**GetSamplePosition**</span></span>](sm5-object-texture2dmsarray-getsampleposition.md)          | <span data-ttu-id="d03a5-111">取得指定之範例的位置。</span><span class="sxs-lookup"><span data-stu-id="d03a5-111">Gets the position of the specified sample.</span></span>         |
| [<span data-ttu-id="d03a5-112">**載入**</span><span class="sxs-lookup"><span data-stu-id="d03a5-112">**Load**</span></span>](texture2dmsarray-load.md)                                               | <span data-ttu-id="d03a5-113">取得一個值。</span><span class="sxs-lookup"><span data-stu-id="d03a5-113">Gets one value.</span></span>                                    |
| <span data-ttu-id="d03a5-114">[**樣品。運算元\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="d03a5-114">[**sample.Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span></span>  | <span data-ttu-id="d03a5-115">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="d03a5-115">Gets a read-only resource variable.</span></span>                |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d03a5-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d03a5-116">Minimum Shader Model</span></span>

<span data-ttu-id="d03a5-117">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="d03a5-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d03a5-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d03a5-118">Shader Model</span></span>                                                                | <span data-ttu-id="d03a5-119">支援</span><span class="sxs-lookup"><span data-stu-id="d03a5-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d03a5-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d03a5-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d03a5-121">是</span><span class="sxs-lookup"><span data-stu-id="d03a5-121">yes</span></span>       |



 

<span data-ttu-id="d03a5-122">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="d03a5-122">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d03a5-123">頂點</span><span class="sxs-lookup"><span data-stu-id="d03a5-123">Vertex</span></span> | <span data-ttu-id="d03a5-124">船體</span><span class="sxs-lookup"><span data-stu-id="d03a5-124">Hull</span></span> | <span data-ttu-id="d03a5-125">網域</span><span class="sxs-lookup"><span data-stu-id="d03a5-125">Domain</span></span> | <span data-ttu-id="d03a5-126">幾何</span><span class="sxs-lookup"><span data-stu-id="d03a5-126">Geometry</span></span> | <span data-ttu-id="d03a5-127">像素</span><span class="sxs-lookup"><span data-stu-id="d03a5-127">Pixel</span></span> | <span data-ttu-id="d03a5-128">計算</span><span class="sxs-lookup"><span data-stu-id="d03a5-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d03a5-129">x</span><span class="sxs-lookup"><span data-stu-id="d03a5-129">x</span></span>      | <span data-ttu-id="d03a5-130">x</span><span class="sxs-lookup"><span data-stu-id="d03a5-130">x</span></span>    | <span data-ttu-id="d03a5-131">x</span><span class="sxs-lookup"><span data-stu-id="d03a5-131">x</span></span>      | <span data-ttu-id="d03a5-132">x</span><span class="sxs-lookup"><span data-stu-id="d03a5-132">x</span></span>        | <span data-ttu-id="d03a5-133">x</span><span class="sxs-lookup"><span data-stu-id="d03a5-133">x</span></span>     | <span data-ttu-id="d03a5-134">x</span><span class="sxs-lookup"><span data-stu-id="d03a5-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d03a5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d03a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03a5-136">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="d03a5-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





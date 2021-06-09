---
title: SV_InsideTessFactor
description: 定義修補程式介面內的鑲嵌量。
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826612"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="36d04-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="36d04-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="36d04-105">定義修補程式介面內的鑲嵌量。</span><span class="sxs-lookup"><span data-stu-id="36d04-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="36d04-106">類型</span><span class="sxs-lookup"><span data-stu-id="36d04-106">Type</span></span>



|  <span data-ttu-id="36d04-107">類型</span><span class="sxs-lookup"><span data-stu-id="36d04-107">Type</span></span>          | <span data-ttu-id="36d04-108">輸入拓撲</span><span class="sxs-lookup"><span data-stu-id="36d04-108">Input topology</span></span>               |
|------------|----------------|
| <span data-ttu-id="36d04-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="36d04-109">float\[2\]</span></span> | <span data-ttu-id="36d04-110">四個修補程式</span><span class="sxs-lookup"><span data-stu-id="36d04-110">quad patch</span></span>     |
| <span data-ttu-id="36d04-111">FLOAT</span><span class="sxs-lookup"><span data-stu-id="36d04-111">float</span></span>      | <span data-ttu-id="36d04-112">三個修補程式</span><span class="sxs-lookup"><span data-stu-id="36d04-112">tri patch</span></span>      |
| <span data-ttu-id="36d04-113">unused</span><span class="sxs-lookup"><span data-stu-id="36d04-113">unused</span></span>     | <span data-ttu-id="36d04-114">等值 線</span><span class="sxs-lookup"><span data-stu-id="36d04-114">isoline</span></span>        |



 

<span data-ttu-id="36d04-115">鑲嵌式因數必須宣告為數組;它們無法封裝成單一向量。</span><span class="sxs-lookup"><span data-stu-id="36d04-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="36d04-116">備註</span><span class="sxs-lookup"><span data-stu-id="36d04-116">Remarks</span></span>

<span data-ttu-id="36d04-117">此值必須在輪廓著色器的 patch 常數函式期間定義。</span><span class="sxs-lookup"><span data-stu-id="36d04-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="36d04-118">如果使用四或三個修補程式，則為輪廓著色器所需的輸出值。</span><span class="sxs-lookup"><span data-stu-id="36d04-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="36d04-119">此值是網域著色器的必要輸入，以便硬體透過鑲嵌來比對簽章。</span><span class="sxs-lookup"><span data-stu-id="36d04-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="36d04-120">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="36d04-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="36d04-121">頂點</span><span class="sxs-lookup"><span data-stu-id="36d04-121">Vertex</span></span> | <span data-ttu-id="36d04-122">船體</span><span class="sxs-lookup"><span data-stu-id="36d04-122">Hull</span></span> | <span data-ttu-id="36d04-123">網域</span><span class="sxs-lookup"><span data-stu-id="36d04-123">Domain</span></span> | <span data-ttu-id="36d04-124">幾何</span><span class="sxs-lookup"><span data-stu-id="36d04-124">Geometry</span></span> | <span data-ttu-id="36d04-125">像素</span><span class="sxs-lookup"><span data-stu-id="36d04-125">Pixel</span></span> | <span data-ttu-id="36d04-126">計算</span><span class="sxs-lookup"><span data-stu-id="36d04-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="36d04-127">x</span><span class="sxs-lookup"><span data-stu-id="36d04-127">x</span></span>    | <span data-ttu-id="36d04-128">x</span><span class="sxs-lookup"><span data-stu-id="36d04-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="36d04-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36d04-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d04-130">語意</span><span class="sxs-lookup"><span data-stu-id="36d04-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="36d04-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="36d04-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





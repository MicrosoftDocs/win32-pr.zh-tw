---
title: SV_DomainLocation
description: 定義要評估之目前網域點的輪廓上的位置。
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c5195881df438c94cdaed7de8484d0df65e4d54
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373389"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="69ec1-104">SV \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="69ec1-104">SV\_DomainLocation</span></span>

<span data-ttu-id="69ec1-105">定義要評估之目前網域點的輪廓上的位置。</span><span class="sxs-lookup"><span data-stu-id="69ec1-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="69ec1-106">類型</span><span class="sxs-lookup"><span data-stu-id="69ec1-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="69ec1-107">類型</span><span class="sxs-lookup"><span data-stu-id="69ec1-107">Type</span></span>   | <span data-ttu-id="69ec1-108">輸入拓撲</span><span class="sxs-lookup"><span data-stu-id="69ec1-108">Input Topology</span></span> |
| <span data-ttu-id="69ec1-109">float2</span><span class="sxs-lookup"><span data-stu-id="69ec1-109">float2</span></span> | <span data-ttu-id="69ec1-110">四個修補程式</span><span class="sxs-lookup"><span data-stu-id="69ec1-110">quad patch</span></span>     |
| <span data-ttu-id="69ec1-111">float3</span><span class="sxs-lookup"><span data-stu-id="69ec1-111">float3</span></span> | <span data-ttu-id="69ec1-112">三個修補程式</span><span class="sxs-lookup"><span data-stu-id="69ec1-112">tri patch</span></span>      |
| <span data-ttu-id="69ec1-113">float2</span><span class="sxs-lookup"><span data-stu-id="69ec1-113">float2</span></span> | <span data-ttu-id="69ec1-114">等值 線</span><span class="sxs-lookup"><span data-stu-id="69ec1-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="69ec1-115">備註</span><span class="sxs-lookup"><span data-stu-id="69ec1-115">Remarks</span></span>

<span data-ttu-id="69ec1-116">此為必要的系統值。</span><span class="sxs-lookup"><span data-stu-id="69ec1-116">This system value is required.</span></span>

<span data-ttu-id="69ec1-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="69ec1-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="69ec1-118">頂點</span><span class="sxs-lookup"><span data-stu-id="69ec1-118">Vertex</span></span> | <span data-ttu-id="69ec1-119">船體</span><span class="sxs-lookup"><span data-stu-id="69ec1-119">Hull</span></span> | <span data-ttu-id="69ec1-120">網域</span><span class="sxs-lookup"><span data-stu-id="69ec1-120">Domain</span></span> | <span data-ttu-id="69ec1-121">幾何</span><span class="sxs-lookup"><span data-stu-id="69ec1-121">Geometry</span></span> | <span data-ttu-id="69ec1-122">像素</span><span class="sxs-lookup"><span data-stu-id="69ec1-122">Pixel</span></span> | <span data-ttu-id="69ec1-123">計算</span><span class="sxs-lookup"><span data-stu-id="69ec1-123">Compute</span></span> |
|        |      | <span data-ttu-id="69ec1-124">x</span><span class="sxs-lookup"><span data-stu-id="69ec1-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="69ec1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69ec1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ec1-126">語意</span><span class="sxs-lookup"><span data-stu-id="69ec1-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="69ec1-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="69ec1-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: cb9265734663881981f1626db6e23c6b7dd9415a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996505"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="86609-104">SV \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="86609-104">SV\_DomainLocation</span></span>

<span data-ttu-id="86609-105">定義要評估之目前網域點的輪廓上的位置。</span><span class="sxs-lookup"><span data-stu-id="86609-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="86609-106">類型</span><span class="sxs-lookup"><span data-stu-id="86609-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="86609-107">類型</span><span class="sxs-lookup"><span data-stu-id="86609-107">Type</span></span>   | <span data-ttu-id="86609-108">輸入拓撲</span><span class="sxs-lookup"><span data-stu-id="86609-108">Input Topology</span></span> |
| <span data-ttu-id="86609-109">float2</span><span class="sxs-lookup"><span data-stu-id="86609-109">float2</span></span> | <span data-ttu-id="86609-110">四個修補程式</span><span class="sxs-lookup"><span data-stu-id="86609-110">quad patch</span></span>     |
| <span data-ttu-id="86609-111">float3</span><span class="sxs-lookup"><span data-stu-id="86609-111">float3</span></span> | <span data-ttu-id="86609-112">三個修補程式</span><span class="sxs-lookup"><span data-stu-id="86609-112">tri patch</span></span>      |
| <span data-ttu-id="86609-113">float2</span><span class="sxs-lookup"><span data-stu-id="86609-113">float2</span></span> | <span data-ttu-id="86609-114">等值 線</span><span class="sxs-lookup"><span data-stu-id="86609-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="86609-115">備註</span><span class="sxs-lookup"><span data-stu-id="86609-115">Remarks</span></span>

<span data-ttu-id="86609-116">此為必要的系統值。</span><span class="sxs-lookup"><span data-stu-id="86609-116">This system value is required.</span></span>

<span data-ttu-id="86609-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="86609-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="86609-118">頂點</span><span class="sxs-lookup"><span data-stu-id="86609-118">Vertex</span></span> | <span data-ttu-id="86609-119">船體</span><span class="sxs-lookup"><span data-stu-id="86609-119">Hull</span></span> | <span data-ttu-id="86609-120">網域</span><span class="sxs-lookup"><span data-stu-id="86609-120">Domain</span></span> | <span data-ttu-id="86609-121">幾何</span><span class="sxs-lookup"><span data-stu-id="86609-121">Geometry</span></span> | <span data-ttu-id="86609-122">像素</span><span class="sxs-lookup"><span data-stu-id="86609-122">Pixel</span></span> | <span data-ttu-id="86609-123">計算</span><span class="sxs-lookup"><span data-stu-id="86609-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="86609-124">x</span><span class="sxs-lookup"><span data-stu-id="86609-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="86609-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86609-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86609-126">語意</span><span class="sxs-lookup"><span data-stu-id="86609-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="86609-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="86609-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





---
title: Texture2DMS：： GetSamplePosition 函數
description: 傳回所提供之範例索引的範例位置。
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- GetSamplePosition 函式 HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508272"
---
# <a name="texture2dmsgetsampleposition-function"></a><span data-ttu-id="3010c-104">Texture2DMS：： GetSamplePosition 函數</span><span class="sxs-lookup"><span data-stu-id="3010c-104">Texture2DMS::GetSamplePosition function</span></span>

<span data-ttu-id="3010c-105">傳回所提供之範例索引的範例位置。</span><span class="sxs-lookup"><span data-stu-id="3010c-105">Returns the sample position for the sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="3010c-106">語法</span><span class="sxs-lookup"><span data-stu-id="3010c-106">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="3010c-107">參數</span><span class="sxs-lookup"><span data-stu-id="3010c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3010c-108">*sampleindex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3010c-108">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3010c-109">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3010c-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3010c-110">範例位置以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="3010c-110">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3010c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3010c-111">Return value</span></span>

<span data-ttu-id="3010c-112">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="3010c-112">Type: **float2**</span></span>

<span data-ttu-id="3010c-113">範例位置。</span><span class="sxs-lookup"><span data-stu-id="3010c-113">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="3010c-114">備註</span><span class="sxs-lookup"><span data-stu-id="3010c-114">Remarks</span></span>

<span data-ttu-id="3010c-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="3010c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3010c-116">頂點</span><span class="sxs-lookup"><span data-stu-id="3010c-116">Vertex</span></span> | <span data-ttu-id="3010c-117">船體</span><span class="sxs-lookup"><span data-stu-id="3010c-117">Hull</span></span> | <span data-ttu-id="3010c-118">網域</span><span class="sxs-lookup"><span data-stu-id="3010c-118">Domain</span></span> | <span data-ttu-id="3010c-119">幾何</span><span class="sxs-lookup"><span data-stu-id="3010c-119">Geometry</span></span> | <span data-ttu-id="3010c-120">像素</span><span class="sxs-lookup"><span data-stu-id="3010c-120">Pixel</span></span> | <span data-ttu-id="3010c-121">計算</span><span class="sxs-lookup"><span data-stu-id="3010c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3010c-122">x</span><span class="sxs-lookup"><span data-stu-id="3010c-122">x</span></span>      | <span data-ttu-id="3010c-123">x</span><span class="sxs-lookup"><span data-stu-id="3010c-123">x</span></span>    | <span data-ttu-id="3010c-124">x</span><span class="sxs-lookup"><span data-stu-id="3010c-124">x</span></span>      | <span data-ttu-id="3010c-125">x</span><span class="sxs-lookup"><span data-stu-id="3010c-125">x</span></span>        | <span data-ttu-id="3010c-126">x</span><span class="sxs-lookup"><span data-stu-id="3010c-126">x</span></span>     | <span data-ttu-id="3010c-127">x</span><span class="sxs-lookup"><span data-stu-id="3010c-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3010c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3010c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3010c-129">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="3010c-129">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="3010c-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3010c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

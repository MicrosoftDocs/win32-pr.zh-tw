---
title: Texture2DMSArray：： GetSamplePosition 函數
description: 取得指定之範例的位置。 |Texture2DMSArray：： GetSamplePosition 函數
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196124"
---
# <a name="texture2dmsarraygetsampleposition-function"></a><span data-ttu-id="c1192-105">Texture2DMSArray：： GetSamplePosition 函數</span><span class="sxs-lookup"><span data-stu-id="c1192-105">Texture2DMSArray::GetSamplePosition function</span></span>

<span data-ttu-id="c1192-106">取得指定之範例的位置。</span><span class="sxs-lookup"><span data-stu-id="c1192-106">Gets the position of the specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1192-107">語法</span><span class="sxs-lookup"><span data-stu-id="c1192-107">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="c1192-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1192-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1192-109">*sampleindex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1192-109">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1192-110">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c1192-110">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c1192-111">範例位置以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="c1192-111">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1192-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1192-112">Return value</span></span>

<span data-ttu-id="c1192-113">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="c1192-113">Type: **float2**</span></span>

<span data-ttu-id="c1192-114">範例位置。</span><span class="sxs-lookup"><span data-stu-id="c1192-114">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1192-115">備註</span><span class="sxs-lookup"><span data-stu-id="c1192-115">Remarks</span></span>

<span data-ttu-id="c1192-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c1192-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c1192-117">頂點</span><span class="sxs-lookup"><span data-stu-id="c1192-117">Vertex</span></span> | <span data-ttu-id="c1192-118">船體</span><span class="sxs-lookup"><span data-stu-id="c1192-118">Hull</span></span> | <span data-ttu-id="c1192-119">網域</span><span class="sxs-lookup"><span data-stu-id="c1192-119">Domain</span></span> | <span data-ttu-id="c1192-120">幾何</span><span class="sxs-lookup"><span data-stu-id="c1192-120">Geometry</span></span> | <span data-ttu-id="c1192-121">像素</span><span class="sxs-lookup"><span data-stu-id="c1192-121">Pixel</span></span> | <span data-ttu-id="c1192-122">計算</span><span class="sxs-lookup"><span data-stu-id="c1192-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c1192-123">x</span><span class="sxs-lookup"><span data-stu-id="c1192-123">x</span></span>      | <span data-ttu-id="c1192-124">x</span><span class="sxs-lookup"><span data-stu-id="c1192-124">x</span></span>    | <span data-ttu-id="c1192-125">x</span><span class="sxs-lookup"><span data-stu-id="c1192-125">x</span></span>      | <span data-ttu-id="c1192-126">x</span><span class="sxs-lookup"><span data-stu-id="c1192-126">x</span></span>        | <span data-ttu-id="c1192-127">x</span><span class="sxs-lookup"><span data-stu-id="c1192-127">x</span></span>     | <span data-ttu-id="c1192-128">x</span><span class="sxs-lookup"><span data-stu-id="c1192-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c1192-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1192-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1192-130">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c1192-130">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="c1192-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c1192-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

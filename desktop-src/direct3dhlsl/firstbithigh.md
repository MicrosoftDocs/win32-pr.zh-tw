---
title: firstbithigh 函式
description: 取得第一個集合位從最高順序位開始，每個元件往下工作的位置。
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- firstbithigh 函式 HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375688"
---
# <a name="firstbithigh-function"></a><span data-ttu-id="f4dad-104">firstbithigh 函式</span><span class="sxs-lookup"><span data-stu-id="f4dad-104">firstbithigh function</span></span>

<span data-ttu-id="f4dad-105">取得第一個集合位從最高順序位開始，每個元件往下工作的位置。</span><span class="sxs-lookup"><span data-stu-id="f4dad-105">Gets the location of the first set bit starting from the highest order bit and working downward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4dad-106">語法</span><span class="sxs-lookup"><span data-stu-id="f4dad-106">Syntax</span></span>

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="f4dad-107">參數</span><span class="sxs-lookup"><span data-stu-id="f4dad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4dad-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4dad-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4dad-109">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f4dad-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f4dad-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="f4dad-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4dad-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4dad-111">Return value</span></span>

<span data-ttu-id="f4dad-112">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f4dad-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f4dad-113">第一個設定位的位置。</span><span class="sxs-lookup"><span data-stu-id="f4dad-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4dad-114">備註</span><span class="sxs-lookup"><span data-stu-id="f4dad-114">Remarks</span></span>

<span data-ttu-id="f4dad-115">若為帶正負號的整數，負數的第一個有效位為零。</span><span class="sxs-lookup"><span data-stu-id="f4dad-115">For a signed integer, the first significant bit is zero for a negative number.</span></span>

<span data-ttu-id="f4dad-116">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="f4dad-116">The following overloaded versions are also available:</span></span>

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="f4dad-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4dad-117">Minimum Shader Model</span></span>

<span data-ttu-id="f4dad-118">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="f4dad-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f4dad-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4dad-119">Shader Model</span></span>                                                                | <span data-ttu-id="f4dad-120">支援</span><span class="sxs-lookup"><span data-stu-id="f4dad-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f4dad-121">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4dad-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f4dad-122">是</span><span class="sxs-lookup"><span data-stu-id="f4dad-122">yes</span></span>       |



 

<span data-ttu-id="f4dad-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="f4dad-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f4dad-124">頂點</span><span class="sxs-lookup"><span data-stu-id="f4dad-124">Vertex</span></span> | <span data-ttu-id="f4dad-125">船體</span><span class="sxs-lookup"><span data-stu-id="f4dad-125">Hull</span></span> | <span data-ttu-id="f4dad-126">網域</span><span class="sxs-lookup"><span data-stu-id="f4dad-126">Domain</span></span> | <span data-ttu-id="f4dad-127">幾何</span><span class="sxs-lookup"><span data-stu-id="f4dad-127">Geometry</span></span> | <span data-ttu-id="f4dad-128">像素</span><span class="sxs-lookup"><span data-stu-id="f4dad-128">Pixel</span></span> | <span data-ttu-id="f4dad-129">計算</span><span class="sxs-lookup"><span data-stu-id="f4dad-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f4dad-130">x</span><span class="sxs-lookup"><span data-stu-id="f4dad-130">x</span></span>      | <span data-ttu-id="f4dad-131">x</span><span class="sxs-lookup"><span data-stu-id="f4dad-131">x</span></span>    | <span data-ttu-id="f4dad-132">x</span><span class="sxs-lookup"><span data-stu-id="f4dad-132">x</span></span>      | <span data-ttu-id="f4dad-133">x</span><span class="sxs-lookup"><span data-stu-id="f4dad-133">x</span></span>        | <span data-ttu-id="f4dad-134">x</span><span class="sxs-lookup"><span data-stu-id="f4dad-134">x</span></span>     | <span data-ttu-id="f4dad-135">x</span><span class="sxs-lookup"><span data-stu-id="f4dad-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f4dad-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4dad-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4dad-137">內建函式</span><span class="sxs-lookup"><span data-stu-id="f4dad-137">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f4dad-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f4dad-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
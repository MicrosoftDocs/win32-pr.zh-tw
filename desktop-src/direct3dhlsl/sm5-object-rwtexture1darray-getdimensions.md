---
title: RWTexture1DArray：： GetDimensions 函數
description: 傳回資源的維度。 |RWTexture1DArray：： GetDimensions 函數
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196018"
---
# <a name="rwtexture1darraygetdimensions-function"></a><span data-ttu-id="6de7a-105">RWTexture1DArray：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="6de7a-105">RWTexture1DArray::GetDimensions function</span></span>

<span data-ttu-id="6de7a-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="6de7a-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de7a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6de7a-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="6de7a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6de7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de7a-109">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6de7a-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6de7a-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6de7a-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6de7a-111">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="6de7a-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="6de7a-112">*元素* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6de7a-112">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6de7a-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6de7a-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6de7a-114">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="6de7a-114">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de7a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6de7a-115">Return value</span></span>

<span data-ttu-id="6de7a-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6de7a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6de7a-117">備註</span><span class="sxs-lookup"><span data-stu-id="6de7a-117">Remarks</span></span>

<span data-ttu-id="6de7a-118">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="6de7a-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="6de7a-119">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="6de7a-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6de7a-120">頂點</span><span class="sxs-lookup"><span data-stu-id="6de7a-120">Vertex</span></span> | <span data-ttu-id="6de7a-121">船體</span><span class="sxs-lookup"><span data-stu-id="6de7a-121">Hull</span></span> | <span data-ttu-id="6de7a-122">網域</span><span class="sxs-lookup"><span data-stu-id="6de7a-122">Domain</span></span> | <span data-ttu-id="6de7a-123">幾何</span><span class="sxs-lookup"><span data-stu-id="6de7a-123">Geometry</span></span> | <span data-ttu-id="6de7a-124">像素</span><span class="sxs-lookup"><span data-stu-id="6de7a-124">Pixel</span></span> | <span data-ttu-id="6de7a-125">計算</span><span class="sxs-lookup"><span data-stu-id="6de7a-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6de7a-126">x</span><span class="sxs-lookup"><span data-stu-id="6de7a-126">x</span></span>     | <span data-ttu-id="6de7a-127">x</span><span class="sxs-lookup"><span data-stu-id="6de7a-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6de7a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6de7a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de7a-129">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="6de7a-129">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="6de7a-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6de7a-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

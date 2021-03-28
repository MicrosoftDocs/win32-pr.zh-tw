---
title: Texture2DMS：： Load (int，int) 函數
description: 取得一個值。 |Texture2DMS：： Load (int，int) 函數
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Load 函數 DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974168"
---
# <a name="texture2dmsloadintint-function"></a><span data-ttu-id="4702f-105">Texture2DMS：： Load (int，int) 函數</span><span class="sxs-lookup"><span data-stu-id="4702f-105">Texture2DMS::Load(int,int) function</span></span>

<span data-ttu-id="4702f-106">取得一個值。</span><span class="sxs-lookup"><span data-stu-id="4702f-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4702f-107">語法</span><span class="sxs-lookup"><span data-stu-id="4702f-107">Syntax</span></span>

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="4702f-108">參數</span><span class="sxs-lookup"><span data-stu-id="4702f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4702f-109">*coord* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4702f-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4702f-110">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="4702f-110">Type: **int2**</span></span>

<span data-ttu-id="4702f-111">輸入位置。</span><span class="sxs-lookup"><span data-stu-id="4702f-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="4702f-112">*sampleindex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4702f-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4702f-113">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4702f-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4702f-114">範例索引。</span><span class="sxs-lookup"><span data-stu-id="4702f-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4702f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4702f-115">Return value</span></span>

<span data-ttu-id="4702f-116">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="4702f-116">Type: **T**</span></span>

<span data-ttu-id="4702f-117">一個值，其類型符合紋理範本類型。</span><span class="sxs-lookup"><span data-stu-id="4702f-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4702f-118">備註</span><span class="sxs-lookup"><span data-stu-id="4702f-118">Remarks</span></span>

<span data-ttu-id="4702f-119">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="4702f-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="4702f-120">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="4702f-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4702f-121">頂點</span><span class="sxs-lookup"><span data-stu-id="4702f-121">Vertex</span></span> | <span data-ttu-id="4702f-122">船體</span><span class="sxs-lookup"><span data-stu-id="4702f-122">Hull</span></span> | <span data-ttu-id="4702f-123">網域</span><span class="sxs-lookup"><span data-stu-id="4702f-123">Domain</span></span> | <span data-ttu-id="4702f-124">幾何</span><span class="sxs-lookup"><span data-stu-id="4702f-124">Geometry</span></span> | <span data-ttu-id="4702f-125">像素</span><span class="sxs-lookup"><span data-stu-id="4702f-125">Pixel</span></span> | <span data-ttu-id="4702f-126">計算</span><span class="sxs-lookup"><span data-stu-id="4702f-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4702f-127">x</span><span class="sxs-lookup"><span data-stu-id="4702f-127">x</span></span>     | <span data-ttu-id="4702f-128">x</span><span class="sxs-lookup"><span data-stu-id="4702f-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4702f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4702f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4702f-130">載入方法</span><span class="sxs-lookup"><span data-stu-id="4702f-130">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="4702f-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4702f-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

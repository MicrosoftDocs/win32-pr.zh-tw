---
title: ConsumeStructuredBuffer：：取用函式
description: 從緩衝區的結尾移除值。
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- 使用函式 HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104022721"
---
# <a name="consume-function"></a><span data-ttu-id="f0e2b-104">取用函式</span><span class="sxs-lookup"><span data-stu-id="f0e2b-104">Consume function</span></span>

<span data-ttu-id="f0e2b-105">從緩衝區的結尾移除值。</span><span class="sxs-lookup"><span data-stu-id="f0e2b-105">Removes a value from the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e2b-106">語法</span><span class="sxs-lookup"><span data-stu-id="f0e2b-106">Syntax</span></span>

``` syntax
T Consume(void);
```

## <a name="parameters"></a><span data-ttu-id="f0e2b-107">參數</span><span class="sxs-lookup"><span data-stu-id="f0e2b-107">Parameters</span></span>

<span data-ttu-id="f0e2b-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f0e2b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0e2b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0e2b-109">Return value</span></span>

<span data-ttu-id="f0e2b-110">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="f0e2b-110">Type: **T**</span></span>

<span data-ttu-id="f0e2b-111"> (移除的值可以是結構) 。</span><span class="sxs-lookup"><span data-stu-id="f0e2b-111">The value removed (can be a structure).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0e2b-112">備註</span><span class="sxs-lookup"><span data-stu-id="f0e2b-112">Remarks</span></span>

<span data-ttu-id="f0e2b-113">T 可以是任何資料類型，包括結構。</span><span class="sxs-lookup"><span data-stu-id="f0e2b-113">T can be any data type including a structure.</span></span>

<span data-ttu-id="f0e2b-114">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="f0e2b-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f0e2b-115">頂點</span><span class="sxs-lookup"><span data-stu-id="f0e2b-115">Vertex</span></span> | <span data-ttu-id="f0e2b-116">船體</span><span class="sxs-lookup"><span data-stu-id="f0e2b-116">Hull</span></span> | <span data-ttu-id="f0e2b-117">網域</span><span class="sxs-lookup"><span data-stu-id="f0e2b-117">Domain</span></span> | <span data-ttu-id="f0e2b-118">幾何</span><span class="sxs-lookup"><span data-stu-id="f0e2b-118">Geometry</span></span> | <span data-ttu-id="f0e2b-119">像素</span><span class="sxs-lookup"><span data-stu-id="f0e2b-119">Pixel</span></span> | <span data-ttu-id="f0e2b-120">計算</span><span class="sxs-lookup"><span data-stu-id="f0e2b-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f0e2b-121">x</span><span class="sxs-lookup"><span data-stu-id="f0e2b-121">x</span></span>      | <span data-ttu-id="f0e2b-122">x</span><span class="sxs-lookup"><span data-stu-id="f0e2b-122">x</span></span>    | <span data-ttu-id="f0e2b-123">x</span><span class="sxs-lookup"><span data-stu-id="f0e2b-123">x</span></span>      | <span data-ttu-id="f0e2b-124">x</span><span class="sxs-lookup"><span data-stu-id="f0e2b-124">x</span></span>        | <span data-ttu-id="f0e2b-125">x</span><span class="sxs-lookup"><span data-stu-id="f0e2b-125">x</span></span>     | <span data-ttu-id="f0e2b-126">x</span><span class="sxs-lookup"><span data-stu-id="f0e2b-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f0e2b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0e2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e2b-128">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="f0e2b-128">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="f0e2b-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f0e2b-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





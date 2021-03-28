---
title: AllMemoryBarrier 函式
description: 封鎖群組中所有線程的執行，直到所有記憶體存取都完成為止。
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- AllMemoryBarrier 函式 HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373365"
---
# <a name="allmemorybarrier-function"></a><span data-ttu-id="91198-104">AllMemoryBarrier 函式</span><span class="sxs-lookup"><span data-stu-id="91198-104">AllMemoryBarrier function</span></span>

<span data-ttu-id="91198-105">封鎖群組中所有線程的執行，直到所有記憶體存取都完成為止。</span><span class="sxs-lookup"><span data-stu-id="91198-105">Blocks execution of all threads in a group until all memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="91198-106">語法</span><span class="sxs-lookup"><span data-stu-id="91198-106">Syntax</span></span>

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="91198-107">參數</span><span class="sxs-lookup"><span data-stu-id="91198-107">Parameters</span></span>

<span data-ttu-id="91198-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="91198-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91198-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="91198-109">Return value</span></span>

<span data-ttu-id="91198-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="91198-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91198-111">備註</span><span class="sxs-lookup"><span data-stu-id="91198-111">Remarks</span></span>

<span data-ttu-id="91198-112">記憶體關卡可保證未完成的記憶體作業已完成。</span><span class="sxs-lookup"><span data-stu-id="91198-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="91198-113">執行緒會在 GroupSync 關卡進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="91198-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="91198-114">如果記憶體作業正在進行中，這可能會導致執行緒或執行緒停止運作。</span><span class="sxs-lookup"><span data-stu-id="91198-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="91198-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="91198-115">Minimum Shader Model</span></span>

<span data-ttu-id="91198-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="91198-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="91198-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="91198-117">Shader Model</span></span>                                                                | <span data-ttu-id="91198-118">支援</span><span class="sxs-lookup"><span data-stu-id="91198-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="91198-119">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="91198-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="91198-120">是</span><span class="sxs-lookup"><span data-stu-id="91198-120">yes</span></span>       |



 

<span data-ttu-id="91198-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="91198-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="91198-122">頂點</span><span class="sxs-lookup"><span data-stu-id="91198-122">Vertex</span></span> | <span data-ttu-id="91198-123">船體</span><span class="sxs-lookup"><span data-stu-id="91198-123">Hull</span></span> | <span data-ttu-id="91198-124">網域</span><span class="sxs-lookup"><span data-stu-id="91198-124">Domain</span></span> | <span data-ttu-id="91198-125">幾何</span><span class="sxs-lookup"><span data-stu-id="91198-125">Geometry</span></span> | <span data-ttu-id="91198-126">像素</span><span class="sxs-lookup"><span data-stu-id="91198-126">Pixel</span></span> | <span data-ttu-id="91198-127">計算</span><span class="sxs-lookup"><span data-stu-id="91198-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="91198-128">x</span><span class="sxs-lookup"><span data-stu-id="91198-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="91198-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91198-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91198-130">內建函式</span><span class="sxs-lookup"><span data-stu-id="91198-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="91198-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="91198-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





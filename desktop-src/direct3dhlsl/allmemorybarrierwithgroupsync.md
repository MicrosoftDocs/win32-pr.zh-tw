---
title: AllMemoryBarrierWithGroupSync 函式
description: 封鎖群組中所有線程的執行，直到所有記憶體存取都已完成，且群組中的所有線程都已達到此呼叫。
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- AllMemoryBarrierWithGroupSync 函式 HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022628"
---
# <a name="allmemorybarrierwithgroupsync-function"></a><span data-ttu-id="ed3e0-104">AllMemoryBarrierWithGroupSync 函式</span><span class="sxs-lookup"><span data-stu-id="ed3e0-104">AllMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="ed3e0-105">封鎖群組中所有線程的執行，直到所有記憶體存取都已完成，且群組中的所有線程都已達到此呼叫。</span><span class="sxs-lookup"><span data-stu-id="ed3e0-105">Blocks execution of all threads in a group until all memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3e0-106">語法</span><span class="sxs-lookup"><span data-stu-id="ed3e0-106">Syntax</span></span>

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="ed3e0-107">參數</span><span class="sxs-lookup"><span data-stu-id="ed3e0-107">Parameters</span></span>

<span data-ttu-id="ed3e0-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="ed3e0-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed3e0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed3e0-109">Return value</span></span>

<span data-ttu-id="ed3e0-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ed3e0-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed3e0-111">備註</span><span class="sxs-lookup"><span data-stu-id="ed3e0-111">Remarks</span></span>

<span data-ttu-id="ed3e0-112">記憶體關卡可保證未完成的記憶體作業已完成。</span><span class="sxs-lookup"><span data-stu-id="ed3e0-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="ed3e0-113">執行緒會在 GroupSync 關卡進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ed3e0-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="ed3e0-114">如果記憶體作業正在進行中，這可能會導致執行緒或執行緒停止運作。</span><span class="sxs-lookup"><span data-stu-id="ed3e0-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="ed3e0-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ed3e0-115">Minimum Shader Model</span></span>

<span data-ttu-id="ed3e0-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ed3e0-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ed3e0-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ed3e0-117">Shader Model</span></span>                                                                | <span data-ttu-id="ed3e0-118">支援</span><span class="sxs-lookup"><span data-stu-id="ed3e0-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ed3e0-119">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ed3e0-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ed3e0-120">是</span><span class="sxs-lookup"><span data-stu-id="ed3e0-120">yes</span></span>       |



 

<span data-ttu-id="ed3e0-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ed3e0-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ed3e0-122">頂點</span><span class="sxs-lookup"><span data-stu-id="ed3e0-122">Vertex</span></span> | <span data-ttu-id="ed3e0-123">船體</span><span class="sxs-lookup"><span data-stu-id="ed3e0-123">Hull</span></span> | <span data-ttu-id="ed3e0-124">網域</span><span class="sxs-lookup"><span data-stu-id="ed3e0-124">Domain</span></span> | <span data-ttu-id="ed3e0-125">幾何</span><span class="sxs-lookup"><span data-stu-id="ed3e0-125">Geometry</span></span> | <span data-ttu-id="ed3e0-126">像素</span><span class="sxs-lookup"><span data-stu-id="ed3e0-126">Pixel</span></span> | <span data-ttu-id="ed3e0-127">計算</span><span class="sxs-lookup"><span data-stu-id="ed3e0-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="ed3e0-128">x</span><span class="sxs-lookup"><span data-stu-id="ed3e0-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ed3e0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed3e0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3e0-130">內建函式</span><span class="sxs-lookup"><span data-stu-id="ed3e0-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ed3e0-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ed3e0-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





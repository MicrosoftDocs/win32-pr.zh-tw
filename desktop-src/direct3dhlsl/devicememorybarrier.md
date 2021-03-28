---
title: DeviceMemoryBarrier 函式
description: 封鎖群組中所有線程的執行，直到所有裝置記憶體存取都完成為止。
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- DeviceMemoryBarrier 函式 HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372741"
---
# <a name="devicememorybarrier-function"></a><span data-ttu-id="f2430-104">DeviceMemoryBarrier 函式</span><span class="sxs-lookup"><span data-stu-id="f2430-104">DeviceMemoryBarrier function</span></span>

<span data-ttu-id="f2430-105">封鎖群組中所有線程的執行，直到所有裝置記憶體存取都完成為止。</span><span class="sxs-lookup"><span data-stu-id="f2430-105">Blocks execution of all threads in a group until all device memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2430-106">語法</span><span class="sxs-lookup"><span data-stu-id="f2430-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="f2430-107">參數</span><span class="sxs-lookup"><span data-stu-id="f2430-107">Parameters</span></span>

<span data-ttu-id="f2430-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f2430-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2430-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2430-109">Return value</span></span>

<span data-ttu-id="f2430-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f2430-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2430-111">備註</span><span class="sxs-lookup"><span data-stu-id="f2430-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="f2430-112">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2430-112">Minimum Shader Model</span></span>

<span data-ttu-id="f2430-113">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="f2430-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f2430-114">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2430-114">Shader Model</span></span>                                                                | <span data-ttu-id="f2430-115">支援</span><span class="sxs-lookup"><span data-stu-id="f2430-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f2430-116">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2430-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f2430-117">是</span><span class="sxs-lookup"><span data-stu-id="f2430-117">yes</span></span>       |



 

<span data-ttu-id="f2430-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="f2430-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f2430-119">頂點</span><span class="sxs-lookup"><span data-stu-id="f2430-119">Vertex</span></span> | <span data-ttu-id="f2430-120">船體</span><span class="sxs-lookup"><span data-stu-id="f2430-120">Hull</span></span> | <span data-ttu-id="f2430-121">網域</span><span class="sxs-lookup"><span data-stu-id="f2430-121">Domain</span></span> | <span data-ttu-id="f2430-122">幾何</span><span class="sxs-lookup"><span data-stu-id="f2430-122">Geometry</span></span> | <span data-ttu-id="f2430-123">像素</span><span class="sxs-lookup"><span data-stu-id="f2430-123">Pixel</span></span> | <span data-ttu-id="f2430-124">計算</span><span class="sxs-lookup"><span data-stu-id="f2430-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f2430-125">x</span><span class="sxs-lookup"><span data-stu-id="f2430-125">x</span></span>     | <span data-ttu-id="f2430-126">x</span><span class="sxs-lookup"><span data-stu-id="f2430-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f2430-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2430-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2430-128">內建函式</span><span class="sxs-lookup"><span data-stu-id="f2430-128">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f2430-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f2430-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





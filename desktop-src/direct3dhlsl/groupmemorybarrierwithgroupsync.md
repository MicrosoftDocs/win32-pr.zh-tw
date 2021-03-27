---
title: GroupMemoryBarrierWithGroupSync 函式
description: 封鎖群組中所有線程的執行，直到完成所有群組共用存取，而且群組中的所有線程都已達到此呼叫。
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- GroupMemoryBarrierWithGroupSync 函式 HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104971465"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a><span data-ttu-id="2afb3-104">GroupMemoryBarrierWithGroupSync 函式</span><span class="sxs-lookup"><span data-stu-id="2afb3-104">GroupMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="2afb3-105">封鎖群組中所有線程的執行，直到完成所有群組共用存取，而且群組中的所有線程都已達到此呼叫。</span><span class="sxs-lookup"><span data-stu-id="2afb3-105">Blocks execution of all threads in a group until all group shared accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afb3-106">語法</span><span class="sxs-lookup"><span data-stu-id="2afb3-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="2afb3-107">參數</span><span class="sxs-lookup"><span data-stu-id="2afb3-107">Parameters</span></span>

<span data-ttu-id="2afb3-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="2afb3-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2afb3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2afb3-109">Return value</span></span>

<span data-ttu-id="2afb3-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2afb3-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2afb3-111">備註</span><span class="sxs-lookup"><span data-stu-id="2afb3-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2afb3-112">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2afb3-112">Minimum Shader Model</span></span>

<span data-ttu-id="2afb3-113">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2afb3-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2afb3-114">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2afb3-114">Shader Model</span></span>                                                                | <span data-ttu-id="2afb3-115">支援</span><span class="sxs-lookup"><span data-stu-id="2afb3-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2afb3-116">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="2afb3-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2afb3-117">是</span><span class="sxs-lookup"><span data-stu-id="2afb3-117">yes</span></span>       |



 

<span data-ttu-id="2afb3-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="2afb3-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2afb3-119">頂點</span><span class="sxs-lookup"><span data-stu-id="2afb3-119">Vertex</span></span> | <span data-ttu-id="2afb3-120">船體</span><span class="sxs-lookup"><span data-stu-id="2afb3-120">Hull</span></span> | <span data-ttu-id="2afb3-121">網域</span><span class="sxs-lookup"><span data-stu-id="2afb3-121">Domain</span></span> | <span data-ttu-id="2afb3-122">幾何</span><span class="sxs-lookup"><span data-stu-id="2afb3-122">Geometry</span></span> | <span data-ttu-id="2afb3-123">像素</span><span class="sxs-lookup"><span data-stu-id="2afb3-123">Pixel</span></span> | <span data-ttu-id="2afb3-124">計算</span><span class="sxs-lookup"><span data-stu-id="2afb3-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="2afb3-125">x</span><span class="sxs-lookup"><span data-stu-id="2afb3-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2afb3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2afb3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2afb3-127">內建函式</span><span class="sxs-lookup"><span data-stu-id="2afb3-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2afb3-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2afb3-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





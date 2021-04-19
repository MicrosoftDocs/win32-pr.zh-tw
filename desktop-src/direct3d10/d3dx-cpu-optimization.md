---
description: 指定目前針對 D3DX 優化的指令集。
ms.assetid: 5fc97028-4a9d-4bc7-9c90-236a70e570e1
title: 'D3DX_CPU_OPTIMIZATION 列舉 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_CPU_OPTIMIZATION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 208422604e79b3ef7a87b548e7d71eceedd9fb78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992704"
---
# <a name="d3dx_cpu_optimization-enumeration"></a><span data-ttu-id="df196-103">D3DX \_ CPU \_ 優化列舉</span><span class="sxs-lookup"><span data-stu-id="df196-103">D3DX\_CPU\_OPTIMIZATION enumeration</span></span>

<span data-ttu-id="df196-104">指定目前針對 D3DX 優化的指令集。</span><span class="sxs-lookup"><span data-stu-id="df196-104">Specifies the instruction set D3DX is currently optimized for.</span></span>

## <a name="syntax"></a><span data-ttu-id="df196-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df196-105">Syntax</span></span>


```C++
typedef enum _D3DX_CPU_OPTIMIZATION { 
  D3DX_NOT_OPTIMIZED    = 0,
  D3DX_3DNOW_OPTIMIZED  = 1,
  D3DX_SSE2_OPTIMIZED   = 2,
  D3DX_SSE_OPTIMIZED    = 3
} D3DX_CPU_OPTIMIZATION;
```



## <a name="constants"></a><span data-ttu-id="df196-106">常數</span><span class="sxs-lookup"><span data-stu-id="df196-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="df196-107"><span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX \_ 未 \_ 優化**</span><span class="sxs-lookup"><span data-stu-id="df196-107"><span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX\_NOT\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="df196-108">請勿優化。</span><span class="sxs-lookup"><span data-stu-id="df196-108">Do not optimize.</span></span>

</dd> <dt>

<span data-ttu-id="df196-109"><span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX \_ 3DNOW \_ 優化**</span><span class="sxs-lookup"><span data-stu-id="df196-109"><span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX\_3DNOW\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="df196-110">針對3DNow 進行優化！</span><span class="sxs-lookup"><span data-stu-id="df196-110">Optimize for a 3DNow!</span></span> <span data-ttu-id="df196-111">指令集。</span><span class="sxs-lookup"><span data-stu-id="df196-111">instruction set.</span></span>

</dd> <dt>

<span data-ttu-id="df196-112"><span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX \_ SSE2 \_ 優化**</span><span class="sxs-lookup"><span data-stu-id="df196-112"><span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX\_SSE2\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="df196-113">針對 SSE2 指令集進行優化。</span><span class="sxs-lookup"><span data-stu-id="df196-113">Optimize for an SSE2 instruction set.</span></span>

</dd> <dt>

<span data-ttu-id="df196-114"><span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX \_ 已 \_ 優化的 SSE**</span><span class="sxs-lookup"><span data-stu-id="df196-114"><span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX\_SSE\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="df196-115">針對 SSE 指令集優化。</span><span class="sxs-lookup"><span data-stu-id="df196-115">Optimize for an SSE instruction set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df196-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="df196-116">Requirements</span></span>



| <span data-ttu-id="df196-117">需求</span><span class="sxs-lookup"><span data-stu-id="df196-117">Requirement</span></span> | <span data-ttu-id="df196-118">值</span><span class="sxs-lookup"><span data-stu-id="df196-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df196-119">標頭</span><span class="sxs-lookup"><span data-stu-id="df196-119">Header</span></span><br/> | <dl> <span data-ttu-id="df196-120"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="df196-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df196-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df196-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df196-122">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="df196-122">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





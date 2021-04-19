---
description: 包含記憶體壓力報告的資料。
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: 'D3DMEMORYPRESSURE 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988597"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="e3420-103">D3DMEMORYPRESSURE 結構 (D3d9types .h) </span><span class="sxs-lookup"><span data-stu-id="e3420-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="e3420-104">包含記憶體壓力報告的資料。</span><span class="sxs-lookup"><span data-stu-id="e3420-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3420-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3420-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="e3420-106">成員</span><span class="sxs-lookup"><span data-stu-id="e3420-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3420-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="e3420-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="e3420-108">類型： **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3420-108">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3420-109">進程在查詢期間收回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e3420-109">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="e3420-110">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="e3420-110">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="e3420-111">類型： **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3420-111">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3420-112">因為慣用記憶體區段內的空間不足，所以放置在非最非最非最佳記憶體區段中的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="e3420-112">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="e3420-113">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="e3420-113">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="e3420-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3420-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3420-115">放在非最佳記憶體中之記憶體配置的整體效率。</span><span class="sxs-lookup"><span data-stu-id="e3420-115">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="e3420-116">此值以百分比表示。</span><span class="sxs-lookup"><span data-stu-id="e3420-116">The value is expressed as a percentage.</span></span> <span data-ttu-id="e3420-117">例如，值95表示放置在 nonpreferred 記憶體區段中的配置為95% 的效率。</span><span class="sxs-lookup"><span data-stu-id="e3420-117">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="e3420-118">此數位不應視為確切的度量。</span><span class="sxs-lookup"><span data-stu-id="e3420-118">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3420-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3420-119">Requirements</span></span>



| <span data-ttu-id="e3420-120">需求</span><span class="sxs-lookup"><span data-stu-id="e3420-120">Requirement</span></span> | <span data-ttu-id="e3420-121">值</span><span class="sxs-lookup"><span data-stu-id="e3420-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3420-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e3420-122">Header</span></span><br/> | <dl> <span data-ttu-id="e3420-123"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3420-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3420-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3420-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3420-125">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="e3420-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

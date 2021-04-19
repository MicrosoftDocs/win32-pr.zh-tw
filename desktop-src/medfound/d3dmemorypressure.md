---
description: 此結構包含記憶體壓力報告的資料。
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: 'Microsoft 媒體基礎的 D3DMEMORYPRESSURE 結構 (D3d9types) '
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
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106990511"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a><span data-ttu-id="efe11-103">Microsoft 媒體基礎的 D3DMEMORYPRESSURE 結構 (D3d9types) </span><span class="sxs-lookup"><span data-stu-id="efe11-103">D3DMEMORYPRESSURE structure (D3d9types.h) for Microsoft Media Foundation</span></span>

<span data-ttu-id="efe11-104">包含記憶體壓力報告的資料。</span><span class="sxs-lookup"><span data-stu-id="efe11-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe11-105">語法</span><span class="sxs-lookup"><span data-stu-id="efe11-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="efe11-106">成員</span><span class="sxs-lookup"><span data-stu-id="efe11-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="efe11-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="efe11-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="efe11-108">進程在查詢期間收回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="efe11-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="efe11-109">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="efe11-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="efe11-110">因為慣用記憶體區段內的空間不足，所以放置在非最非最非最佳記憶體區段中的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="efe11-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="efe11-111">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="efe11-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="efe11-112">放在非最佳記憶體中之記憶體配置的整體效率。</span><span class="sxs-lookup"><span data-stu-id="efe11-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="efe11-113">此值以百分比表示。</span><span class="sxs-lookup"><span data-stu-id="efe11-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="efe11-114">例如，值95表示放置在 nonpreferred 記憶體區段中的配置為95% 的效率。</span><span class="sxs-lookup"><span data-stu-id="efe11-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="efe11-115">此數位不應視為確切的度量。</span><span class="sxs-lookup"><span data-stu-id="efe11-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efe11-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="efe11-116">Requirements</span></span>



| <span data-ttu-id="efe11-117">需求</span><span class="sxs-lookup"><span data-stu-id="efe11-117">Requirement</span></span> | <span data-ttu-id="efe11-118">值</span><span class="sxs-lookup"><span data-stu-id="efe11-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe11-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="efe11-119">Minimum supported client</span></span> | <span data-ttu-id="efe11-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efe11-120">Windows 7 \[desktop apps only\]</span></span>                                                              |
| <span data-ttu-id="efe11-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="efe11-121">Minimum supported server</span></span> | <span data-ttu-id="efe11-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efe11-122">Windows Server 2008 R2 \[desktop apps only\]</span></span>                                                 |
| <span data-ttu-id="efe11-123">標頭</span><span class="sxs-lookup"><span data-stu-id="efe11-123">Header</span></span>                  | <span data-ttu-id="efe11-124">D3d9types (包含 D3d9) </span><span class="sxs-lookup"><span data-stu-id="efe11-124">D3d9types.h (include D3d9.h)</span></span> |



## <a name="see-also"></a><span data-ttu-id="efe11-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="efe11-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe11-126">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="efe11-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="efe11-127">記憶體壓力報告</span><span class="sxs-lookup"><span data-stu-id="efe11-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 





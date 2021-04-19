---
description: 驅動程式中處理資料的時間百分比。 當驅動程式正在等候其他資源時，這些統計資料可能有助於找出案例。
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: 'D3DDEVINFO_D3D9INTERFACETIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976695"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a><span data-ttu-id="6d997-104">D3DDEVINFO \_ D3D9INTERFACETIMINGS 結構</span><span class="sxs-lookup"><span data-stu-id="6d997-104">D3DDEVINFO\_D3D9INTERFACETIMINGS structure</span></span>

<span data-ttu-id="6d997-105">驅動程式中處理資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="6d997-105">Percent of time processing data in the driver.</span></span> <span data-ttu-id="6d997-106">當驅動程式正在等候其他資源時，這些統計資料可能有助於找出案例。</span><span class="sxs-lookup"><span data-stu-id="6d997-106">These statistics may help identify cases when the driver is waiting for other resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d997-107">語法</span><span class="sxs-lookup"><span data-stu-id="6d997-107">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a><span data-ttu-id="6d997-108">成員</span><span class="sxs-lookup"><span data-stu-id="6d997-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d997-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="6d997-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="6d997-110">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d997-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d997-111">驅動程式花費在等候 GPU 完成使用鎖定的資源 (且未指定) 的 [D3DLOCK \_ DONOTWAIT](d3dlock.md) 時，所花費的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="6d997-111">Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and [D3DLOCK\_DONOTWAIT](d3dlock.md) wasn't specified).</span></span>

</dd> <dt>

<span data-ttu-id="6d997-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span><span class="sxs-lookup"><span data-stu-id="6d997-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="6d997-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d997-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d997-114">驅動程式在驅動程式可以傳送更多之前，等候 GPU 完成處理某些命令所花費的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="6d997-114">Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more.</span></span> <span data-ttu-id="6d997-115">這表示驅動程式的空間不足，無法將命令傳送至 GPU。</span><span class="sxs-lookup"><span data-stu-id="6d997-115">This indicates the driver has run out of room to send commands to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="6d997-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span><span class="sxs-lookup"><span data-stu-id="6d997-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="6d997-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d997-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d997-118">驅動程式花費在等候 GPU 延遲降至小於三個轉譯畫面的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="6d997-118">Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames.</span></span>

<span data-ttu-id="6d997-119">如果應用程式是 GPU 受限的，則驅動程式必須在 GPU 于三個框架內進行時，才會停止 CPU。</span><span class="sxs-lookup"><span data-stu-id="6d997-119">If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames.</span></span> <span data-ttu-id="6d997-120">這可防止應用程式將許多秒鐘的轉譯呼叫排入佇列，這可能會大幅增加使用者輸入新資料的時間，以及使用者看到該輸入的結果之間的延遲。</span><span class="sxs-lookup"><span data-stu-id="6d997-120">This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input.</span></span> <span data-ttu-id="6d997-121">一般而言，驅動程式可以追蹤呼叫 [**的次數，**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 以防止佇列超過三個轉譯工作的畫面格。</span><span class="sxs-lookup"><span data-stu-id="6d997-121">In general, the driver can track the number of times [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called to prevent queuing up more than three frames of rendering work.</span></span>

</dd> <dt>

<span data-ttu-id="6d997-122">**WaitingForGPUExclusiveResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="6d997-122">**WaitingForGPUExclusiveResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="6d997-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d997-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d997-124">驅動程式花費在等候無法進行管線處理的資源 (的時間百分比，以平行) 方式運作。</span><span class="sxs-lookup"><span data-stu-id="6d997-124">Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel).</span></span> <span data-ttu-id="6d997-125">基於效能考慮，應用程式可能會想要避免使用非管線資源。</span><span class="sxs-lookup"><span data-stu-id="6d997-125">An application may want to avoid using a non-pipelined resource for performance reasons.</span></span>

</dd> <dt>

<span data-ttu-id="6d997-126">**WaitingForGPUOtherTimePercent**</span><span class="sxs-lookup"><span data-stu-id="6d997-126">**WaitingForGPUOtherTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="6d997-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d997-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d997-128">驅動程式等候其他 GPU 處理所花費的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="6d997-128">Percentage of time the driver spent waiting for other GPU processing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d997-129">備註</span><span class="sxs-lookup"><span data-stu-id="6d997-129">Remarks</span></span>

<span data-ttu-id="6d997-130">這些計量有助於識別驅動程式何時正在等候，以及它正在等待的時間。</span><span class="sxs-lookup"><span data-stu-id="6d997-130">These metrics help identify when a driver is waiting and what it is waiting for.</span></span> <span data-ttu-id="6d997-131">高百分比不一定是問題。</span><span class="sxs-lookup"><span data-stu-id="6d997-131">High percentages are not necessarily a problem.</span></span>

<span data-ttu-id="6d997-132">這些系統全域計量可能會或可能不會執行。</span><span class="sxs-lookup"><span data-stu-id="6d997-132">These system-global metrics may or may not be implemented.</span></span> <span data-ttu-id="6d997-133">根據特定的硬體而定，這些計量可能不會同時支援多個查詢。</span><span class="sxs-lookup"><span data-stu-id="6d997-133">Depending on the specific hardware, these metrics may not support multiple queries simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d997-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d997-134">Requirements</span></span>



| <span data-ttu-id="6d997-135">需求</span><span class="sxs-lookup"><span data-stu-id="6d997-135">Requirement</span></span> | <span data-ttu-id="6d997-136">值</span><span class="sxs-lookup"><span data-stu-id="6d997-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d997-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6d997-137">Header</span></span><br/> | <dl> <span data-ttu-id="6d997-138"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d997-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d997-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d997-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d997-140">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="6d997-140">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="6d997-141">**GetData**</span><span class="sxs-lookup"><span data-stu-id="6d997-141">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 

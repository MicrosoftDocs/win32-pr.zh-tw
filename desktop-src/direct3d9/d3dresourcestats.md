---
description: 使用非同步查詢機制時，由 D3DDEVINFO ResourceManager 收集的資源統計資料 \_ 。
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: 'D3DRESOURCESTATS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990017"
---
# <a name="d3dresourcestats-structure"></a><span data-ttu-id="83f00-103">D3DRESOURCESTATS 結構</span><span class="sxs-lookup"><span data-stu-id="83f00-103">D3DRESOURCESTATS structure</span></span>

<span data-ttu-id="83f00-104">使用非同步查詢機制時，由 [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md) 收集的資源統計資料。</span><span class="sxs-lookup"><span data-stu-id="83f00-104">Resource statistics gathered by the [**D3DDEVINFO\_ResourceManager**](d3ddevinfo-resourcemanager.md) when using the asynchronous query mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f00-105">語法</span><span class="sxs-lookup"><span data-stu-id="83f00-105">Syntax</span></span>


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a><span data-ttu-id="83f00-106">成員</span><span class="sxs-lookup"><span data-stu-id="83f00-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="83f00-107">**bThrashing**</span><span class="sxs-lookup"><span data-stu-id="83f00-107">**bThrashing**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-108">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-109">指出是否發生節流。</span><span class="sxs-lookup"><span data-stu-id="83f00-109">Indicates if thrashing is occurring.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-110">**ApproxBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="83f00-110">**ApproxBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-112">資源管理員所下載的大約位元組數目。</span><span class="sxs-lookup"><span data-stu-id="83f00-112">Approximate number of bytes downloaded by the resource manager.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-113">**NumEvicts**</span><span class="sxs-lookup"><span data-stu-id="83f00-113">**NumEvicts**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-115">已收回的物件數目。</span><span class="sxs-lookup"><span data-stu-id="83f00-115">Number of objects evicted.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-116">**NumVidCreates**</span><span class="sxs-lookup"><span data-stu-id="83f00-116">**NumVidCreates**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-118">在視訊記憶體中建立的物件數目。</span><span class="sxs-lookup"><span data-stu-id="83f00-118">Number of objects created in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-119">**LastPri**</span><span class="sxs-lookup"><span data-stu-id="83f00-119">**LastPri**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-121">上次收回物件的優先順序。</span><span class="sxs-lookup"><span data-stu-id="83f00-121">Priority of last object evicted.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-122">**NumUsed**</span><span class="sxs-lookup"><span data-stu-id="83f00-122">**NumUsed**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-124">設定至裝置的物件數目。</span><span class="sxs-lookup"><span data-stu-id="83f00-124">Number of objects set to the device.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-125">**NumUsedInVidMem**</span><span class="sxs-lookup"><span data-stu-id="83f00-125">**NumUsedInVidMem**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-126">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-127">已在視訊記憶體中設定至裝置的物件數目。</span><span class="sxs-lookup"><span data-stu-id="83f00-127">Number of objects set to the device, which are already in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-128">**WorkingSet**</span><span class="sxs-lookup"><span data-stu-id="83f00-128">**WorkingSet**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-129">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-129">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-130">視訊記憶體中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="83f00-130">Number of objects in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-131">**WorkingSetBytes**</span><span class="sxs-lookup"><span data-stu-id="83f00-131">**WorkingSetBytes**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-133">視訊記憶體中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="83f00-133">Number of bytes in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-134">**TotalManaged**</span><span class="sxs-lookup"><span data-stu-id="83f00-134">**TotalManaged**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-135">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-135">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-136">受管理物件的總數。</span><span class="sxs-lookup"><span data-stu-id="83f00-136">Total number of managed objects.</span></span>

</dd> <dt>

<span data-ttu-id="83f00-137">**TotalBytes**</span><span class="sxs-lookup"><span data-stu-id="83f00-137">**TotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="83f00-138">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83f00-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="83f00-139">Managed 物件的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="83f00-139">Total number of bytes of managed objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83f00-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="83f00-140">Requirements</span></span>



| <span data-ttu-id="83f00-141">需求</span><span class="sxs-lookup"><span data-stu-id="83f00-141">Requirement</span></span> | <span data-ttu-id="83f00-142">值</span><span class="sxs-lookup"><span data-stu-id="83f00-142">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83f00-143">標頭</span><span class="sxs-lookup"><span data-stu-id="83f00-143">Header</span></span><br/> | <dl> <span data-ttu-id="83f00-144"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="83f00-144"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83f00-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83f00-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f00-146">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="83f00-146">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="83f00-147"> (Direct3D 9) 的非同步通知 </span><span class="sxs-lookup"><span data-stu-id="83f00-147">Asynchronous Notification (Direct3D 9)</span></span>](asynchronous-notification.md)
</dt> </dl>

 

 

---
description: 用來指定網格之建立選項的旗標。
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: 'D3DXMESH 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 602eb38f2113b54ee02477faf3bdd15a6a924abc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322651"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="c5ec3-103">D3DXMESH 列舉</span><span class="sxs-lookup"><span data-stu-id="c5ec3-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="c5ec3-104">用來指定網格之建立選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ec3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5ec3-105">Syntax</span></span>


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a><span data-ttu-id="c5ec3-106">常數</span><span class="sxs-lookup"><span data-stu-id="c5ec3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c5ec3-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 位**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-108">網格有32位的索引，而不是16位的索引。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="c5ec3-109">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-111">針對頂點和索引緩衝區使用 [**D3DUSAGE \_ DONOTCLIP**](d3dusage.md) usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH \_ 點**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-113">針對頂點和索引緩衝區使用 [**D3DUSAGE \_ 點**](d3dusage.md) 使用方式旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-115">針對頂點和索引緩衝區使用 [**D3DUSAGE \_ RTPATCHES**](d3dusage.md) usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-117">指定此旗標會讓網格的頂點和索引緩衝區以 [**D3DUSAGE \_ NPATCHES**](d3dusage.md) 旗標建立。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="c5ec3-118">如果要使用 Direct3D 以 N 修補程式增強功能來呈現網格物件，則這是必要的。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-120">針對頂點緩衝區使用 [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ MANAGED**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-122">針對頂點緩衝區使用 [**D3DPOOL \_ 受控**](./d3dpool.md) 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-124">針對頂點緩衝區使用 [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ 動態**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-126">針對頂點緩衝區使用 [**D3DUSAGE \_ 動態**](d3dusage.md) 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-128">針對頂點緩衝區使用 [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-130">使用索引緩衝區的 [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ 管理**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-132">使用索引緩衝區的 [**D3DPOOL \_ 受控**](./d3dpool.md) 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-134">使用索引緩衝區的 [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ 動態**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-136">使用索引緩衝區的 [**D3DUSAGE \_ 動態**](d3dusage.md) 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-138">使用索引緩衝區的 [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ VB \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-140">強制複製的網格共用頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-142">只使用硬體處理。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-142">Use hardware processing only.</span></span> <span data-ttu-id="c5ec3-143">若為混合模式裝置，此旗標將會導致系統使用硬體 (（如果硬體) 支援）或預設為軟體處理。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-145">相當於同時指定 D3DXMESH \_ VB \_ SYSTEMMEM 和 D3DXMESH \_ IB \_ SYSTEMMEM。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ 受控**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-147">相當於指定 D3DXMESH \_ VB managed \_ 和 D3DXMESH \_ IB \_ managed。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-149">相當於同時指定 D3DXMESH \_ VB \_ WRITEONLY 和 D3DXMESH \_ IB \_ writeonly。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ 動態**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-151">相當於同時指定 D3DXMESH \_ VB \_ DYNAMIC 和 D3DXMESH \_ IB \_ dynamic。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="c5ec3-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="c5ec3-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="c5ec3-153">相當於同時指定 D3DXMESH \_ VB \_ SOFTWAREPROCESSING 和 D3DXMESH \_ IB \_ SOFTWAREPROCESSING。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5ec3-154">備註</span><span class="sxs-lookup"><span data-stu-id="c5ec3-154">Remarks</span></span>

<span data-ttu-id="c5ec3-155">32位網格 (D3DXMESH 32 位 \_) 理論上可支援 (2 ^ 32) -1 臉部和頂點。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="c5ec3-156">不過，為在32位作業系統上大的網狀架構配置記憶體並不實用。</span><span class="sxs-lookup"><span data-stu-id="c5ec3-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ec3-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5ec3-157">Requirements</span></span>



| <span data-ttu-id="c5ec3-158">需求</span><span class="sxs-lookup"><span data-stu-id="c5ec3-158">Requirement</span></span> | <span data-ttu-id="c5ec3-159">值</span><span class="sxs-lookup"><span data-stu-id="c5ec3-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ec3-160">標頭</span><span class="sxs-lookup"><span data-stu-id="c5ec3-160">Header</span></span><br/> | <dl> <span data-ttu-id="c5ec3-161"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ec3-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ec3-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5ec3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ec3-163">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="c5ec3-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 

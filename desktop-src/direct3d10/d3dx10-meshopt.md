---
description: 指定要執行的網格優化類型。
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: 'D3DX10_MESHOPT 列舉 (D3DX10Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c8ccb13da1549b7e2eeeb67ebf7899c2187be363
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323200"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="9c6c7-103">D3DX10 \_ MESHOPT 列舉</span><span class="sxs-lookup"><span data-stu-id="9c6c7-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="9c6c7-104">指定要執行的網格優化類型。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c6c7-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a><span data-ttu-id="9c6c7-106">常數</span><span class="sxs-lookup"><span data-stu-id="9c6c7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9c6c7-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**</span><span class="sxs-lookup"><span data-stu-id="9c6c7-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="9c6c7-108">重新排序臉部以移除未使用的頂點和臉部。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c7-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ 排序**</span><span class="sxs-lookup"><span data-stu-id="9c6c7-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="9c6c7-110">重新排列臉部以針對較少的屬性套件組合狀態變更和增強的 DrawSubset 效能進行優化。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c7-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ 頂點快取 \_**</span><span class="sxs-lookup"><span data-stu-id="9c6c7-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="9c6c7-112">重新排列臉部以增加頂點快取的快取點擊率。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c7-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10 \_ MESHOPT \_ 帶狀 \_ 重新排序**</span><span class="sxs-lookup"><span data-stu-id="9c6c7-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="9c6c7-114">重新排列臉部以將相鄰三角形的最大長度重新排序。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c7-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ 忽略 \_ VERTS**</span><span class="sxs-lookup"><span data-stu-id="9c6c7-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="9c6c7-116">僅將臉部優化;請勿將頂點優化。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c7-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ 不 \_ \_ 分割**</span><span class="sxs-lookup"><span data-stu-id="9c6c7-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="9c6c7-118">屬性排序時，請勿分割屬性群組之間共用的頂點。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="9c6c7-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**\_ \_ 獨立于 D3DX10 MESHOPT 裝置 \_**</span><span class="sxs-lookup"><span data-stu-id="9c6c7-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="9c6c7-120">影響頂點快取大小。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-120">Affects the vertex cache size.</span></span> <span data-ttu-id="9c6c7-121">使用此旗標可指定在舊版硬體上運作正常的預設頂點快取大小。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c6c7-122">備註</span><span class="sxs-lookup"><span data-stu-id="9c6c7-122">Remarks</span></span>

<span data-ttu-id="9c6c7-123">D3DXMESHOPT \_ STRIPREORDER 和 D3DXMESHOPT \_ VERTEXCACHE 優化旗標彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="9c6c7-124">\_此列舉已移除 D3DXMESHOPT SHAREVB 旗標。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="9c6c7-125">\_ \_ 在 D3DXMESH 中，請改用 D3DXMESH VB SHARE。</span><span class="sxs-lookup"><span data-stu-id="9c6c7-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c6c7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c6c7-126">Requirements</span></span>



| <span data-ttu-id="9c6c7-127">需求</span><span class="sxs-lookup"><span data-stu-id="9c6c7-127">Requirement</span></span> | <span data-ttu-id="9c6c7-128">值</span><span class="sxs-lookup"><span data-stu-id="9c6c7-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6c7-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9c6c7-129">Header</span></span><br/> | <dl> <span data-ttu-id="9c6c7-130"><dt>D3DX10Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c6c7-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c6c7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c6c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6c7-132">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="9c6c7-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





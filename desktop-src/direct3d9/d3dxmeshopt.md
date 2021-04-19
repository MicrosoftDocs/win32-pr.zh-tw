---
description: 指定要執行的網格優化類型。
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: 'D3DXMESHOPT 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986090"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="5b1e2-103">D3DXMESHOPT 列舉</span><span class="sxs-lookup"><span data-stu-id="5b1e2-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="5b1e2-104">指定要執行的網格優化類型。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b1e2-105">Syntax</span></span>


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a><span data-ttu-id="5b1e2-106">常數</span><span class="sxs-lookup"><span data-stu-id="5b1e2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5b1e2-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="5b1e2-108">重新排序臉部以移除未使用的頂點和臉部。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="5b1e2-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="5b1e2-110">重新排列臉部以針對較少的屬性套件組合狀態變更和增強的 ID3DXBaseMesh 進行優化 [**：:D rawsubset**](id3dxbasemesh--drawsubset.md) 效能。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="5b1e2-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="5b1e2-112">重新排列臉部以增加頂點快取的快取點擊率。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="5b1e2-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="5b1e2-114">重新排列臉部以將相鄰三角形的最大長度重新排序。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="5b1e2-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="5b1e2-116">僅將臉部優化;請勿將頂點優化。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="5b1e2-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="5b1e2-118">屬性排序時，請勿分割屬性群組之間共用的頂點。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="5b1e2-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="5b1e2-120">影響頂點快取大小。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-120">Affects the vertex cache size.</span></span> <span data-ttu-id="5b1e2-121">使用此旗標可指定在舊版硬體上運作正常的預設頂點快取大小。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b1e2-122">備註</span><span class="sxs-lookup"><span data-stu-id="5b1e2-122">Remarks</span></span>

<span data-ttu-id="5b1e2-123">D3DXMESHOPT \_ STRIPREORDER 和 D3DXMESHOPT \_ VERTEXCACHE 優化旗標彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="5b1e2-124">\_此列舉已移除 D3DXMESHOPT SHAREVB 旗標。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="5b1e2-125">\_ \_ 在 [**D3DXMESH**](./d3dxmesh.md)中，請改用 D3DXMESH VB SHARE。</span><span class="sxs-lookup"><span data-stu-id="5b1e2-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1e2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b1e2-126">Requirements</span></span>



| <span data-ttu-id="5b1e2-127">需求</span><span class="sxs-lookup"><span data-stu-id="5b1e2-127">Requirement</span></span> | <span data-ttu-id="5b1e2-128">值</span><span class="sxs-lookup"><span data-stu-id="5b1e2-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1e2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5b1e2-129">Header</span></span><br/> | <dl> <span data-ttu-id="5b1e2-130"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b1e2-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b1e2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b1e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1e2-132">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="5b1e2-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 

---
description: 定義要在頂點上執行的作業，以準備進行網格清理。
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: 'D3DXCLEANTYPE 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196301"
---
# <a name="d3dxcleantype-enumeration"></a><span data-ttu-id="fd8bd-103">D3DXCLEANTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="fd8bd-103">D3DXCLEANTYPE enumeration</span></span>

<span data-ttu-id="fd8bd-104">定義要在頂點上執行的作業，以準備進行網格清理。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-104">Defines operations to perform on vertices in preparation for mesh cleaning.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd8bd-105">Syntax</span></span>


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a><span data-ttu-id="fd8bd-106">常數</span><span class="sxs-lookup"><span data-stu-id="fd8bd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd8bd-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKFACING**</span><span class="sxs-lookup"><span data-stu-id="fd8bd-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN\_BACKFACING**</span></span>
</dt> <dd>

<span data-ttu-id="fd8bd-108">共用相同頂點索引的合併三角形，但以相反方向指向的臉部法線 () 的回溯三角形。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-108">Merge triangles that share the same vertex indices but have face normals pointing in opposite directions (back-facing triangles).</span></span> <span data-ttu-id="fd8bd-109">除非三角形未藉由新增複寫頂點來分割，否則兩個三角形的網狀相鄰資料可能會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-109">Unless the triangles are not split by adding a replicated vertex, mesh adjacency data from the two triangles may conflict.</span></span>

</dd> <dt>

<span data-ttu-id="fd8bd-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**</span><span class="sxs-lookup"><span data-stu-id="fd8bd-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN\_BOWTIES**</span></span>
</dt> <dd>

<span data-ttu-id="fd8bd-111">如果頂點是兩個三角形風扇的頂點 () ，而網格操作將會影響其中一個風扇，然後將共用頂點分割成兩個新頂點。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-111">If a vertex is the apex of two triangle fans (a bowtie) and mesh operations will affect one of the fans, then split the shared vertex into two new vertices.</span></span> <span data-ttu-id="fd8bd-112">Bowties 可能會對移除頂點的作業（例如網格簡化）造成問題，因為移除一個頂點會影響兩組不同的三角形。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-112">Bowties can cause problems for operations such as mesh simplification that remove vertices, because removing one vertex affects two distinct sets of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="fd8bd-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN \_ 外觀**</span><span class="sxs-lookup"><span data-stu-id="fd8bd-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN\_SKINNING**</span></span>
</dt> <dd>

<span data-ttu-id="fd8bd-114">使用此旗標來防止在設定網格操作時進行無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-114">Use this flag to prevent infinite loops during skinning setup mesh operations.</span></span>

</dd> <dt>

<span data-ttu-id="fd8bd-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN \_ 優化**</span><span class="sxs-lookup"><span data-stu-id="fd8bd-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN\_OPTIMIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="fd8bd-116">使用此旗標來防止網格優化作業期間的無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-116">Use this flag to prevent infinite loops during mesh optimization operations.</span></span>

</dd> <dt>

<span data-ttu-id="fd8bd-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN \_ 簡化**</span><span class="sxs-lookup"><span data-stu-id="fd8bd-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN\_SIMPLIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="fd8bd-118">使用此旗標來防止網格簡化作業期間的無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="fd8bd-118">Use this flag to prevent infinite loops during mesh simplification operations.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd8bd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd8bd-119">Requirements</span></span>



| <span data-ttu-id="fd8bd-120">需求</span><span class="sxs-lookup"><span data-stu-id="fd8bd-120">Requirement</span></span> | <span data-ttu-id="fd8bd-121">值</span><span class="sxs-lookup"><span data-stu-id="fd8bd-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8bd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fd8bd-122">Header</span></span><br/> | <dl> <span data-ttu-id="fd8bd-123"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8bd-123"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8bd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd8bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8bd-125">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="fd8bd-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





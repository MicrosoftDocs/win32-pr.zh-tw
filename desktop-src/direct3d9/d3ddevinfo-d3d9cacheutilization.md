---
description: 測量紋理和索引頂點的快取點擊率效能。
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: 'D3DDEVINFO_D3D9CACHEUTILIZATION 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514569"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a><span data-ttu-id="1f436-103">D3DDEVINFO \_ D3D9CACHEUTILIZATION 結構</span><span class="sxs-lookup"><span data-stu-id="1f436-103">D3DDEVINFO\_D3D9CACHEUTILIZATION structure</span></span>

<span data-ttu-id="1f436-104">測量紋理和索引頂點的快取點擊率效能。</span><span class="sxs-lookup"><span data-stu-id="1f436-104">Measure the cache hit rate performance for textures and indexed vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f436-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f436-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a><span data-ttu-id="1f436-106">成員</span><span class="sxs-lookup"><span data-stu-id="1f436-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f436-107">**TextureCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="1f436-107">**TextureCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="1f436-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f436-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f436-109">在紋理快取中尋找材質的點擊率。</span><span class="sxs-lookup"><span data-stu-id="1f436-109">The hit rate for finding a texture in the texture cache.</span></span> <span data-ttu-id="1f436-110">這假設有紋理快取。</span><span class="sxs-lookup"><span data-stu-id="1f436-110">This assumes there is a texture cache.</span></span> <span data-ttu-id="1f436-111">使用許多大型紋理來增加詳細資料偏差，以使用最詳細的材質，或使用自訂著色器程式碼在大型紋理上產生近乎隨機的材質存取模式，可能會大幅影響紋理快取點擊率。</span><span class="sxs-lookup"><span data-stu-id="1f436-111">Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.</span></span>

</dd> <dt>

<span data-ttu-id="1f436-112">**PostTransformVertexCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="1f436-112">**PostTransformVertexCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="1f436-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f436-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f436-114">在頂點快取中尋找已轉換頂點的點擊率。</span><span class="sxs-lookup"><span data-stu-id="1f436-114">The hit rate for finding transformed vertices in the vertex cache.</span></span> <span data-ttu-id="1f436-115">GPU 的設計目的是要轉換索引的頂點，並可將其儲存在頂點快取中。</span><span class="sxs-lookup"><span data-stu-id="1f436-115">The GPU is designed to transform indexed vertices and may store them in a vertex cache.</span></span> <span data-ttu-id="1f436-116">如果您使用的是網格， [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) 或 [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) 可能會導致更好的頂點快取使用。</span><span class="sxs-lookup"><span data-stu-id="1f436-116">If you are using meshes, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) or [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) may result in better vertex cache utilization.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f436-117">備註</span><span class="sxs-lookup"><span data-stu-id="1f436-117">Remarks</span></span>

<span data-ttu-id="1f436-118">有效率的快取通常較接近90% 的點擊率，而且效率不佳的快取通常會接近10% 的點擊率 (但低百分比不一定是) 的問題。</span><span class="sxs-lookup"><span data-stu-id="1f436-118">An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f436-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f436-119">Requirements</span></span>



| <span data-ttu-id="1f436-120">需求</span><span class="sxs-lookup"><span data-stu-id="1f436-120">Requirement</span></span> | <span data-ttu-id="1f436-121">值</span><span class="sxs-lookup"><span data-stu-id="1f436-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f436-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1f436-122">Header</span></span><br/> | <dl> <span data-ttu-id="1f436-123"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f436-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f436-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f436-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f436-125">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="1f436-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="1f436-126">**GetData**</span><span class="sxs-lookup"><span data-stu-id="1f436-126">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 

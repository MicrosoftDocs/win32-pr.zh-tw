---
description: 將頂點焊接在一起的選項。
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: 'D3DXWELDEPSILONSFLAGS 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322992"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a><span data-ttu-id="27f1e-103">D3DXWELDEPSILONSFLAGS 列舉</span><span class="sxs-lookup"><span data-stu-id="27f1e-103">D3DXWELDEPSILONSFLAGS enumeration</span></span>

<span data-ttu-id="27f1e-104">將頂點焊接在一起的選項。</span><span class="sxs-lookup"><span data-stu-id="27f1e-104">Options for welding together vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="27f1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27f1e-105">Syntax</span></span>


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a><span data-ttu-id="27f1e-106">常數</span><span class="sxs-lookup"><span data-stu-id="27f1e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="27f1e-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**</span><span class="sxs-lookup"><span data-stu-id="27f1e-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS\_WELDALL**</span></span>
</dt> <dd>

<span data-ttu-id="27f1e-108">將位於相同位置的所有頂點焊接在一起。</span><span class="sxs-lookup"><span data-stu-id="27f1e-108">Weld together all vertices that are at the same location.</span></span> <span data-ttu-id="27f1e-109">使用這個旗標可避免頂點元件之間的 epsilon 比較。</span><span class="sxs-lookup"><span data-stu-id="27f1e-109">Using this flag avoids an epsilon comparison between vertex components.</span></span>

</dd> <dt>

<span data-ttu-id="27f1e-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**</span><span class="sxs-lookup"><span data-stu-id="27f1e-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS\_WELDPARTIALMATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="27f1e-111">如果指定的頂點元件在 epsilon 內，請修改部分相符的頂點，使這兩個元件相同。</span><span class="sxs-lookup"><span data-stu-id="27f1e-111">If a given vertex component is within epsilon, modify partially matched vertices so that both components are identical.</span></span> <span data-ttu-id="27f1e-112">如果所有元件相等，請移除其中一個頂點。</span><span class="sxs-lookup"><span data-stu-id="27f1e-112">If all components are equal, remove one of the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="27f1e-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**</span><span class="sxs-lookup"><span data-stu-id="27f1e-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS\_DONOTREMOVEVERTICES**</span></span>
</dt> <dd>

<span data-ttu-id="27f1e-114">指示焊縫只允許修改頂點，而不會移除。</span><span class="sxs-lookup"><span data-stu-id="27f1e-114">Instructs the weld to allow only modifications to vertices and not removal.</span></span> <span data-ttu-id="27f1e-115">只有在設定 D3DXWELDEPSILONS WELDPARTIALMATCHES 時，此旗標才有效 \_ 。</span><span class="sxs-lookup"><span data-stu-id="27f1e-115">This flag is valid only if D3DXWELDEPSILONS\_WELDPARTIALMATCHES is set.</span></span> <span data-ttu-id="27f1e-116">將頂點修改為相等，但不允許移除頂點會很有用。</span><span class="sxs-lookup"><span data-stu-id="27f1e-116">It is useful to modify vertices to be equal, but not to allow vertices to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="27f1e-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="27f1e-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="27f1e-118">指示焊縫不要分割位於不同屬性群組中的頂點。</span><span class="sxs-lookup"><span data-stu-id="27f1e-118">Instructs the weld not to split vertices that are in separate attribute groups.</span></span> <span data-ttu-id="27f1e-119">使用 D3DXMESHOPT ATTRSORT 旗標呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 方法時 \_ ， \_ 也會設定 D3DXMESHOPT DONOTSPLIT 旗標。</span><span class="sxs-lookup"><span data-stu-id="27f1e-119">When the [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method is called with the D3DXMESHOPT\_ATTRSORT flag, then the D3DXMESHOPT\_DONOTSPLIT flag will also be set.</span></span> <span data-ttu-id="27f1e-120">設定此旗標可能會減緩軟體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="27f1e-120">Setting this flag can slow down software vertex processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27f1e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="27f1e-121">Requirements</span></span>



| <span data-ttu-id="27f1e-122">需求</span><span class="sxs-lookup"><span data-stu-id="27f1e-122">Requirement</span></span> | <span data-ttu-id="27f1e-123">值</span><span class="sxs-lookup"><span data-stu-id="27f1e-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27f1e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="27f1e-124">Header</span></span><br/> | <dl> <span data-ttu-id="27f1e-125"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="27f1e-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27f1e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27f1e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27f1e-127">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="27f1e-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="27f1e-128">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="27f1e-128">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 





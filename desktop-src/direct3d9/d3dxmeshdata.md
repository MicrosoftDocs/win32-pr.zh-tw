---
description: 網格資料結構。
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: 'D3DXMESHDATA 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322647"
---
# <a name="d3dxmeshdata-structure"></a><span data-ttu-id="e04c7-103">D3DXMESHDATA 結構</span><span class="sxs-lookup"><span data-stu-id="e04c7-103">D3DXMESHDATA structure</span></span>

<span data-ttu-id="e04c7-104">網格資料結構。</span><span class="sxs-lookup"><span data-stu-id="e04c7-104">Mesh data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="e04c7-105">Syntax</span></span>


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a><span data-ttu-id="e04c7-106">成員</span><span class="sxs-lookup"><span data-stu-id="e04c7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e04c7-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="e04c7-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e04c7-108">類型： **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span><span class="sxs-lookup"><span data-stu-id="e04c7-108">Type: **[**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e04c7-109">定義網格資料類型。</span><span class="sxs-lookup"><span data-stu-id="e04c7-109">Defines the mesh data type.</span></span> <span data-ttu-id="e04c7-110">請參閱 [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)。</span><span class="sxs-lookup"><span data-stu-id="e04c7-110">See [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="e04c7-111">**pMesh**</span><span class="sxs-lookup"><span data-stu-id="e04c7-111">**pMesh**</span></span>
</dt> <dd>

<span data-ttu-id="e04c7-112">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="e04c7-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e04c7-113">網格的指標。</span><span class="sxs-lookup"><span data-stu-id="e04c7-113">Pointer to a mesh.</span></span> <span data-ttu-id="e04c7-114">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="e04c7-114">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="e04c7-115">**pPatchMesh**</span><span class="sxs-lookup"><span data-stu-id="e04c7-115">**pPatchMesh**</span></span>
</dt> <dd>

<span data-ttu-id="e04c7-116">類型： **LPD3DXPATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="e04c7-116">Type: **LPD3DXPATCHMESH**</span></span>

</dd> <dd>

<span data-ttu-id="e04c7-117">修補程式網格的指標。</span><span class="sxs-lookup"><span data-stu-id="e04c7-117">Pointer to a patch mesh.</span></span> <span data-ttu-id="e04c7-118">請參閱 [**ID3DXPatchMesh**](id3dxpatchmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="e04c7-118">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e04c7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e04c7-119">Requirements</span></span>



| <span data-ttu-id="e04c7-120">需求</span><span class="sxs-lookup"><span data-stu-id="e04c7-120">Requirement</span></span> | <span data-ttu-id="e04c7-121">值</span><span class="sxs-lookup"><span data-stu-id="e04c7-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e04c7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e04c7-122">Header</span></span><br/> | <dl> <span data-ttu-id="e04c7-123"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="e04c7-123"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04c7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e04c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04c7-125">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="e04c7-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e04c7-126">**D3DXMESHCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="e04c7-126">**D3DXMESHCONTAINER**</span></span>](d3dxmeshcontainer.md)
</dt> </dl>

 

 

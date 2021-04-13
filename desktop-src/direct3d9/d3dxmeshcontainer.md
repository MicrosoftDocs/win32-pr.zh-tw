---
description: 封裝轉換框架階層中的網格物件。
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: 'D3DXMESHCONTAINER 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322648"
---
# <a name="d3dxmeshcontainer-structure"></a><span data-ttu-id="adafd-103">D3DXMESHCONTAINER 結構</span><span class="sxs-lookup"><span data-stu-id="adafd-103">D3DXMESHCONTAINER structure</span></span>

<span data-ttu-id="adafd-104">封裝轉換框架階層中的網格物件。</span><span class="sxs-lookup"><span data-stu-id="adafd-104">Encapsulates a mesh object in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="adafd-105">語法</span><span class="sxs-lookup"><span data-stu-id="adafd-105">Syntax</span></span>


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a><span data-ttu-id="adafd-106">成員</span><span class="sxs-lookup"><span data-stu-id="adafd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="adafd-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="adafd-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-108">類型： **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="adafd-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="adafd-109">網格名稱。</span><span class="sxs-lookup"><span data-stu-id="adafd-109">Mesh name.</span></span>

</dd> <dt>

<span data-ttu-id="adafd-110">**MeshData**</span><span class="sxs-lookup"><span data-stu-id="adafd-110">**MeshData**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-111">類型： **[ **D3DXMESHDATA**](d3dxmeshdata.md)**</span><span class="sxs-lookup"><span data-stu-id="adafd-111">Type: **[**D3DXMESHDATA**](d3dxmeshdata.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adafd-112">網格中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="adafd-112">Type of data in the mesh.</span></span> <span data-ttu-id="adafd-113">請參閱 [**D3DXMESHDATA**](d3dxmeshdata.md)。</span><span class="sxs-lookup"><span data-stu-id="adafd-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="adafd-114">**pMaterials**</span><span class="sxs-lookup"><span data-stu-id="adafd-114">**pMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-115">類型： **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**</span><span class="sxs-lookup"><span data-stu-id="adafd-115">Type: **[**LPD3DXMATERIAL**](d3dxmaterial.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adafd-116">網格材質的陣列。</span><span class="sxs-lookup"><span data-stu-id="adafd-116">Array of mesh materials.</span></span> <span data-ttu-id="adafd-117">請參閱 [**D3DXMATERIAL**](d3dxmaterial.md)。</span><span class="sxs-lookup"><span data-stu-id="adafd-117">See [**D3DXMATERIAL**](d3dxmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="adafd-118">**pEffects**</span><span class="sxs-lookup"><span data-stu-id="adafd-118">**pEffects**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-119">類型： **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span><span class="sxs-lookup"><span data-stu-id="adafd-119">Type: **[**LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adafd-120">一組預設效果參數的指標。</span><span class="sxs-lookup"><span data-stu-id="adafd-120">Pointer to a set of default effect parameters.</span></span> <span data-ttu-id="adafd-121">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="adafd-121">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="adafd-122">**NumMaterials**</span><span class="sxs-lookup"><span data-stu-id="adafd-122">**NumMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="adafd-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adafd-124">網格中的材質數目。</span><span class="sxs-lookup"><span data-stu-id="adafd-124">Number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="adafd-125">**pAdjacency**</span><span class="sxs-lookup"><span data-stu-id="adafd-125">**pAdjacency**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-126">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="adafd-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="adafd-127">包含相鄰資訊之網格的每個三角形的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="adafd-127">Pointer to an array of three DWORDs per triangle of the mesh that contains adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="adafd-128">**pSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="adafd-128">**pSkinInfo**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-129">類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="adafd-129">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adafd-130">外觀資訊介面的指標。</span><span class="sxs-lookup"><span data-stu-id="adafd-130">Pointer to the skin information interface.</span></span> <span data-ttu-id="adafd-131">請參閱 [**ID3DXSkinInfo**](id3dxskininfo.md)。</span><span class="sxs-lookup"><span data-stu-id="adafd-131">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="adafd-132">**pNextMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="adafd-132">**pNextMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="adafd-133">類型： \* \* \* \* D3DXMESHCONTAINER **\***</span><span class="sxs-lookup"><span data-stu-id="adafd-133">Type: \*\*\*\*D3DXMESHCONTAINER **\***</span></span>

</dd> <dd>

<span data-ttu-id="adafd-134">下一個網格容器的指標。</span><span class="sxs-lookup"><span data-stu-id="adafd-134">Pointer to the next mesh container.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adafd-135">備註</span><span class="sxs-lookup"><span data-stu-id="adafd-135">Remarks</span></span>

<span data-ttu-id="adafd-136">應用程式可以從此結構衍生，以新增其他資料。</span><span class="sxs-lookup"><span data-stu-id="adafd-136">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="adafd-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="adafd-137">Requirements</span></span>



| <span data-ttu-id="adafd-138">需求</span><span class="sxs-lookup"><span data-stu-id="adafd-138">Requirement</span></span> | <span data-ttu-id="adafd-139">值</span><span class="sxs-lookup"><span data-stu-id="adafd-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adafd-140">標頭</span><span class="sxs-lookup"><span data-stu-id="adafd-140">Header</span></span><br/> | <dl> <span data-ttu-id="adafd-141"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="adafd-141"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adafd-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adafd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adafd-143">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="adafd-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

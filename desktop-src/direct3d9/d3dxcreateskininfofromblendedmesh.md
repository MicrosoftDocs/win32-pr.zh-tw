---
description: 從另一個網格建立外觀網格。
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: 'D3DXCreateSkinInfoFromBlendedMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514609"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a><span data-ttu-id="effe3-103">D3DXCreateSkinInfoFromBlendedMesh 函式</span><span class="sxs-lookup"><span data-stu-id="effe3-103">D3DXCreateSkinInfoFromBlendedMesh function</span></span>

<span data-ttu-id="effe3-104">從另一個網格建立外觀網格。</span><span class="sxs-lookup"><span data-stu-id="effe3-104">Creates a skin mesh from another mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="effe3-105">語法</span><span class="sxs-lookup"><span data-stu-id="effe3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="effe3-106">參數</span><span class="sxs-lookup"><span data-stu-id="effe3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effe3-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="effe3-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effe3-108">類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="effe3-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="effe3-109">[**ID3DXBaseMesh**](id3dxbasemesh.md)物件的指標，用來建立面板網格的網格。</span><span class="sxs-lookup"><span data-stu-id="effe3-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) object, the mesh from which to create the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="effe3-110">*NumBones* \[在\]</span><span class="sxs-lookup"><span data-stu-id="effe3-110">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effe3-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="effe3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="effe3-112">附加至 BoneId 的陣列長度。</span><span class="sxs-lookup"><span data-stu-id="effe3-112">The length of the array attached to the BoneId.</span></span> <span data-ttu-id="effe3-113">請參閱 [**D3DXBONECOMBINATION**](d3dxbonecombination.md)。</span><span class="sxs-lookup"><span data-stu-id="effe3-113">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="effe3-114">*pBoneCombinationTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="effe3-114">*pBoneCombinationTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effe3-115">Type： **Const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***</span><span class="sxs-lookup"><span data-stu-id="effe3-115">Type: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md)\***</span></span>

<span data-ttu-id="effe3-116">骨骼組合陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="effe3-116">Pointer to an array of bone combinations.</span></span> <span data-ttu-id="effe3-117">請參閱 [**D3DXBONECOMBINATION**](d3dxbonecombination.md)。</span><span class="sxs-lookup"><span data-stu-id="effe3-117">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="effe3-118">*ppSkinInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="effe3-118">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="effe3-119">類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="effe3-119">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="effe3-120">[**ID3DXSkinInfo**](id3dxskininfo.md)介面指標的位址，表示所建立的面板網格物件。</span><span class="sxs-lookup"><span data-stu-id="effe3-120">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effe3-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="effe3-121">Return value</span></span>

<span data-ttu-id="effe3-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="effe3-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="effe3-123">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="effe3-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="effe3-124">如果函式失敗，則傳回值可以是下列內容： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="effe3-124">If the function fails, the return value can be the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="effe3-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="effe3-125">Requirements</span></span>



| <span data-ttu-id="effe3-126">需求</span><span class="sxs-lookup"><span data-stu-id="effe3-126">Requirement</span></span> | <span data-ttu-id="effe3-127">值</span><span class="sxs-lookup"><span data-stu-id="effe3-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="effe3-128">標頭</span><span class="sxs-lookup"><span data-stu-id="effe3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="effe3-129"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="effe3-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="effe3-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="effe3-130">Library</span></span><br/> | <dl> <span data-ttu-id="effe3-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="effe3-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="effe3-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="effe3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effe3-133">網格函數</span><span class="sxs-lookup"><span data-stu-id="effe3-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

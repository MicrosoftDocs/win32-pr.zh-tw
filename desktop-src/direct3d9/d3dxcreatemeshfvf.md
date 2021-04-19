---
description: 使用 (FVF) 程式碼的彈性頂點格式來建立網格物件。
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: 'D3DXCreateMeshFVF 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999048"
---
# <a name="d3dxcreatemeshfvf-function"></a><span data-ttu-id="d6432-103">D3DXCreateMeshFVF 函式</span><span class="sxs-lookup"><span data-stu-id="d6432-103">D3DXCreateMeshFVF function</span></span>

<span data-ttu-id="d6432-104">使用 (FVF) 程式碼的彈性頂點格式來建立網格物件。</span><span class="sxs-lookup"><span data-stu-id="d6432-104">Creates a mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6432-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6432-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d6432-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6432-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6432-107">*NumFaces* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6432-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6432-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6432-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6432-109">網格的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="d6432-109">Number of faces for the mesh.</span></span> <span data-ttu-id="d6432-110">此數位的有效範圍大於0，而一個小於最大 DWORD 值（通常是2³²-1），因為會保留最後一個索引。</span><span class="sxs-lookup"><span data-stu-id="d6432-110">The valid range for this number is greater than 0, and one less than the max DWORD value, typically 2³² - 1, because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d6432-111">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6432-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6432-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6432-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6432-113">網格的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="d6432-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="d6432-114">此參數必須大於0。</span><span class="sxs-lookup"><span data-stu-id="d6432-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="d6432-115">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6432-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6432-116">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6432-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6432-117">結合 [**D3DXMESH**](./d3dxmesh.md) 列舉中的一或多個旗標，指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="d6432-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d6432-118">*FVF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6432-118">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6432-119">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6432-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6432-120">描述所傳回網格之頂點格式的 [D3DFVF](d3dfvf.md) 組合。</span><span class="sxs-lookup"><span data-stu-id="d6432-120">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned mesh.</span></span> <span data-ttu-id="d6432-121">此函數不支援 D3DFVF \_ XYZRHW。</span><span class="sxs-lookup"><span data-stu-id="d6432-121">This function does not support D3DFVF\_XYZRHW.</span></span>

</dd> <dt>

<span data-ttu-id="d6432-122">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6432-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6432-123">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d6432-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d6432-124">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，也就是要與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="d6432-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d6432-125">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d6432-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6432-126">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6432-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d6432-127">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示所建立的網格物件。</span><span class="sxs-lookup"><span data-stu-id="d6432-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6432-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6432-128">Return value</span></span>

<span data-ttu-id="d6432-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6432-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6432-130">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d6432-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d6432-131">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="d6432-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6432-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6432-132">Requirements</span></span>



| <span data-ttu-id="d6432-133">需求</span><span class="sxs-lookup"><span data-stu-id="d6432-133">Requirement</span></span> | <span data-ttu-id="d6432-134">值</span><span class="sxs-lookup"><span data-stu-id="d6432-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6432-135">標頭</span><span class="sxs-lookup"><span data-stu-id="d6432-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d6432-136"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6432-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d6432-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6432-137">Library</span></span><br/> | <dl> <span data-ttu-id="d6432-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6432-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6432-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6432-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6432-140">網格函數</span><span class="sxs-lookup"><span data-stu-id="d6432-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d6432-141">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="d6432-141">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 

---
description: 使用宣告子建立網格物件。
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: 'D3DXCreateMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cfb56fe5c52d2726dff0877522b6f72f70437552
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001482"
---
# <a name="d3dxcreatemesh-function"></a><span data-ttu-id="4c581-103">D3DXCreateMesh 函式</span><span class="sxs-lookup"><span data-stu-id="4c581-103">D3DXCreateMesh function</span></span>

<span data-ttu-id="4c581-104">使用宣告子建立網格物件。</span><span class="sxs-lookup"><span data-stu-id="4c581-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c581-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c581-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="4c581-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c581-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c581-107">*NumFaces* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c581-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c581-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c581-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c581-109">網格的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="4c581-109">Number of faces for the mesh.</span></span> <span data-ttu-id="4c581-110">此數位的有效範圍大於0，而一個小於最大 DWORD (通常是 65534) ，因為會保留最後一個索引。</span><span class="sxs-lookup"><span data-stu-id="4c581-110">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4c581-111">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c581-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c581-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c581-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c581-113">網格的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="4c581-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="4c581-114">此參數必須大於0。</span><span class="sxs-lookup"><span data-stu-id="4c581-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="4c581-115">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c581-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c581-116">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c581-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c581-117">[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，指定網格的選項。</span><span class="sxs-lookup"><span data-stu-id="4c581-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4c581-118">*pDeclaration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c581-118">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c581-119">Type： **Const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c581-119">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4c581-120">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述傳回之網格的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="4c581-120">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="4c581-121">此參數必須直接對應至彈性頂點格式， (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="4c581-121">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="4c581-122">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c581-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c581-123">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4c581-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4c581-124">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，也就是要與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="4c581-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4c581-125">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4c581-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c581-126">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c581-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="4c581-127">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示所建立的網格物件。</span><span class="sxs-lookup"><span data-stu-id="4c581-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c581-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c581-128">Return value</span></span>

<span data-ttu-id="4c581-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c581-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c581-130">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4c581-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c581-131">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="4c581-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c581-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c581-132">Requirements</span></span>



| <span data-ttu-id="4c581-133">需求</span><span class="sxs-lookup"><span data-stu-id="4c581-133">Requirement</span></span> | <span data-ttu-id="4c581-134">值</span><span class="sxs-lookup"><span data-stu-id="4c581-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c581-135">標頭</span><span class="sxs-lookup"><span data-stu-id="4c581-135">Header</span></span><br/>  | <dl> <span data-ttu-id="4c581-136"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c581-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4c581-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c581-137">Library</span></span><br/> | <dl> <span data-ttu-id="4c581-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c581-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c581-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c581-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c581-140">網格函數</span><span class="sxs-lookup"><span data-stu-id="4c581-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="4c581-141">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="4c581-141">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 

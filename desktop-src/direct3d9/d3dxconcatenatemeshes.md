---
description: 將網格群組串連成一個常見的網格。 這個方法可以選擇性地將矩陣轉換套用到每個輸入網格及其材質座標。
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: 'D3DXConcatenateMeshes 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981842"
---
# <a name="d3dxconcatenatemeshes-function"></a><span data-ttu-id="1680a-104">D3DXConcatenateMeshes 函式</span><span class="sxs-lookup"><span data-stu-id="1680a-104">D3DXConcatenateMeshes function</span></span>

<span data-ttu-id="1680a-105">將網格群組串連成一個常見的網格。</span><span class="sxs-lookup"><span data-stu-id="1680a-105">Concatenates a group of meshes into one common mesh.</span></span> <span data-ttu-id="1680a-106">這個方法可以選擇性地將矩陣轉換套用到每個輸入網格及其材質座標。</span><span class="sxs-lookup"><span data-stu-id="1680a-106">This method can optionally apply a matrix transformation to each input mesh and its texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1680a-107">語法</span><span class="sxs-lookup"><span data-stu-id="1680a-107">Syntax</span></span>


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a><span data-ttu-id="1680a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1680a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1680a-109">*ppMeshes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1680a-109">*ppMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-110">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1680a-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1680a-111">輸入網格指標的陣列 (參閱 [**ID3DXMesh**](id3dxmesh.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1680a-111">Array of input mesh pointers (see [**ID3DXMesh**](id3dxmesh.md)).</span></span> <span data-ttu-id="1680a-112">陣列中的元素數目是 NumMeshes。</span><span class="sxs-lookup"><span data-stu-id="1680a-112">The number of elements in the array is NumMeshes.</span></span>

</dd> <dt>

<span data-ttu-id="1680a-113">*NumMeshes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1680a-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1680a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1680a-115">要串連的輸入網格數目。</span><span class="sxs-lookup"><span data-stu-id="1680a-115">Number of input meshes to concatenate.</span></span>

</dd> <dt>

<span data-ttu-id="1680a-116">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1680a-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1680a-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1680a-118">網狀建立選項;這是一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="1680a-118">Mesh creation options; this is a combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags.</span></span> <span data-ttu-id="1680a-119">網格建立選項相當於 [**D3DXCreateMesh**](d3dxcreatemesh.md)所需的 options 參數。</span><span class="sxs-lookup"><span data-stu-id="1680a-119">The mesh creation options are equivalent to the options parameter required by [**D3DXCreateMesh**](d3dxcreatemesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="1680a-120">*pGeomXForms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1680a-120">*pGeomXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-121">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1680a-121">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1680a-122">幾何轉換的選擇性陣列。</span><span class="sxs-lookup"><span data-stu-id="1680a-122">Optional array of geometry transforms.</span></span> <span data-ttu-id="1680a-123">陣列中的元素數目為 NumMeshes;每個元素都是轉換矩陣 (請參閱 [**D3DXMATRIX**](d3dxmatrix.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1680a-123">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="1680a-124">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1680a-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1680a-125">*pTextureXForms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1680a-125">*pTextureXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-126">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1680a-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1680a-127">紋理轉換的選擇性陣列。</span><span class="sxs-lookup"><span data-stu-id="1680a-127">Optional array of texture transforms.</span></span> <span data-ttu-id="1680a-128">陣列中的元素數目為 NumMeshes;每個元素都是轉換矩陣 (請參閱 [**D3DXMATRIX**](d3dxmatrix.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1680a-128">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="1680a-129">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1680a-129">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1680a-130">*pDecl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1680a-130">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-131">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="1680a-131">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="1680a-132">頂點宣告的選擇性指標 (查看 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1680a-132">Optional pointer to a vertex declaration (see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span></span> <span data-ttu-id="1680a-133">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1680a-133">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1680a-134">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1680a-134">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-135">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1680a-135">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1680a-136">用來建立新網格之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="1680a-136">Pointer to a [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the new mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1680a-137">*ppMeshOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1680a-137">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1680a-138">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1680a-138">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1680a-139">所建立之網狀 (的指標位址，請參閱 [**ID3DXMesh**](id3dxmesh.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1680a-139">Address of a pointer to the mesh created (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1680a-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="1680a-140">Return value</span></span>

<span data-ttu-id="1680a-141">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1680a-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1680a-142">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1680a-142">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1680a-143">如果函式失敗，則傳回值可以是下列其中一個： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="1680a-143">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1680a-144">備註</span><span class="sxs-lookup"><span data-stu-id="1680a-144">Remarks</span></span>

<span data-ttu-id="1680a-145">如果在選項網格建立參數中未提供任何 [頂點](vertex-declaration.md) 宣告，方法會產生 submeshes 之所有頂點宣告的聯集，並在必要時升階通道和類型。</span><span class="sxs-lookup"><span data-stu-id="1680a-145">If no [vertex declaration](vertex-declaration.md) is given as part of the Options mesh creation parameter, the method will generate a union of all of the vertex declarations of the submeshes, promoting channels and types if necessary.</span></span> <span data-ttu-id="1680a-146">方法將會從輸入網格的屬性工作表建立屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="1680a-146">The method will create an attribute table from attribute tables of the input meshes.</span></span> <span data-ttu-id="1680a-147">為確保建立屬性工作表，請呼叫 [**Optimize**](id3dxmesh--optimize.md) With 旗標設定為 D3DXMESHOPT \_ COMPACT and D3DXMESHOPT \_ ATTRSORT (參閱 [**D3DXMESHOPT**](./d3dxmeshopt.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1680a-147">To ensure creation of an attribute table, call [**Optimize**](id3dxmesh--optimize.md) with Flags set to D3DXMESHOPT\_COMPACT and D3DXMESHOPT\_ATTRSORT (see [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="1680a-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="1680a-148">Requirements</span></span>



| <span data-ttu-id="1680a-149">需求</span><span class="sxs-lookup"><span data-stu-id="1680a-149">Requirement</span></span> | <span data-ttu-id="1680a-150">值</span><span class="sxs-lookup"><span data-stu-id="1680a-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1680a-151">標頭</span><span class="sxs-lookup"><span data-stu-id="1680a-151">Header</span></span><br/>  | <dl> <span data-ttu-id="1680a-152"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1680a-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1680a-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="1680a-153">Library</span></span><br/> | <dl> <span data-ttu-id="1680a-154"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1680a-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1680a-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1680a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1680a-156">網格函數</span><span class="sxs-lookup"><span data-stu-id="1680a-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

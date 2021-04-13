---
description: 從控制修補程式網格建立網格。
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: 'D3DXCreatePatchMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323320"
---
# <a name="d3dxcreatepatchmesh-function"></a><span data-ttu-id="570d7-103">D3DXCreatePatchMesh 函式</span><span class="sxs-lookup"><span data-stu-id="570d7-103">D3DXCreatePatchMesh function</span></span>

<span data-ttu-id="570d7-104">從控制修補程式網格建立網格。</span><span class="sxs-lookup"><span data-stu-id="570d7-104">Creates a mesh from a control-patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="570d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="570d7-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="570d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="570d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="570d7-107">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="570d7-107">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570d7-108">Type： **Const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***</span><span class="sxs-lookup"><span data-stu-id="570d7-108">Type: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md)\***</span></span>

<span data-ttu-id="570d7-109">修補程式資訊結構。</span><span class="sxs-lookup"><span data-stu-id="570d7-109">Patch information structure.</span></span> <span data-ttu-id="570d7-110">如需詳細資訊，請參閱 [**D3DXPATCHINFO**](d3dxpatchinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="570d7-110">For more information, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="570d7-111">*dwNumPatches* \[在\]</span><span class="sxs-lookup"><span data-stu-id="570d7-111">*dwNumPatches* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570d7-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="570d7-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="570d7-113">修補程式的數目。</span><span class="sxs-lookup"><span data-stu-id="570d7-113">Number of patches.</span></span>

</dd> <dt>

<span data-ttu-id="570d7-114">*dwNumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="570d7-114">*dwNumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570d7-115">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="570d7-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="570d7-116">修補程式中的控制頂點數目。</span><span class="sxs-lookup"><span data-stu-id="570d7-116">Number of control vertices in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="570d7-117">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="570d7-117">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570d7-118">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="570d7-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="570d7-119">未使用的。</span><span class="sxs-lookup"><span data-stu-id="570d7-119">Unused.</span></span> <span data-ttu-id="570d7-120">保留以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="570d7-120">Reserved for later use.</span></span>

</dd> <dt>

<span data-ttu-id="570d7-121">*pDecl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="570d7-121">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570d7-122">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="570d7-122">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="570d7-123">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述傳回之網格的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="570d7-123">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="570d7-124">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="570d7-124">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570d7-125">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="570d7-125">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="570d7-126">建立修補程式網格的裝置指標。</span><span class="sxs-lookup"><span data-stu-id="570d7-126">Pointer the device that creates the patch mesh.</span></span> <span data-ttu-id="570d7-127">請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。</span><span class="sxs-lookup"><span data-stu-id="570d7-127">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="570d7-128">*pPatchMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="570d7-128">*pPatchMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="570d7-129">類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="570d7-129">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="570d7-130">所建立之 [**ID3DXPatchMesh**](id3dxpatchmesh.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="570d7-130">Pointer to the [**ID3DXPatchMesh**](id3dxpatchmesh.md) object that is created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="570d7-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="570d7-131">Return value</span></span>

<span data-ttu-id="570d7-132">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="570d7-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="570d7-133">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="570d7-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="570d7-134">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="570d7-134">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="570d7-135">備註</span><span class="sxs-lookup"><span data-stu-id="570d7-135">Remarks</span></span>

<span data-ttu-id="570d7-136">這個方法會採用輸入修補程式網格，並將其轉換成鑲嵌網格。</span><span class="sxs-lookup"><span data-stu-id="570d7-136">This method takes an input patch mesh and converts it to a tessellated mesh.</span></span> <span data-ttu-id="570d7-137">Patch 網格使用16位索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="570d7-137">Patch meshes use 16-bit index buffers.</span></span> <span data-ttu-id="570d7-138">因此， [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) 的索引為16位。</span><span class="sxs-lookup"><span data-stu-id="570d7-138">Therefore, indices to [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) are 16 bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="570d7-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="570d7-139">Requirements</span></span>



| <span data-ttu-id="570d7-140">需求</span><span class="sxs-lookup"><span data-stu-id="570d7-140">Requirement</span></span> | <span data-ttu-id="570d7-141">值</span><span class="sxs-lookup"><span data-stu-id="570d7-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="570d7-142">標頭</span><span class="sxs-lookup"><span data-stu-id="570d7-142">Header</span></span><br/>  | <dl> <span data-ttu-id="570d7-143"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="570d7-143"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="570d7-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="570d7-144">Library</span></span><br/> | <dl> <span data-ttu-id="570d7-145"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="570d7-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="570d7-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="570d7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570d7-147">網格函數</span><span class="sxs-lookup"><span data-stu-id="570d7-147">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="570d7-148">**D3DXPATCHINFO**</span><span class="sxs-lookup"><span data-stu-id="570d7-148">**D3DXPATCHINFO**</span></span>](d3dxpatchinfo.md)
</dt> </dl>

 

 

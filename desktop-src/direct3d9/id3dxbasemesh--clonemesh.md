---
description: 使用宣告子複製網格。
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'ID3DXBaseMesh：： CloneMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 421b72a080564886a10c187594223fb58a0b69fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974854"
---
# <a name="id3dxbasemeshclonemesh-method"></a><span data-ttu-id="a9444-103">ID3DXBaseMesh：： CloneMesh 方法</span><span class="sxs-lookup"><span data-stu-id="a9444-103">ID3DXBaseMesh::CloneMesh method</span></span>

<span data-ttu-id="a9444-104">使用宣告子複製網格。</span><span class="sxs-lookup"><span data-stu-id="a9444-104">Clones a mesh using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9444-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9444-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="a9444-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9444-107">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9444-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9444-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9444-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9444-109">一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="a9444-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a9444-110">*pDeclaration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9444-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9444-111">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9444-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="a9444-112">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，可指定輸出網格中頂點的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="a9444-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, which specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a9444-113">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9444-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9444-114">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a9444-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a9444-115">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="a9444-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a9444-116">*ppCloneMesh* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="a9444-116">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a9444-117">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9444-117">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a9444-118">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示複製的網格。</span><span class="sxs-lookup"><span data-stu-id="a9444-118">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9444-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9444-119">Return value</span></span>

<span data-ttu-id="a9444-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9444-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9444-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a9444-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a9444-122">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a9444-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9444-123">備註</span><span class="sxs-lookup"><span data-stu-id="a9444-123">Remarks</span></span>

<span data-ttu-id="a9444-124">**ID3DXBaseMesh：： CloneMesh** 是用來重新格式化及變更頂點資料版面配置。</span><span class="sxs-lookup"><span data-stu-id="a9444-124">**ID3DXBaseMesh::CloneMesh** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="a9444-125">這是藉由建立新的網格物件來完成。</span><span class="sxs-lookup"><span data-stu-id="a9444-125">This is done by creating a new mesh object.</span></span> <span data-ttu-id="a9444-126">例如，您可以使用它來為不存在的法線、材質座標、色彩、加權等新增空間。</span><span class="sxs-lookup"><span data-stu-id="a9444-126">For example, use it to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="a9444-127">[**ID3DXBaseMesh：： UpdateSemantics**](id3dxbasemesh--updatesemantics.md) 會使用不同的語義資訊來更新頂點宣告，而不會變更頂點緩衝區的版面配置。</span><span class="sxs-lookup"><span data-stu-id="a9444-127">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="a9444-128">這個方法不會修改頂點緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="a9444-128">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="a9444-129">例如，使用它將3D 紋理座標重定為 binormal 或正切函數，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="a9444-129">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9444-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9444-130">Requirements</span></span>



| <span data-ttu-id="a9444-131">需求</span><span class="sxs-lookup"><span data-stu-id="a9444-131">Requirement</span></span> | <span data-ttu-id="a9444-132">值</span><span class="sxs-lookup"><span data-stu-id="a9444-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9444-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a9444-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a9444-134"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9444-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a9444-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9444-135">Library</span></span><br/> | <dl> <span data-ttu-id="a9444-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9444-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9444-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9444-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9444-138">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="a9444-138">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="a9444-139">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="a9444-139">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="a9444-140">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="a9444-140">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 

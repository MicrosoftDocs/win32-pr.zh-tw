---
description: 使用彈性頂點格式來複製網格 (FVF) 程式碼。
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'ID3DXBaseMesh：： CloneMeshFVF 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976702"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a><span data-ttu-id="b7600-103">ID3DXBaseMesh：： CloneMeshFVF 方法</span><span class="sxs-lookup"><span data-stu-id="b7600-103">ID3DXBaseMesh::CloneMeshFVF method</span></span>

<span data-ttu-id="b7600-104">使用彈性頂點格式來複製網格 (FVF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="b7600-104">Clones a mesh using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7600-105">語法</span><span class="sxs-lookup"><span data-stu-id="b7600-105">Syntax</span></span>


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="b7600-106">參數</span><span class="sxs-lookup"><span data-stu-id="b7600-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7600-107">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7600-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7600-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7600-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7600-109">一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="b7600-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b7600-110">*FVF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7600-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7600-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7600-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7600-112">FVF 碼的組合，指定輸出網格中頂點的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="b7600-112">Combination of FVF codes, which specifies the vertex format for the vertices in the output mesh.</span></span> <span data-ttu-id="b7600-113">如需程式碼的值，請參閱 [D3DFVF](d3dfvf.md)。</span><span class="sxs-lookup"><span data-stu-id="b7600-113">For the values of the codes, see [D3DFVF](d3dfvf.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7600-114">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7600-114">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7600-115">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b7600-115">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b7600-116">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="b7600-116">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b7600-117">*ppCloneMesh* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="b7600-117">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b7600-118">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7600-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b7600-119">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示複製的網格。</span><span class="sxs-lookup"><span data-stu-id="b7600-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7600-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7600-120">Return value</span></span>

<span data-ttu-id="b7600-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7600-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7600-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b7600-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7600-123">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b7600-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7600-124">備註</span><span class="sxs-lookup"><span data-stu-id="b7600-124">Remarks</span></span>

<span data-ttu-id="b7600-125">**ID3DXBaseMesh：： CloneMeshFVF** 是用來重新格式化及變更頂點資料版面配置。</span><span class="sxs-lookup"><span data-stu-id="b7600-125">**ID3DXBaseMesh::CloneMeshFVF** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="b7600-126">這是藉由建立新的網格物件來完成。</span><span class="sxs-lookup"><span data-stu-id="b7600-126">This is done by creating a new mesh object.</span></span> <span data-ttu-id="b7600-127">例如，您可以使用它來新增不存在之法線、材質座標、色彩、權數等的空間。</span><span class="sxs-lookup"><span data-stu-id="b7600-127">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="b7600-128">[**ID3DXBaseMesh：： UpdateSemantics**](id3dxbasemesh--updatesemantics.md) 會使用不同的語義資訊來更新頂點宣告，而不會變更頂點緩衝區的版面配置。</span><span class="sxs-lookup"><span data-stu-id="b7600-128">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="b7600-129">這個方法不會修改頂點緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="b7600-129">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="b7600-130">例如，使用它將3D 紋理座標重定為 binormal 或正切函數，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b7600-130">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7600-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7600-131">Requirements</span></span>



| <span data-ttu-id="b7600-132">需求</span><span class="sxs-lookup"><span data-stu-id="b7600-132">Requirement</span></span> | <span data-ttu-id="b7600-133">值</span><span class="sxs-lookup"><span data-stu-id="b7600-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7600-134">標頭</span><span class="sxs-lookup"><span data-stu-id="b7600-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b7600-135"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7600-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b7600-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7600-136">Library</span></span><br/> | <dl> <span data-ttu-id="b7600-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7600-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7600-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7600-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7600-139">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="b7600-139">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="b7600-140">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="b7600-140">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 

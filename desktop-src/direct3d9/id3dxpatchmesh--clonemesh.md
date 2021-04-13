---
description: 使用指定的頂點宣告來建立新的 patch 網狀。
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh：： CloneMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322707"
---
# <a name="id3dxpatchmeshclonemesh-method"></a><span data-ttu-id="a508e-103">ID3DXPatchMesh：： CloneMesh 方法</span><span class="sxs-lookup"><span data-stu-id="a508e-103">ID3DXPatchMesh::CloneMesh method</span></span>

<span data-ttu-id="a508e-104">使用指定的頂點宣告來建立新的 patch 網狀。</span><span class="sxs-lookup"><span data-stu-id="a508e-104">Creates a new patch mesh with the specified vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="a508e-105">語法</span><span class="sxs-lookup"><span data-stu-id="a508e-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="a508e-106">參數</span><span class="sxs-lookup"><span data-stu-id="a508e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a508e-107">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a508e-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a508e-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a508e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a508e-109">一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，這些旗標會指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="a508e-109">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a508e-110">*pDecl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a508e-110">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a508e-111">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="a508e-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="a508e-112">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，可指定輸出網格中頂點的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="a508e-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements that specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a508e-113">*pMesh* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="a508e-113">*pMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a508e-114">類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a508e-114">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="a508e-115">[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面指標的位址，表示複製的網格。</span><span class="sxs-lookup"><span data-stu-id="a508e-115">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a508e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a508e-116">Return value</span></span>

<span data-ttu-id="a508e-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a508e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a508e-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a508e-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a508e-119">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a508e-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a508e-120">備註</span><span class="sxs-lookup"><span data-stu-id="a508e-120">Remarks</span></span>

<span data-ttu-id="a508e-121">**CloneMesh** 會將頂點緩衝區轉換成新的頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="a508e-121">**CloneMesh** converts the vertex buffer to the new vertex declaration.</span></span> <span data-ttu-id="a508e-122">對原始網格而言，頂點宣告中的專案會設定為0。</span><span class="sxs-lookup"><span data-stu-id="a508e-122">Entries in the vertex declaration that are new to the original mesh are set to 0.</span></span> <span data-ttu-id="a508e-123">如果目前的網格具有連續的，則新的網格也會有連續的。</span><span class="sxs-lookup"><span data-stu-id="a508e-123">If the current mesh has adjacency, the new mesh will also have adjacency.</span></span>

## <a name="requirements"></a><span data-ttu-id="a508e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a508e-124">Requirements</span></span>



| <span data-ttu-id="a508e-125">需求</span><span class="sxs-lookup"><span data-stu-id="a508e-125">Requirement</span></span> | <span data-ttu-id="a508e-126">值</span><span class="sxs-lookup"><span data-stu-id="a508e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a508e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a508e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a508e-128"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="a508e-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a508e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="a508e-129">Library</span></span><br/> | <dl> <span data-ttu-id="a508e-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a508e-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a508e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a508e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a508e-132">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="a508e-132">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

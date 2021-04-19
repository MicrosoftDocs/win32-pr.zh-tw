---
description: 根據目前的矩陣，將軟體外觀套用至目標頂點。
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'ID3DXSkinInfo：： UpdateSkinnedMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000567"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a><span data-ttu-id="6c65b-103">ID3DXSkinInfo：： UpdateSkinnedMesh 方法</span><span class="sxs-lookup"><span data-stu-id="6c65b-103">ID3DXSkinInfo::UpdateSkinnedMesh method</span></span>

<span data-ttu-id="6c65b-104">根據目前的矩陣，將軟體外觀套用至目標頂點。</span><span class="sxs-lookup"><span data-stu-id="6c65b-104">Applies software skinning to the target vertices based on the current matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c65b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c65b-105">Syntax</span></span>


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a><span data-ttu-id="6c65b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c65b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c65b-107">*pBoneTransforms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c65b-107">*pBoneTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c65b-108">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c65b-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6c65b-109">骨骼轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="6c65b-109">Bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6c65b-110">*pBoneInvTransposeTransforms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c65b-110">*pBoneInvTransposeTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c65b-111">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c65b-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6c65b-112">骨骼轉換矩陣的反向變換。</span><span class="sxs-lookup"><span data-stu-id="6c65b-112">Inverse transpose of the bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6c65b-113">*pVerticesSrc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c65b-113">*pVerticesSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c65b-114">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c65b-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c65b-115">包含來源頂點的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="6c65b-115">Pointer to the buffer containing the source vertices.</span></span>

</dd> <dt>

<span data-ttu-id="6c65b-116">*pVerticesDst* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c65b-116">*pVerticesDst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c65b-117">類型： **[ **PVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c65b-117">Type: **[**PVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c65b-118">包含目的地頂點之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="6c65b-118">Pointer to the buffer containing the destination vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c65b-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c65b-119">Return value</span></span>

<span data-ttu-id="6c65b-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c65b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c65b-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6c65b-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c65b-122">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="6c65b-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c65b-123">備註</span><span class="sxs-lookup"><span data-stu-id="6c65b-123">Remarks</span></span>

<span data-ttu-id="6c65b-124">當用來處理具有兩個位置專案的面板頂點時，此方法會將第二個位置元素與骨骼的反函數（而非骨骼本身）搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6c65b-124">When used to skin vertices with two position elements, this method skins the second position element with the inverse of the bone instead of the bone itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c65b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c65b-125">Requirements</span></span>



| <span data-ttu-id="6c65b-126">需求</span><span class="sxs-lookup"><span data-stu-id="6c65b-126">Requirement</span></span> | <span data-ttu-id="6c65b-127">值</span><span class="sxs-lookup"><span data-stu-id="6c65b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c65b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6c65b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6c65b-129"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c65b-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6c65b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c65b-130">Library</span></span><br/> | <dl> <span data-ttu-id="6c65b-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c65b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c65b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c65b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c65b-133">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="6c65b-133">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

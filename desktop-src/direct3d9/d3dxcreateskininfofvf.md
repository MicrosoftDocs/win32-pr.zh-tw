---
description: 使用 (FVF) 程式碼的彈性頂點格式，建立空白的外觀網格物件。
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: 'D3DXCreateSkinInfoFVF 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982014"
---
# <a name="d3dxcreateskininfofvf-function"></a><span data-ttu-id="6c806-103">D3DXCreateSkinInfoFVF 函式</span><span class="sxs-lookup"><span data-stu-id="6c806-103">D3DXCreateSkinInfoFVF function</span></span>

<span data-ttu-id="6c806-104">使用 (FVF) 程式碼的彈性頂點格式，建立空白的外觀網格物件。</span><span class="sxs-lookup"><span data-stu-id="6c806-104">Creates an empty skin mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c806-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c806-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6c806-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c806-107">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c806-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c806-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c806-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c806-109">外觀網格的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="6c806-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6c806-110">*FVF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c806-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c806-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c806-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c806-112">描述所傳回面板網格之頂點格式的 [D3DFVF](d3dfvf.md) 組合。</span><span class="sxs-lookup"><span data-stu-id="6c806-112">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6c806-113">*NumBones* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c806-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c806-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c806-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c806-115">外觀網格的骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="6c806-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6c806-116">*ppSkinInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c806-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c806-117">類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c806-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="6c806-118">[**ID3DXSkinInfo**](id3dxskininfo.md)介面指標的位址，表示所建立的外觀資訊物件。</span><span class="sxs-lookup"><span data-stu-id="6c806-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin information object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c806-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c806-119">Return value</span></span>

<span data-ttu-id="6c806-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c806-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c806-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6c806-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c806-122">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6c806-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c806-123">備註</span><span class="sxs-lookup"><span data-stu-id="6c806-123">Remarks</span></span>

<span data-ttu-id="6c806-124">使用 [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) 來填入這個方法所傳回的空白麵板網格物件。</span><span class="sxs-lookup"><span data-stu-id="6c806-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c806-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c806-125">Requirements</span></span>



| <span data-ttu-id="6c806-126">需求</span><span class="sxs-lookup"><span data-stu-id="6c806-126">Requirement</span></span> | <span data-ttu-id="6c806-127">值</span><span class="sxs-lookup"><span data-stu-id="6c806-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c806-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6c806-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6c806-129"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c806-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6c806-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c806-130">Library</span></span><br/> | <dl> <span data-ttu-id="6c806-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c806-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c806-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c806-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c806-133">網格函數</span><span class="sxs-lookup"><span data-stu-id="6c806-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="6c806-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="6c806-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 

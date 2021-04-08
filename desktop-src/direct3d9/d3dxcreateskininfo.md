---
description: 使用宣告子建立空白的外觀網格物件。
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: 'D3DXCreateSkinInfo 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83ee214eb997414e113256060dbe59d3cd47d1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853995"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="bbc1f-103">D3DXCreateSkinInfo 函式</span><span class="sxs-lookup"><span data-stu-id="bbc1f-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="bbc1f-104">使用宣告子建立空白的外觀網格物件。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc1f-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbc1f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bbc1f-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbc1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc1f-107">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbc1f-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc1f-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbc1f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbc1f-109">外觀網格的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bbc1f-110">*pDeclaration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbc1f-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc1f-111">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="bbc1f-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="bbc1f-112">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述傳回之網格的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bbc1f-113">*NumBones* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbc1f-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc1f-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbc1f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbc1f-115">外觀網格的骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bbc1f-116">*ppSkinInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bbc1f-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc1f-117">類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbc1f-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="bbc1f-118">[**ID3DXSkinInfo**](id3dxskininfo.md)介面指標的位址，表示所建立的面板網格物件。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc1f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbc1f-119">Return value</span></span>

<span data-ttu-id="bbc1f-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bbc1f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bbc1f-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bbc1f-122">如果函式失敗，則傳回值可以是： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc1f-123">備註</span><span class="sxs-lookup"><span data-stu-id="bbc1f-123">Remarks</span></span>

<span data-ttu-id="bbc1f-124">使用 [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) 來填入這個方法所傳回的空白麵板網格物件。</span><span class="sxs-lookup"><span data-stu-id="bbc1f-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc1f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbc1f-125">Requirements</span></span>



| <span data-ttu-id="bbc1f-126">需求</span><span class="sxs-lookup"><span data-stu-id="bbc1f-126">Requirement</span></span> | <span data-ttu-id="bbc1f-127">值</span><span class="sxs-lookup"><span data-stu-id="bbc1f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc1f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bbc1f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bbc1f-129"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc1f-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bbc1f-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="bbc1f-130">Library</span></span><br/> | <dl> <span data-ttu-id="bbc1f-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbc1f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bbc1f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbc1f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc1f-133">網格函數</span><span class="sxs-lookup"><span data-stu-id="bbc1f-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="bbc1f-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="bbc1f-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 

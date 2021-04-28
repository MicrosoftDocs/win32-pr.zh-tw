---
description: D3DXATTRIBUTERANGE 結構-儲存屬性資料表專案。
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: 'D3DXATTRIBUTERANGE 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7dfdf15f653fda77b1ca8c9a14cd32decee9658e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116006"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="f7ee6-103">D3DXATTRIBUTERANGE 結構</span><span class="sxs-lookup"><span data-stu-id="f7ee6-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="f7ee6-104">儲存屬性資料表專案。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ee6-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7ee6-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="f7ee6-106">成員</span><span class="sxs-lookup"><span data-stu-id="f7ee6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f7ee6-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="f7ee6-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7ee6-109">屬性資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f7ee6-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="f7ee6-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7ee6-112">開始臉部。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="f7ee6-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="f7ee6-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7ee6-115">臉部計數。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="f7ee6-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="f7ee6-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7ee6-118">正在啟動頂點。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="f7ee6-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="f7ee6-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7ee6-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7ee6-121">頂點計數。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7ee6-122">備註</span><span class="sxs-lookup"><span data-stu-id="f7ee6-122">Remarks</span></span>

<span data-ttu-id="f7ee6-123">屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="f7ee6-124">此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時 (AttribId) 繪製指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="f7ee6-125">LPD3DXATTRIBUTERANGE 型別定義為 **D3DXATTRIBUTERANGE** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f7ee6-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="f7ee6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7ee6-126">Requirements</span></span>



| <span data-ttu-id="f7ee6-127">需求</span><span class="sxs-lookup"><span data-stu-id="f7ee6-127">Requirement</span></span> | <span data-ttu-id="f7ee6-128">值</span><span class="sxs-lookup"><span data-stu-id="f7ee6-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ee6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f7ee6-129">Header</span></span><br/> | <dl> <span data-ttu-id="f7ee6-130"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7ee6-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7ee6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7ee6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ee6-132">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="f7ee6-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

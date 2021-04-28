---
description: D3DX10_ATTRIBUTE_RANGE 結構-儲存屬性資料表專案。
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: 'D3DX10_ATTRIBUTE_RANGE 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094366"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="ec7df-103">D3DX10 \_ 屬性 \_ 範圍結構</span><span class="sxs-lookup"><span data-stu-id="ec7df-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="ec7df-104">儲存屬性資料表專案。</span><span class="sxs-lookup"><span data-stu-id="ec7df-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7df-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec7df-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="ec7df-106">成員</span><span class="sxs-lookup"><span data-stu-id="ec7df-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec7df-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="ec7df-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="ec7df-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec7df-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec7df-109">屬性資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec7df-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ec7df-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="ec7df-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="ec7df-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec7df-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec7df-112">開始臉部。</span><span class="sxs-lookup"><span data-stu-id="ec7df-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="ec7df-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="ec7df-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="ec7df-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec7df-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec7df-115">臉部計數。</span><span class="sxs-lookup"><span data-stu-id="ec7df-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="ec7df-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="ec7df-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="ec7df-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec7df-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec7df-118">正在啟動頂點。</span><span class="sxs-lookup"><span data-stu-id="ec7df-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="ec7df-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="ec7df-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="ec7df-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec7df-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec7df-121">頂點計數。</span><span class="sxs-lookup"><span data-stu-id="ec7df-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec7df-122">備註</span><span class="sxs-lookup"><span data-stu-id="ec7df-122">Remarks</span></span>

<span data-ttu-id="ec7df-123">屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。</span><span class="sxs-lookup"><span data-stu-id="ec7df-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="ec7df-124">此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時 (AttribId) 繪製指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec7df-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="ec7df-125">LPD3DX \_ 屬性 \_ 範圍類型定義為 D3DX \_ 屬性 \_ 範圍結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ec7df-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="ec7df-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec7df-126">Requirements</span></span>



| <span data-ttu-id="ec7df-127">需求</span><span class="sxs-lookup"><span data-stu-id="ec7df-127">Requirement</span></span> | <span data-ttu-id="ec7df-128">值</span><span class="sxs-lookup"><span data-stu-id="ec7df-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7df-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ec7df-129">Header</span></span><br/> | <dl> <span data-ttu-id="ec7df-130"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec7df-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec7df-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec7df-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7df-132">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="ec7df-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

---
description: D3DXSHPRTSPLITMESHCLUSTERDATA 結構
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: 'D3DXSHPRTSPLITMESHCLUSTERDATA 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993872"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a><span data-ttu-id="6dfed-103">D3DXSHPRTSPLITMESHCLUSTERDATA 結構</span><span class="sxs-lookup"><span data-stu-id="6dfed-103">D3DXSHPRTSPLITMESHCLUSTERDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfed-104">語法</span><span class="sxs-lookup"><span data-stu-id="6dfed-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a><span data-ttu-id="6dfed-105">成員</span><span class="sxs-lookup"><span data-stu-id="6dfed-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="6dfed-106">**uVertStart**</span><span class="sxs-lookup"><span data-stu-id="6dfed-106">**uVertStart**</span></span>
</dt> <dd>

<span data-ttu-id="6dfed-107">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfed-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6dfed-108">重新對應頂點陣列的初始頂點。</span><span class="sxs-lookup"><span data-stu-id="6dfed-108">Initial vertex into remapped vertex array.</span></span>

</dd> <dt>

<span data-ttu-id="6dfed-109">**uVertLength**</span><span class="sxs-lookup"><span data-stu-id="6dfed-109">**uVertLength**</span></span>
</dt> <dd>

<span data-ttu-id="6dfed-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfed-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6dfed-111">此 supercluster 中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="6dfed-111">Number of vertices in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="6dfed-112">**uFaceStart**</span><span class="sxs-lookup"><span data-stu-id="6dfed-112">**uFaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="6dfed-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfed-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6dfed-114">臉部陣列的初始索引。</span><span class="sxs-lookup"><span data-stu-id="6dfed-114">Initial index into face array.</span></span>

</dd> <dt>

<span data-ttu-id="6dfed-115">**uFaceLength**</span><span class="sxs-lookup"><span data-stu-id="6dfed-115">**uFaceLength**</span></span>
</dt> <dd>

<span data-ttu-id="6dfed-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfed-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6dfed-117">此 supercluster 中的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="6dfed-117">Number of faces in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="6dfed-118">**uClusterStart**</span><span class="sxs-lookup"><span data-stu-id="6dfed-118">**uClusterStart**</span></span>
</dt> <dd>

<span data-ttu-id="6dfed-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfed-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6dfed-120">群集陣列的初始索引。</span><span class="sxs-lookup"><span data-stu-id="6dfed-120">Initial index into cluster array.</span></span>

</dd> <dt>

<span data-ttu-id="6dfed-121">**uClusterLength**</span><span class="sxs-lookup"><span data-stu-id="6dfed-121">**uClusterLength**</span></span>
</dt> <dd>

<span data-ttu-id="6dfed-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfed-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6dfed-123">這個 supercluster 陣列中的群集數目。</span><span class="sxs-lookup"><span data-stu-id="6dfed-123">Number of clusters in this supercluster array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dfed-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dfed-124">Requirements</span></span>



| <span data-ttu-id="6dfed-125">需求</span><span class="sxs-lookup"><span data-stu-id="6dfed-125">Requirement</span></span> | <span data-ttu-id="6dfed-126">值</span><span class="sxs-lookup"><span data-stu-id="6dfed-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfed-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6dfed-127">Header</span></span><br/> | <dl> <span data-ttu-id="6dfed-128"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dfed-128"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dfed-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dfed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfed-130">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="6dfed-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="6dfed-131">**D3DXSHPRTCompSplitMeshSC**</span><span class="sxs-lookup"><span data-stu-id="6dfed-131">**D3DXSHPRTCompSplitMeshSC**</span></span>](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 

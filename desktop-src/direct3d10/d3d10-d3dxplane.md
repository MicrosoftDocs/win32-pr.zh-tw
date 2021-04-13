---
description: 描述平面。
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: 'D3DXPLANE 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323239"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="0b12a-103">D3DXPLANE 結構 (D3DX10Math .h) </span><span class="sxs-lookup"><span data-stu-id="0b12a-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="0b12a-104">描述平面。</span><span class="sxs-lookup"><span data-stu-id="0b12a-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b12a-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b12a-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="0b12a-106">成員</span><span class="sxs-lookup"><span data-stu-id="0b12a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0b12a-107">**的**</span><span class="sxs-lookup"><span data-stu-id="0b12a-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="0b12a-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b12a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0b12a-109">一般平面方程式中裁剪平面的係數。</span><span class="sxs-lookup"><span data-stu-id="0b12a-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0b12a-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="0b12a-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0b12a-111">**b**</span><span class="sxs-lookup"><span data-stu-id="0b12a-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="0b12a-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b12a-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0b12a-113">一般平面方程式中裁剪平面的 b 係數。</span><span class="sxs-lookup"><span data-stu-id="0b12a-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0b12a-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="0b12a-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0b12a-115">**c**</span><span class="sxs-lookup"><span data-stu-id="0b12a-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="0b12a-116">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b12a-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0b12a-117">一般平面方程式中裁剪平面的 c 係數。</span><span class="sxs-lookup"><span data-stu-id="0b12a-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0b12a-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="0b12a-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0b12a-119">**d**</span><span class="sxs-lookup"><span data-stu-id="0b12a-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="0b12a-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b12a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0b12a-121">一般平面方程式中裁剪平面的 d 係數。</span><span class="sxs-lookup"><span data-stu-id="0b12a-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0b12a-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="0b12a-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b12a-123">備註</span><span class="sxs-lookup"><span data-stu-id="0b12a-123">Remarks</span></span>

<span data-ttu-id="0b12a-124">**D3DXPLANE** 結構的成員採用一般平面方程式的形式。</span><span class="sxs-lookup"><span data-stu-id="0b12a-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="0b12a-125">它們符合一般平面方程式，因此 ax + by + cz + dw = 0。</span><span class="sxs-lookup"><span data-stu-id="0b12a-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b12a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b12a-126">Requirements</span></span>



| <span data-ttu-id="0b12a-127">需求</span><span class="sxs-lookup"><span data-stu-id="0b12a-127">Requirement</span></span> | <span data-ttu-id="0b12a-128">值</span><span class="sxs-lookup"><span data-stu-id="0b12a-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b12a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0b12a-129">Header</span></span><br/> | <dl> <span data-ttu-id="0b12a-130"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b12a-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b12a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b12a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b12a-132">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="0b12a-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

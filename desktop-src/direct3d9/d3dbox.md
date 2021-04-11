---
description: 定義磁片區。
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: 'D3DBOX 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196207"
---
# <a name="d3dbox-structure"></a><span data-ttu-id="1b738-103">D3DBOX 結構</span><span class="sxs-lookup"><span data-stu-id="1b738-103">D3DBOX structure</span></span>

<span data-ttu-id="1b738-104">定義磁片區。</span><span class="sxs-lookup"><span data-stu-id="1b738-104">Defines a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b738-105">語法</span><span class="sxs-lookup"><span data-stu-id="1b738-105">Syntax</span></span>


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a><span data-ttu-id="1b738-106">成員</span><span class="sxs-lookup"><span data-stu-id="1b738-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b738-107">**離開**</span><span class="sxs-lookup"><span data-stu-id="1b738-107">**Left**</span></span>
</dt> <dd>

<span data-ttu-id="1b738-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b738-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b738-109">方塊左邊的位置（X 軸）。</span><span class="sxs-lookup"><span data-stu-id="1b738-109">Position of the left side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1b738-110">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="1b738-110">**Top**</span></span>
</dt> <dd>

<span data-ttu-id="1b738-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b738-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b738-112">Y 軸上方塊頂端的位置。</span><span class="sxs-lookup"><span data-stu-id="1b738-112">Position of the top of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1b738-113">**對**</span><span class="sxs-lookup"><span data-stu-id="1b738-113">**Right**</span></span>
</dt> <dd>

<span data-ttu-id="1b738-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b738-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b738-115">X 軸右邊方塊的位置。</span><span class="sxs-lookup"><span data-stu-id="1b738-115">Position of the right side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1b738-116">**下層**</span><span class="sxs-lookup"><span data-stu-id="1b738-116">**Bottom**</span></span>
</dt> <dd>

<span data-ttu-id="1b738-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b738-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b738-118">Y 軸上方塊底部的位置。</span><span class="sxs-lookup"><span data-stu-id="1b738-118">Position of the bottom of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1b738-119">**Front**</span><span class="sxs-lookup"><span data-stu-id="1b738-119">**Front**</span></span>
</dt> <dd>

<span data-ttu-id="1b738-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b738-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b738-121">Z 軸上方塊前端的位置。</span><span class="sxs-lookup"><span data-stu-id="1b738-121">Position of the front of the box on the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1b738-122">**上一步**</span><span class="sxs-lookup"><span data-stu-id="1b738-122">**Back**</span></span>
</dt> <dd>

<span data-ttu-id="1b738-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b738-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b738-124">Z 軸上方塊背面的位置。</span><span class="sxs-lookup"><span data-stu-id="1b738-124">Position of the back of the box on the z-axis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b738-125">備註</span><span class="sxs-lookup"><span data-stu-id="1b738-125">Remarks</span></span>

<span data-ttu-id="1b738-126">**D3DBOX** 包含左、上和前邊緣;但是，不包含右邊、下邊緣和後端邊緣。</span><span class="sxs-lookup"><span data-stu-id="1b738-126">**D3DBOX** includes the left, top, and front edges; however, the right, bottom, and back edges are not included.</span></span> <span data-ttu-id="1b738-127">例如，一個全100單元的方塊，並從0開始 (因此，包括最多和包含99的點) 會以0代表左邊的成員，並針對右邊的成員以100的值表示。</span><span class="sxs-lookup"><span data-stu-id="1b738-127">For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member.</span></span> <span data-ttu-id="1b738-128">請注意，不會針對右邊的成員使用99的值。</span><span class="sxs-lookup"><span data-stu-id="1b738-128">Note that a value of 99 is not used for the Right member.</span></span>

<span data-ttu-id="1b738-129">針對 **D3DBOX** 觀察到的順序限制是由左到右、由上到下，以及前端。</span><span class="sxs-lookup"><span data-stu-id="1b738-129">The restrictions on side ordering observed for **D3DBOX** are left to right, top to bottom, and front to back.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b738-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b738-130">Requirements</span></span>



| <span data-ttu-id="1b738-131">需求</span><span class="sxs-lookup"><span data-stu-id="1b738-131">Requirement</span></span> | <span data-ttu-id="1b738-132">值</span><span class="sxs-lookup"><span data-stu-id="1b738-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b738-133">標頭</span><span class="sxs-lookup"><span data-stu-id="1b738-133">Header</span></span><br/> | <dl> <span data-ttu-id="1b738-134"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b738-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b738-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b738-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b738-136">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="1b738-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

---
description: 定義矩形。
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: 'D3DRECT 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696676"
---
# <a name="d3drect-structure"></a><span data-ttu-id="941d1-103">D3DRECT 結構</span><span class="sxs-lookup"><span data-stu-id="941d1-103">D3DRECT structure</span></span>

<span data-ttu-id="941d1-104">定義矩形。</span><span class="sxs-lookup"><span data-stu-id="941d1-104">Defines a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="941d1-105">語法</span><span class="sxs-lookup"><span data-stu-id="941d1-105">Syntax</span></span>


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a><span data-ttu-id="941d1-106">成員</span><span class="sxs-lookup"><span data-stu-id="941d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="941d1-107">**x1**</span><span class="sxs-lookup"><span data-stu-id="941d1-107">**x1**</span></span>
</dt> <dd>

<span data-ttu-id="941d1-108">類型： **[ **LONG**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="941d1-108">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="941d1-109">矩形左上角的 X 座標。</span><span class="sxs-lookup"><span data-stu-id="941d1-109">The x-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="941d1-110">**y1**</span><span class="sxs-lookup"><span data-stu-id="941d1-110">**y1**</span></span>
</dt> <dd>

<span data-ttu-id="941d1-111">類型： **[ **LONG**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="941d1-111">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="941d1-112">矩形左上角的 Y 座標。</span><span class="sxs-lookup"><span data-stu-id="941d1-112">The y-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="941d1-113">**x2**</span><span class="sxs-lookup"><span data-stu-id="941d1-113">**x2**</span></span>
</dt> <dd>

<span data-ttu-id="941d1-114">類型： **[ **LONG**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="941d1-114">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="941d1-115">矩形右下角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="941d1-115">The x-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="941d1-116">**y2**</span><span class="sxs-lookup"><span data-stu-id="941d1-116">**y2**</span></span>
</dt> <dd>

<span data-ttu-id="941d1-117">類型： **[ **LONG**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="941d1-117">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="941d1-118">矩形右下角的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="941d1-118">The y-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="941d1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="941d1-119">Requirements</span></span>



| <span data-ttu-id="941d1-120">需求</span><span class="sxs-lookup"><span data-stu-id="941d1-120">Requirement</span></span> | <span data-ttu-id="941d1-121">值</span><span class="sxs-lookup"><span data-stu-id="941d1-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="941d1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="941d1-122">Header</span></span><br/> | <dl> <span data-ttu-id="941d1-123"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="941d1-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="941d1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="941d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="941d1-125">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="941d1-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="941d1-126">**清楚**</span><span class="sxs-lookup"><span data-stu-id="941d1-126">**Clear**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 

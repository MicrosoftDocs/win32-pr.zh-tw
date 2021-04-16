---
description: 定義常數，以描述支援的陰影模式。
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: 'D3DSHADEMODE 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322792"
---
# <a name="d3dshademode-enumeration"></a><span data-ttu-id="bfcb7-103">D3DSHADEMODE 列舉</span><span class="sxs-lookup"><span data-stu-id="bfcb7-103">D3DSHADEMODE enumeration</span></span>

<span data-ttu-id="bfcb7-104">定義常數，以描述支援的陰影模式。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-104">Defines constants that describe the supported shading modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcb7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfcb7-105">Syntax</span></span>


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a><span data-ttu-id="bfcb7-106">常數</span><span class="sxs-lookup"><span data-stu-id="bfcb7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bfcb7-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ 平面**</span><span class="sxs-lookup"><span data-stu-id="bfcb7-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE\_FLAT**</span></span>
</dt> <dd>

<span data-ttu-id="bfcb7-108">平面陰影模式。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-108">Flat shading mode.</span></span> <span data-ttu-id="bfcb7-109">三角形中第一個頂點的色彩和反射元件是用來判斷臉部的色彩和反射元件。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-109">The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face.</span></span> <span data-ttu-id="bfcb7-110">這些色彩在三角形中保持不變;也就是說，它們不是插補。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-110">These colors remain constant across the triangle; that is, they are not interpolated.</span></span> <span data-ttu-id="bfcb7-111">反射 Alpha 是插補。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-111">The specular alpha is interpolated.</span></span> <span data-ttu-id="bfcb7-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="bfcb7-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**</span><span class="sxs-lookup"><span data-stu-id="bfcb7-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE\_GOURAUD**</span></span>
</dt> <dd>

<span data-ttu-id="bfcb7-114">Gouraud 網底模式。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-114">Gouraud shading mode.</span></span> <span data-ttu-id="bfcb7-115">臉部的色彩和反射元件是由三角形的所有頂點之間的線性插補所決定。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-115">The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices.</span></span>

</dd> <dt>

<span data-ttu-id="bfcb7-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**</span><span class="sxs-lookup"><span data-stu-id="bfcb7-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE\_PHONG**</span></span>
</dt> <dd>

<span data-ttu-id="bfcb7-117">不支援。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bfcb7-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bfcb7-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="bfcb7-119">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="bfcb7-120">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="bfcb7-121">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfcb7-122">備註</span><span class="sxs-lookup"><span data-stu-id="bfcb7-122">Remarks</span></span>

<span data-ttu-id="bfcb7-123">一般陰影模式之三角形的第一個頂點會以下列方式定義。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-123">The first vertex of a triangle for flat shading mode is defined in the following manner.</span></span>

-   <span data-ttu-id="bfcb7-124">若為三角形清單，則為三角形的第一個頂點 i \* 3。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-124">For a triangle list, the first vertex of the triangle i is i \* 3.</span></span>
-   <span data-ttu-id="bfcb7-125">若為三角形帶，則三角形的第一個頂點是頂點 i。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-125">For a triangle strip, the first vertex of the triangle i is vertex i.</span></span>
-   <span data-ttu-id="bfcb7-126">若為三角形風扇，則三角形的第一個頂點是頂點 i + 1。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-126">For a triangle fan, the first vertex of the triangle i is vertex i + 1.</span></span>

<span data-ttu-id="bfcb7-127">此列舉類型的成員會定義 D3DRS SHADEMODE 轉譯狀態的數值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bfcb7-127">The members of this enumerated type define the vales for the D3DRS\_SHADEMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfcb7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfcb7-128">Requirements</span></span>



| <span data-ttu-id="bfcb7-129">需求</span><span class="sxs-lookup"><span data-stu-id="bfcb7-129">Requirement</span></span> | <span data-ttu-id="bfcb7-130">值</span><span class="sxs-lookup"><span data-stu-id="bfcb7-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcb7-131">標頭</span><span class="sxs-lookup"><span data-stu-id="bfcb7-131">Header</span></span><br/> | <dl> <span data-ttu-id="bfcb7-132"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb7-132"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcb7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfcb7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcb7-134">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="bfcb7-134">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="bfcb7-135">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="bfcb7-135">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 

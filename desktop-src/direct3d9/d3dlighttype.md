---
description: 定義光源類型。
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: 'D3DLIGHTTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976715"
---
# <a name="d3dlighttype-enumeration"></a><span data-ttu-id="3b8e7-103">D3DLIGHTTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="3b8e7-103">D3DLIGHTTYPE enumeration</span></span>

<span data-ttu-id="3b8e7-104">定義光源類型。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-104">Defines the light type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b8e7-105">Syntax</span></span>


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a><span data-ttu-id="3b8e7-106">常數</span><span class="sxs-lookup"><span data-stu-id="3b8e7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3b8e7-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT \_ 點**</span><span class="sxs-lookup"><span data-stu-id="3b8e7-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="3b8e7-108">Light 是點來源。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-108">Light is a point source.</span></span> <span data-ttu-id="3b8e7-109">光線在空間中有一個位置，而 radiates 光的方向。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-109">The light has a position in space and radiates light in all directions.</span></span>

</dd> <dt>

<span data-ttu-id="3b8e7-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="3b8e7-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="3b8e7-111">Light 是焦點來源。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-111">Light is a spotlight source.</span></span> <span data-ttu-id="3b8e7-112">這種光線就像點燈，只不過照明僅限於錐形。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-112">This light is like a point light, except that the illumination is limited to a cone.</span></span> <span data-ttu-id="3b8e7-113">此光線類型具有方向和數個其他參數，可決定所產生之錐形的形狀。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-113">This light type has a direction and several other parameters that determine the shape of the cone it produces.</span></span> <span data-ttu-id="3b8e7-114">如需這些參數的詳細資訊，請參閱 [**D3DLIGHT9**](d3dlight9.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-114">For information about these parameters, see the [**D3DLIGHT9**](d3dlight9.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3b8e7-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ 方向**</span><span class="sxs-lookup"><span data-stu-id="3b8e7-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT\_DIRECTIONAL**</span></span>
</dt> <dd>

<span data-ttu-id="3b8e7-116">Light 是方向性光源。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-116">Light is a directional light source.</span></span> <span data-ttu-id="3b8e7-117">這相當於使用無限距離的點光源來源。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-117">This is equivalent to using a point light source at an infinite distance.</span></span>

</dd> <dt>

<span data-ttu-id="3b8e7-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b8e7-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3b8e7-119">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3b8e7-120">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3b8e7-121">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b8e7-122">備註</span><span class="sxs-lookup"><span data-stu-id="3b8e7-122">Remarks</span></span>

<span data-ttu-id="3b8e7-123">方向光源的速度比點光源稍微快一點，但點燈看起來比較好。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-123">Directional lights are slightly faster than point light sources, but point lights look a little better.</span></span> <span data-ttu-id="3b8e7-124">聚光燈提供有趣的視覺效果，但需要花費很多時間來計算。</span><span class="sxs-lookup"><span data-stu-id="3b8e7-124">Spotlights offer interesting visual effects but are computationally time-consuming.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8e7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b8e7-125">Requirements</span></span>



| <span data-ttu-id="3b8e7-126">需求</span><span class="sxs-lookup"><span data-stu-id="3b8e7-126">Requirement</span></span> | <span data-ttu-id="3b8e7-127">值</span><span class="sxs-lookup"><span data-stu-id="3b8e7-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8e7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3b8e7-128">Header</span></span><br/> | <dl> <span data-ttu-id="3b8e7-129"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8e7-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8e7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b8e7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8e7-131">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="3b8e7-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="3b8e7-132">**D3DLIGHT9**</span><span class="sxs-lookup"><span data-stu-id="3b8e7-132">**D3DLIGHT9**</span></span>](d3dlight9.md)
</dt> </dl>

 

 





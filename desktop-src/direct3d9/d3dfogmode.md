---
description: 定義描述霧化模式的常數。
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: 'D3DFOGMODE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323072"
---
# <a name="d3dfogmode-enumeration"></a><span data-ttu-id="2f398-103">D3DFOGMODE 列舉</span><span class="sxs-lookup"><span data-stu-id="2f398-103">D3DFOGMODE enumeration</span></span>

<span data-ttu-id="2f398-104">定義描述霧化模式的常數。</span><span class="sxs-lookup"><span data-stu-id="2f398-104">Defines constants that describe the fog mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f398-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f398-105">Syntax</span></span>


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a><span data-ttu-id="2f398-106">常數</span><span class="sxs-lookup"><span data-stu-id="2f398-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f398-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ 無**</span><span class="sxs-lookup"><span data-stu-id="2f398-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="2f398-108">沒有霧化效果。</span><span class="sxs-lookup"><span data-stu-id="2f398-108">No fog effect.</span></span>

</dd> <dt>

<span data-ttu-id="2f398-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ EXP**</span><span class="sxs-lookup"><span data-stu-id="2f398-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG\_EXP**</span></span>
</dt> <dd>

<span data-ttu-id="2f398-110">根據下列公式，會以指數方式增強霧化效果。</span><span class="sxs-lookup"><span data-stu-id="2f398-110">Fog effect intensifies exponentially, according to the following formula.</span></span>

![霧化的公式-效果強度](images/fogexp.png)

</dd> <dt>

<span data-ttu-id="2f398-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**</span><span class="sxs-lookup"><span data-stu-id="2f398-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG\_EXP2**</span></span>
</dt> <dd>

<span data-ttu-id="2f398-113">霧化效果會根據下列公式，以指數方式從距離的平方開始增強。</span><span class="sxs-lookup"><span data-stu-id="2f398-113">Fog effect intensifies exponentially with the square of the distance, according to the following formula.</span></span>

![以距離為基礎的霧化效果濃度公式](images/fogexp2.png)

</dd> <dt>

<span data-ttu-id="2f398-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ 線性**</span><span class="sxs-lookup"><span data-stu-id="2f398-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="2f398-116">您可以根據下列公式，開始與結束點之間的霧化效果呈線性增加。</span><span class="sxs-lookup"><span data-stu-id="2f398-116">Fog effect intensifies linearly between the start and end points, according to the following formula.</span></span>

![以開始和結束點為基礎之霧化效果濃度的公式](images/fogliner.png)

<span data-ttu-id="2f398-118">這是目前唯一支援的霧化模式。</span><span class="sxs-lookup"><span data-stu-id="2f398-118">This is the only fog mode currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="2f398-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2f398-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2f398-120">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="2f398-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2f398-121">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="2f398-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2f398-122">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="2f398-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f398-123">備註</span><span class="sxs-lookup"><span data-stu-id="2f398-123">Remarks</span></span>

<span data-ttu-id="2f398-124">D3DRS \_ FOGTABLEMODE 和 D3DRS FOGVERTEXMODE 轉譯狀態會使用這個列舉型別中的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2f398-124">The values in this enumerated type are used by the D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states.</span></span>

<span data-ttu-id="2f398-125">霧化可視為可見度的量值：霧化方程式所產生的霧化值越低，物件就越不可見。</span><span class="sxs-lookup"><span data-stu-id="2f398-125">Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f398-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f398-126">Requirements</span></span>



| <span data-ttu-id="2f398-127">需求</span><span class="sxs-lookup"><span data-stu-id="2f398-127">Requirement</span></span> | <span data-ttu-id="2f398-128">值</span><span class="sxs-lookup"><span data-stu-id="2f398-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f398-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2f398-129">Header</span></span><br/> | <dl> <span data-ttu-id="2f398-130"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f398-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f398-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f398-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f398-132">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="2f398-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2f398-133">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="2f398-133">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 

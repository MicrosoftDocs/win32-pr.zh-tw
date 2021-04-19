---
description: 定義方程式中描述曲線的變數程度。
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: 'D3DDEGREETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000580"
---
# <a name="d3ddegreetype-enumeration"></a><span data-ttu-id="63962-103">D3DDEGREETYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="63962-103">D3DDEGREETYPE enumeration</span></span>

<span data-ttu-id="63962-104">定義方程式中描述曲線的變數程度。</span><span class="sxs-lookup"><span data-stu-id="63962-104">Defines the degree of the variables in the equation that describes a curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="63962-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63962-105">Syntax</span></span>


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a><span data-ttu-id="63962-106">常數</span><span class="sxs-lookup"><span data-stu-id="63962-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="63962-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ 線性**</span><span class="sxs-lookup"><span data-stu-id="63962-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="63962-108">曲線會以第一個順序的變數來描述。</span><span class="sxs-lookup"><span data-stu-id="63962-108">Curve is described by variables of first order.</span></span>

</dd> <dt>

<span data-ttu-id="63962-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ 二次**</span><span class="sxs-lookup"><span data-stu-id="63962-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE\_QUADRATIC**</span></span>
</dt> <dd>

<span data-ttu-id="63962-110">曲線會以第二個順序的變數來描述。</span><span class="sxs-lookup"><span data-stu-id="63962-110">Curve is described by variables of second order.</span></span>

</dd> <dt>

<span data-ttu-id="63962-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ 立方**</span><span class="sxs-lookup"><span data-stu-id="63962-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE\_CUBIC**</span></span>
</dt> <dd>

<span data-ttu-id="63962-112">曲線會以第三個順序的變數來描述。</span><span class="sxs-lookup"><span data-stu-id="63962-112">Curve is described by variables of third order.</span></span>

</dd> <dt>

<span data-ttu-id="63962-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ QUINTIC**</span><span class="sxs-lookup"><span data-stu-id="63962-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE\_QUINTIC**</span></span>
</dt> <dd>

<span data-ttu-id="63962-114">曲線會以第四個順序的變數來描述。</span><span class="sxs-lookup"><span data-stu-id="63962-114">Curve is described by variables of fourth order.</span></span>

</dd> <dt>

<span data-ttu-id="63962-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="63962-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="63962-116">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="63962-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="63962-117">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="63962-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="63962-118">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="63962-118">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63962-119">備註</span><span class="sxs-lookup"><span data-stu-id="63962-119">Remarks</span></span>

<span data-ttu-id="63962-120">此列舉中的值是用來描述矩形和三角形修補程式所使用的曲線。</span><span class="sxs-lookup"><span data-stu-id="63962-120">The values in this enumeration are used to describe the curves used by rectangle and triangle patches.</span></span> <span data-ttu-id="63962-121">如需詳細資訊，請參閱 D3DRS \_ CULLMODE。</span><span class="sxs-lookup"><span data-stu-id="63962-121">For more information, see D3DRS\_CULLMODE.</span></span>

## <a name="requirements"></a><span data-ttu-id="63962-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="63962-122">Requirements</span></span>



| <span data-ttu-id="63962-123">需求</span><span class="sxs-lookup"><span data-stu-id="63962-123">Requirement</span></span> | <span data-ttu-id="63962-124">值</span><span class="sxs-lookup"><span data-stu-id="63962-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63962-125">標頭</span><span class="sxs-lookup"><span data-stu-id="63962-125">Header</span></span><br/> | <dl> <span data-ttu-id="63962-126"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="63962-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63962-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63962-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63962-128">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="63962-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="63962-129">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="63962-129">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="63962-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="63962-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 

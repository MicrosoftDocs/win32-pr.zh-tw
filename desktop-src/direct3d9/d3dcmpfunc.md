---
description: 定義支援的比較函數。
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: 'D3DCMPFUNC 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853975"
---
# <a name="d3dcmpfunc-enumeration"></a><span data-ttu-id="fc560-103">D3DCMPFUNC 列舉</span><span class="sxs-lookup"><span data-stu-id="fc560-103">D3DCMPFUNC enumeration</span></span>

<span data-ttu-id="fc560-104">定義支援的比較函數。</span><span class="sxs-lookup"><span data-stu-id="fc560-104">Defines the supported compare functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc560-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc560-105">Syntax</span></span>


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a><span data-ttu-id="fc560-106">常數</span><span class="sxs-lookup"><span data-stu-id="fc560-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fc560-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ 永不**</span><span class="sxs-lookup"><span data-stu-id="fc560-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP\_NEVER**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-108">一律會使測試失敗。</span><span class="sxs-lookup"><span data-stu-id="fc560-108">Always fail the test.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ LESS**</span><span class="sxs-lookup"><span data-stu-id="fc560-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP\_LESS**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-110">如果值小於目前圖元的值，則接受新的圖元。</span><span class="sxs-lookup"><span data-stu-id="fc560-110">Accept the new pixel if its value is less than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ 相等**</span><span class="sxs-lookup"><span data-stu-id="fc560-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-112">如果圖元值等於目前圖元的值，則接受新的圖元。</span><span class="sxs-lookup"><span data-stu-id="fc560-112">Accept the new pixel if its value equals the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**</span><span class="sxs-lookup"><span data-stu-id="fc560-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP\_LESSEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-114">如果值小於或等於目前圖元的值，則接受新的圖元。</span><span class="sxs-lookup"><span data-stu-id="fc560-114">Accept the new pixel if its value is less than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ 更大**</span><span class="sxs-lookup"><span data-stu-id="fc560-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP\_GREATER**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-116">如果其值大於目前圖元的值，則接受新的圖元。</span><span class="sxs-lookup"><span data-stu-id="fc560-116">Accept the new pixel if its value is greater than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NOTEQUAL**</span><span class="sxs-lookup"><span data-stu-id="fc560-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP\_NOTEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-118">如果其值不等於目前圖元的值，則接受新的圖元。</span><span class="sxs-lookup"><span data-stu-id="fc560-118">Accept the new pixel if its value does not equal the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ GREATEREQUAL**</span><span class="sxs-lookup"><span data-stu-id="fc560-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP\_GREATEREQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-120">如果其值大於或等於目前圖元的值，則接受新的圖元。</span><span class="sxs-lookup"><span data-stu-id="fc560-120">Accept the new pixel if its value is greater than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**\_一律 D3DCMP**</span><span class="sxs-lookup"><span data-stu-id="fc560-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP\_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-122">一律傳遞測試。</span><span class="sxs-lookup"><span data-stu-id="fc560-122">Always pass the test.</span></span>

</dd> <dt>

<span data-ttu-id="fc560-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc560-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="fc560-124">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="fc560-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="fc560-125">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="fc560-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="fc560-126">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="fc560-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc560-127">備註</span><span class="sxs-lookup"><span data-stu-id="fc560-127">Remarks</span></span>

<span data-ttu-id="fc560-128">此列舉型別中的值會定義 D3DRS \_ ZFUNC、D3DRS \_ ALPHAFUNC 和 D3DRS STENCILFUNC 轉譯狀態的支援比較函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fc560-128">The values in this enumerated type define the supported compare functions for the D3DRS\_ZFUNC, D3DRS\_ALPHAFUNC, and D3DRS\_STENCILFUNC render states.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc560-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc560-129">Requirements</span></span>



| <span data-ttu-id="fc560-130">需求</span><span class="sxs-lookup"><span data-stu-id="fc560-130">Requirement</span></span> | <span data-ttu-id="fc560-131">值</span><span class="sxs-lookup"><span data-stu-id="fc560-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc560-132">標頭</span><span class="sxs-lookup"><span data-stu-id="fc560-132">Header</span></span><br/> | <dl> <span data-ttu-id="fc560-133"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc560-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc560-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc560-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc560-135">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="fc560-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="fc560-136">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="fc560-136">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 

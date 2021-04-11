---
description: 定義目前鑲嵌模式為離散或連續模式。
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: 'D3DPATCHEDGESTYLE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854015"
---
# <a name="d3dpatchedgestyle-enumeration"></a><span data-ttu-id="cedf0-103">D3DPATCHEDGESTYLE 列舉</span><span class="sxs-lookup"><span data-stu-id="cedf0-103">D3DPATCHEDGESTYLE enumeration</span></span>

<span data-ttu-id="cedf0-104">定義目前鑲嵌模式為離散或連續模式。</span><span class="sxs-lookup"><span data-stu-id="cedf0-104">Defines whether the current tessellation mode is discrete or continuous.</span></span>

## <a name="syntax"></a><span data-ttu-id="cedf0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cedf0-105">Syntax</span></span>


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a><span data-ttu-id="cedf0-106">常數</span><span class="sxs-lookup"><span data-stu-id="cedf0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cedf0-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ 離散**</span><span class="sxs-lookup"><span data-stu-id="cedf0-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="cedf0-108">離散邊緣樣式。</span><span class="sxs-lookup"><span data-stu-id="cedf0-108">Discrete edge style.</span></span> <span data-ttu-id="cedf0-109">在獨立模式中，您可以指定 float 鑲嵌式，但是它會被截斷為整數。</span><span class="sxs-lookup"><span data-stu-id="cedf0-109">In discrete mode, you can specify float tessellation but it will be truncated to integers.</span></span>

</dd> <dt>

<span data-ttu-id="cedf0-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ 連續**</span><span class="sxs-lookup"><span data-stu-id="cedf0-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE\_CONTINUOUS**</span></span>
</dt> <dd>

<span data-ttu-id="cedf0-111">連續邊緣樣式。</span><span class="sxs-lookup"><span data-stu-id="cedf0-111">Continuous edge style.</span></span> <span data-ttu-id="cedf0-112">在連續模式中，會將鑲嵌指定為浮點值，而這些值可以平滑地改變，以減少「即將推出」的構件。</span><span class="sxs-lookup"><span data-stu-id="cedf0-112">In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts.</span></span>

</dd> <dt>

<span data-ttu-id="cedf0-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cedf0-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="cedf0-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="cedf0-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="cedf0-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="cedf0-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="cedf0-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="cedf0-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cedf0-117">備註</span><span class="sxs-lookup"><span data-stu-id="cedf0-117">Remarks</span></span>

<span data-ttu-id="cedf0-118">請注意，連續鑲嵌會針對相同的鑲嵌值產生與離散不同的鑲嵌模式 (這線上框模式) 更為明顯。</span><span class="sxs-lookup"><span data-stu-id="cedf0-118">Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode).</span></span> <span data-ttu-id="cedf0-119">因此，4.0 連續與4個離散不同。</span><span class="sxs-lookup"><span data-stu-id="cedf0-119">Thus, 4.0 continuous is not the same as 4 discrete.</span></span>

## <a name="requirements"></a><span data-ttu-id="cedf0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="cedf0-120">Requirements</span></span>



| <span data-ttu-id="cedf0-121">需求</span><span class="sxs-lookup"><span data-stu-id="cedf0-121">Requirement</span></span> | <span data-ttu-id="cedf0-122">值</span><span class="sxs-lookup"><span data-stu-id="cedf0-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cedf0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cedf0-123">Header</span></span><br/> | <dl> <span data-ttu-id="cedf0-124"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="cedf0-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cedf0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cedf0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cedf0-126">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="cedf0-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 





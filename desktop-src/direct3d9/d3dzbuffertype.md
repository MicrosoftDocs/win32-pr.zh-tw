---
description: 定義描述深度緩衝區格式的常數。
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: 'D3DZBUFFERTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985889"
---
# <a name="d3dzbuffertype-enumeration"></a><span data-ttu-id="40d53-103">D3DZBUFFERTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="40d53-103">D3DZBUFFERTYPE enumeration</span></span>

<span data-ttu-id="40d53-104">定義描述深度緩衝區格式的常數。</span><span class="sxs-lookup"><span data-stu-id="40d53-104">Defines constants that describe depth-buffer formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d53-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40d53-105">Syntax</span></span>


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a><span data-ttu-id="40d53-106">常數</span><span class="sxs-lookup"><span data-stu-id="40d53-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="40d53-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="40d53-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="40d53-108">停用深度緩衝。</span><span class="sxs-lookup"><span data-stu-id="40d53-108">Disable depth buffering.</span></span>

</dd> <dt>

<span data-ttu-id="40d53-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="40d53-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB\_TRUE**</span></span>
</dt> <dd>

<span data-ttu-id="40d53-110">啟用 z 緩衝。</span><span class="sxs-lookup"><span data-stu-id="40d53-110">Enable z-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="40d53-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ USEW**</span><span class="sxs-lookup"><span data-stu-id="40d53-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB\_USEW**</span></span>
</dt> <dd>

<span data-ttu-id="40d53-112">啟用 w-緩衝。</span><span class="sxs-lookup"><span data-stu-id="40d53-112">Enable w-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="40d53-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="40d53-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="40d53-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="40d53-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="40d53-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="40d53-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="40d53-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="40d53-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40d53-117">備註</span><span class="sxs-lookup"><span data-stu-id="40d53-117">Remarks</span></span>

<span data-ttu-id="40d53-118">此列舉類型的成員會搭配 D3DRS ZENABLE 轉譯 \_ 狀態使用。</span><span class="sxs-lookup"><span data-stu-id="40d53-118">Members of this enumerated type are used with the D3DRS\_ZENABLE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d53-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="40d53-119">Requirements</span></span>



| <span data-ttu-id="40d53-120">需求</span><span class="sxs-lookup"><span data-stu-id="40d53-120">Requirement</span></span> | <span data-ttu-id="40d53-121">值</span><span class="sxs-lookup"><span data-stu-id="40d53-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40d53-122">標頭</span><span class="sxs-lookup"><span data-stu-id="40d53-122">Header</span></span><br/> | <dl> <span data-ttu-id="40d53-123"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="40d53-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40d53-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40d53-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d53-125">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="40d53-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="40d53-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="40d53-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 

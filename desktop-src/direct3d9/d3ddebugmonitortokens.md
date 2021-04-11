---
description: 定義 debug 監視器權杖。
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: 'D3DDEBUGMONITORTOKENS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946062"
---
# <a name="d3ddebugmonitortokens-enumeration"></a><span data-ttu-id="0cf2d-103">D3DDEBUGMONITORTOKENS 列舉</span><span class="sxs-lookup"><span data-stu-id="0cf2d-103">D3DDEBUGMONITORTOKENS enumeration</span></span>

<span data-ttu-id="0cf2d-104">定義 debug 監視器權杖。</span><span class="sxs-lookup"><span data-stu-id="0cf2d-104">Defines the debug monitor tokens.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf2d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cf2d-105">Syntax</span></span>


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a><span data-ttu-id="0cf2d-106">常數</span><span class="sxs-lookup"><span data-stu-id="0cf2d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0cf2d-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="0cf2d-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0cf2d-108">啟用 [調試] 監視器。</span><span class="sxs-lookup"><span data-stu-id="0cf2d-108">Enable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="0cf2d-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT \_ DISABLE**</span><span class="sxs-lookup"><span data-stu-id="0cf2d-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0cf2d-110">停用調試監視器。</span><span class="sxs-lookup"><span data-stu-id="0cf2d-110">Disable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="0cf2d-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cf2d-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0cf2d-112">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="0cf2d-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0cf2d-113">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="0cf2d-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0cf2d-114">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="0cf2d-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cf2d-115">備註</span><span class="sxs-lookup"><span data-stu-id="0cf2d-115">Remarks</span></span>

<span data-ttu-id="0cf2d-116">此列舉型別中的值是由 D3DRS DEBUGMONITORTOKEN 轉譯狀態所使用 \_ ，而且只與 debug 組建相關。</span><span class="sxs-lookup"><span data-stu-id="0cf2d-116">The values in this enumerated type are used by the D3DRS\_DEBUGMONITORTOKEN render state and are only relevant for debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf2d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cf2d-117">Requirements</span></span>



| <span data-ttu-id="0cf2d-118">需求</span><span class="sxs-lookup"><span data-stu-id="0cf2d-118">Requirement</span></span> | <span data-ttu-id="0cf2d-119">值</span><span class="sxs-lookup"><span data-stu-id="0cf2d-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf2d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0cf2d-120">Header</span></span><br/> | <dl> <span data-ttu-id="0cf2d-121"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cf2d-121"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cf2d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cf2d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf2d-123">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="0cf2d-123">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0cf2d-124">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="0cf2d-124">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 

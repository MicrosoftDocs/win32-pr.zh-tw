---
description: 用來取得回呼資訊的旗標。
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: 'D3DXCALLBACK_SEARCH_FLAGS 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035368"
---
# <a name="d3dxcallback_search_flags-enumeration"></a><span data-ttu-id="890ea-103">D3DXCALLBACK \_ 搜尋 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="890ea-103">D3DXCALLBACK\_SEARCH\_FLAGS enumeration</span></span>

<span data-ttu-id="890ea-104">用來取得回呼資訊的旗標。</span><span class="sxs-lookup"><span data-stu-id="890ea-104">Flags used to obtain callback information.</span></span>

## <a name="syntax"></a><span data-ttu-id="890ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="890ea-105">Syntax</span></span>


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="890ea-106">常數</span><span class="sxs-lookup"><span data-stu-id="890ea-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="890ea-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK \_ 搜尋 \_ 排除 \_ 初始 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="890ea-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK\_SEARCH\_EXCLUDING\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="890ea-108">從搜尋中排除位於初始位置的回呼。</span><span class="sxs-lookup"><span data-stu-id="890ea-108">Exclude callbacks located at the initial position from the search.</span></span>

</dd> <dt>

<span data-ttu-id="890ea-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**在 \_ \_ \_ 初始位置後方 \_ D3DXCALLBACK 搜尋**</span><span class="sxs-lookup"><span data-stu-id="890ea-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK\_SEARCH\_BEHIND\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="890ea-110">反轉回呼搜尋方向。</span><span class="sxs-lookup"><span data-stu-id="890ea-110">Reverse the callback search direction.</span></span>

</dd> <dt>

<span data-ttu-id="890ea-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ 搜尋 \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="890ea-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK\_SEARCH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="890ea-112">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="890ea-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="890ea-113">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="890ea-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="890ea-114">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="890ea-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="890ea-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="890ea-115">Requirements</span></span>



| <span data-ttu-id="890ea-116">需求</span><span class="sxs-lookup"><span data-stu-id="890ea-116">Requirement</span></span> | <span data-ttu-id="890ea-117">值</span><span class="sxs-lookup"><span data-stu-id="890ea-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="890ea-118">標頭</span><span class="sxs-lookup"><span data-stu-id="890ea-118">Header</span></span><br/> | <dl> <span data-ttu-id="890ea-119"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="890ea-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="890ea-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="890ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="890ea-121">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="890ea-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





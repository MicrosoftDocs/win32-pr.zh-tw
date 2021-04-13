---
description: 描述動畫控制器可以做為索引鍵的事件種類。
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: 'D3DXEVENT_TYPE 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322928"
---
# <a name="d3dxevent_type-enumeration"></a><span data-ttu-id="e952c-103">D3DXEVENT \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="e952c-103">D3DXEVENT\_TYPE enumeration</span></span>

<span data-ttu-id="e952c-104">描述動畫控制器可以做為索引鍵的事件種類。</span><span class="sxs-lookup"><span data-stu-id="e952c-104">Describes the type of events that can be keyed by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e952c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e952c-105">Syntax</span></span>


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="e952c-106">常數</span><span class="sxs-lookup"><span data-stu-id="e952c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e952c-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT \_ TRACKSPEED**</span><span class="sxs-lookup"><span data-stu-id="e952c-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT\_TRACKSPEED**</span></span>
</dt> <dd>

<span data-ttu-id="e952c-108">追蹤速度。</span><span class="sxs-lookup"><span data-stu-id="e952c-108">Track speed.</span></span>

</dd> <dt>

<span data-ttu-id="e952c-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT \_ TRACKWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="e952c-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT\_TRACKWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="e952c-110">追蹤權數。</span><span class="sxs-lookup"><span data-stu-id="e952c-110">Track weight.</span></span>

</dd> <dt>

<span data-ttu-id="e952c-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="e952c-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT\_TRACKPOSITION**</span></span>
</dt> <dd>

<span data-ttu-id="e952c-112">追蹤位置。</span><span class="sxs-lookup"><span data-stu-id="e952c-112">Track position.</span></span>

</dd> <dt>

<span data-ttu-id="e952c-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT \_ TRACKENABLE**</span><span class="sxs-lookup"><span data-stu-id="e952c-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT\_TRACKENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="e952c-114">啟用旗標。</span><span class="sxs-lookup"><span data-stu-id="e952c-114">Enable flag.</span></span>

</dd> <dt>

<span data-ttu-id="e952c-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT \_ PRIORITYBLEND**</span><span class="sxs-lookup"><span data-stu-id="e952c-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT\_PRIORITYBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="e952c-116">優先權 blend 值。</span><span class="sxs-lookup"><span data-stu-id="e952c-116">Priority blend value.</span></span>

</dd> <dt>

<span data-ttu-id="e952c-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e952c-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e952c-118">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="e952c-118">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e952c-119">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="e952c-119">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e952c-120">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="e952c-120">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e952c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e952c-121">Requirements</span></span>



| <span data-ttu-id="e952c-122">需求</span><span class="sxs-lookup"><span data-stu-id="e952c-122">Requirement</span></span> | <span data-ttu-id="e952c-123">值</span><span class="sxs-lookup"><span data-stu-id="e952c-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e952c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e952c-124">Header</span></span><br/> | <dl> <span data-ttu-id="e952c-125"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="e952c-125"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e952c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e952c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e952c-127">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="e952c-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





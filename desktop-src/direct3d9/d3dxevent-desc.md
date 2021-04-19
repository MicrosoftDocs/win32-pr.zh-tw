---
description: 描述動畫事件。
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: 'D3DXEVENT_DESC 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982882"
---
# <a name="d3dxevent_desc-structure"></a><span data-ttu-id="388d3-103">D3DXEVENT \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="388d3-103">D3DXEVENT\_DESC structure</span></span>

<span data-ttu-id="388d3-104">描述動畫事件。</span><span class="sxs-lookup"><span data-stu-id="388d3-104">Describes an animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="388d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="388d3-105">Syntax</span></span>


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a><span data-ttu-id="388d3-106">成員</span><span class="sxs-lookup"><span data-stu-id="388d3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="388d3-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="388d3-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-108">類型： **[ **D3DXEVENT \_ 類型**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-108">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-109">事件種類，如 [**D3DXEVENT \_ 類型**](./d3dxevent-type.md)中所定義。</span><span class="sxs-lookup"><span data-stu-id="388d3-109">Event type, as defined in [**D3DXEVENT\_TYPE**](./d3dxevent-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="388d3-110">**Track**</span><span class="sxs-lookup"><span data-stu-id="388d3-110">**Track**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-112">事件追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="388d3-112">Event track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="388d3-113">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="388d3-113">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-114">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-115">全球時間的事件開始時間。</span><span class="sxs-lookup"><span data-stu-id="388d3-115">Start time of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="388d3-116">**有效期間**</span><span class="sxs-lookup"><span data-stu-id="388d3-116">**Duration**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-117">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-117">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-118">全球時間事件的持續時間。</span><span class="sxs-lookup"><span data-stu-id="388d3-118">Duration of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="388d3-119">**轉換**</span><span class="sxs-lookup"><span data-stu-id="388d3-119">**Transition**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-120">類型： **[ **D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-120">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-121">事件的轉換樣式，如 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)中所定義。</span><span class="sxs-lookup"><span data-stu-id="388d3-121">Transition style of the event, as defined in [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="388d3-122">**Weight**</span><span class="sxs-lookup"><span data-stu-id="388d3-122">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-124">追蹤事件的加權。</span><span class="sxs-lookup"><span data-stu-id="388d3-124">Track weight for the event.</span></span>

</dd> <dt>

<span data-ttu-id="388d3-125">**速度**</span><span class="sxs-lookup"><span data-stu-id="388d3-125">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-127">追蹤事件的速度。</span><span class="sxs-lookup"><span data-stu-id="388d3-127">Track speed for the event.</span></span>

</dd> <dt>

<span data-ttu-id="388d3-128">**位置**</span><span class="sxs-lookup"><span data-stu-id="388d3-128">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-129">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-129">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-130">追蹤事件的位置。</span><span class="sxs-lookup"><span data-stu-id="388d3-130">Track position for the event.</span></span>

</dd> <dt>

<span data-ttu-id="388d3-131">**啟用**</span><span class="sxs-lookup"><span data-stu-id="388d3-131">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="388d3-132">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="388d3-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="388d3-133">啟用旗標。</span><span class="sxs-lookup"><span data-stu-id="388d3-133">Enable flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="388d3-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="388d3-134">Requirements</span></span>



| <span data-ttu-id="388d3-135">需求</span><span class="sxs-lookup"><span data-stu-id="388d3-135">Requirement</span></span> | <span data-ttu-id="388d3-136">值</span><span class="sxs-lookup"><span data-stu-id="388d3-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="388d3-137">標頭</span><span class="sxs-lookup"><span data-stu-id="388d3-137">Header</span></span><br/> | <dl> <span data-ttu-id="388d3-138"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="388d3-138"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="388d3-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="388d3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="388d3-140">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="388d3-140">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

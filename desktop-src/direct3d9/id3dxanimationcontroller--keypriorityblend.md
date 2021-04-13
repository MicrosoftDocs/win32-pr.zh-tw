---
description: 設定指定動畫播放軌的混合事件索引鍵。
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController：： KeyPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322680"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a><span data-ttu-id="e8020-103">ID3DXAnimationController：： KeyPriorityBlend 方法</span><span class="sxs-lookup"><span data-stu-id="e8020-103">ID3DXAnimationController::KeyPriorityBlend method</span></span>

<span data-ttu-id="e8020-104">設定指定動畫播放軌的混合事件索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e8020-104">Sets blending event keys for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8020-105">語法</span><span class="sxs-lookup"><span data-stu-id="e8020-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="e8020-106">參數</span><span class="sxs-lookup"><span data-stu-id="e8020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8020-107">*NewBlendWeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8020-107">*NewBlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8020-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8020-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8020-109">介於0和1之間的數位，用來結合追蹤。</span><span class="sxs-lookup"><span data-stu-id="e8020-109">Number between 0 and 1 that is used to blend tracks together.</span></span>

</dd> <dt>

<span data-ttu-id="e8020-110">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8020-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8020-111">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8020-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8020-112">開始 blend 的全球時間。</span><span class="sxs-lookup"><span data-stu-id="e8020-112">Global time to start the blend.</span></span>

</dd> <dt>

<span data-ttu-id="e8020-113">*持續時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8020-113">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8020-114">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8020-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8020-115">Blend 的全球時間持續時間。</span><span class="sxs-lookup"><span data-stu-id="e8020-115">Global time duration of the blend.</span></span>

</dd> <dt>

<span data-ttu-id="e8020-116">*轉換* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8020-116">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8020-117">類型： **[ **D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e8020-117">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="e8020-118">指定用於 blend 期間的轉換類型。</span><span class="sxs-lookup"><span data-stu-id="e8020-118">Specifies the transition type used for the duration of the blend.</span></span> <span data-ttu-id="e8020-119">請參閱 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)。</span><span class="sxs-lookup"><span data-stu-id="e8020-119">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8020-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8020-120">Return value</span></span>

<span data-ttu-id="e8020-121">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="e8020-121">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="e8020-122">優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="e8020-122">Event handle to the priority blend event.</span></span> <span data-ttu-id="e8020-123">如果有一或多個輸入參數無效，或沒有可用的事件，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e8020-123">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8020-124">備註</span><span class="sxs-lookup"><span data-stu-id="e8020-124">Remarks</span></span>

<span data-ttu-id="e8020-125">動畫控制器會以三個階段來混合：低優先順序的軌跡先混合，高優先順序的軌跡則是混合的第二個，然後兩者的結果都是混合的。</span><span class="sxs-lookup"><span data-stu-id="e8020-125">The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8020-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8020-126">Requirements</span></span>



| <span data-ttu-id="e8020-127">需求</span><span class="sxs-lookup"><span data-stu-id="e8020-127">Requirement</span></span> | <span data-ttu-id="e8020-128">值</span><span class="sxs-lookup"><span data-stu-id="e8020-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8020-129">標頭</span><span class="sxs-lookup"><span data-stu-id="e8020-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e8020-130"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8020-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e8020-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="e8020-131">Library</span></span><br/> | <dl> <span data-ttu-id="e8020-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8020-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8020-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8020-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8020-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e8020-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="e8020-135">**SetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="e8020-135">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 

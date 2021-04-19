---
description: 設定可變更動畫播放軌權數的事件索引鍵。將多個追蹤結合在一起時，權數會用來做為乘數。
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController：： KeyTrackWeight 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997416"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a><span data-ttu-id="95ef1-103">ID3DXAnimationController：： KeyTrackWeight 方法</span><span class="sxs-lookup"><span data-stu-id="95ef1-103">ID3DXAnimationController::KeyTrackWeight method</span></span>

<span data-ttu-id="95ef1-104">設定可變更動畫播放軌權數的事件索引鍵。將多個追蹤結合在一起時，權數會用來做為乘數。</span><span class="sxs-lookup"><span data-stu-id="95ef1-104">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ef1-105">語法</span><span class="sxs-lookup"><span data-stu-id="95ef1-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="95ef1-106">參數</span><span class="sxs-lookup"><span data-stu-id="95ef1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ef1-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95ef1-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ef1-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95ef1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95ef1-109">要修改之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="95ef1-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="95ef1-110">*NewWeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95ef1-110">*NewWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ef1-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95ef1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95ef1-112">曲目的新加權。</span><span class="sxs-lookup"><span data-stu-id="95ef1-112">New weight of the track.</span></span>

</dd> <dt>

<span data-ttu-id="95ef1-113">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95ef1-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ef1-114">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95ef1-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95ef1-115">全域時間索引鍵。</span><span class="sxs-lookup"><span data-stu-id="95ef1-115">Global time key.</span></span> <span data-ttu-id="95ef1-116">指定將進行變更的全域時間。</span><span class="sxs-lookup"><span data-stu-id="95ef1-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="95ef1-117">*持續時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95ef1-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ef1-118">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95ef1-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95ef1-119">轉換時間，指定順利完成轉換所需要的時間。</span><span class="sxs-lookup"><span data-stu-id="95ef1-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="95ef1-120">*轉換* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95ef1-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ef1-121">類型： **[ **D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="95ef1-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="95ef1-122">指定用於在加權之間轉換的轉換類型。</span><span class="sxs-lookup"><span data-stu-id="95ef1-122">Specifies the transition type used for transitioning between weights.</span></span> <span data-ttu-id="95ef1-123">請參閱 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)。</span><span class="sxs-lookup"><span data-stu-id="95ef1-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ef1-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="95ef1-124">Return value</span></span>

<span data-ttu-id="95ef1-125">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="95ef1-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="95ef1-126">優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="95ef1-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="95ef1-127">如果有一或多個輸入參數無效，或沒有可用的事件，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="95ef1-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ef1-128">備註</span><span class="sxs-lookup"><span data-stu-id="95ef1-128">Remarks</span></span>

<span data-ttu-id="95ef1-129">權數的使用方式就像乘數，用來決定要將這份追蹤與其他曲目結合在一起的程度。</span><span class="sxs-lookup"><span data-stu-id="95ef1-129">The weight is used like a multiplier to determine how much of this track to blend together with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ef1-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="95ef1-130">Requirements</span></span>



| <span data-ttu-id="95ef1-131">需求</span><span class="sxs-lookup"><span data-stu-id="95ef1-131">Requirement</span></span> | <span data-ttu-id="95ef1-132">值</span><span class="sxs-lookup"><span data-stu-id="95ef1-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95ef1-133">標頭</span><span class="sxs-lookup"><span data-stu-id="95ef1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="95ef1-134"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="95ef1-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="95ef1-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="95ef1-135">Library</span></span><br/> | <dl> <span data-ttu-id="95ef1-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="95ef1-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95ef1-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95ef1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ef1-138">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="95ef1-138">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

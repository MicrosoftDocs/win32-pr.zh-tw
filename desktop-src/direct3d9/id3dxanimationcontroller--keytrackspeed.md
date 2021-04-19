---
description: 設定可變更動畫播放軌播放速率的事件索引鍵。
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'ID3DXAnimationController：： KeyTrackSpeed 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993918"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a><span data-ttu-id="1bca1-103">ID3DXAnimationController：： KeyTrackSpeed 方法</span><span class="sxs-lookup"><span data-stu-id="1bca1-103">ID3DXAnimationController::KeyTrackSpeed method</span></span>

<span data-ttu-id="1bca1-104">設定可變更動畫播放軌播放速率的事件索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1bca1-104">Sets an event key that changes the rate of play of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bca1-105">語法</span><span class="sxs-lookup"><span data-stu-id="1bca1-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="1bca1-106">參數</span><span class="sxs-lookup"><span data-stu-id="1bca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bca1-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bca1-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bca1-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bca1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bca1-109">要修改之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bca1-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="1bca1-110">*NewSpeed* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bca1-110">*NewSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bca1-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bca1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bca1-112">動畫播放軌的新速度。</span><span class="sxs-lookup"><span data-stu-id="1bca1-112">New speed of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="1bca1-113">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bca1-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bca1-114">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bca1-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bca1-115">全域時間索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1bca1-115">Global time key.</span></span> <span data-ttu-id="1bca1-116">指定將進行變更的全域時間。</span><span class="sxs-lookup"><span data-stu-id="1bca1-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="1bca1-117">*持續時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bca1-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bca1-118">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bca1-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bca1-119">轉換時間，指定順利完成轉換所需要的時間。</span><span class="sxs-lookup"><span data-stu-id="1bca1-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="1bca1-120">*轉換* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bca1-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bca1-121">類型： **[ **D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="1bca1-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="1bca1-122">指定用於轉換速度的轉換類型。</span><span class="sxs-lookup"><span data-stu-id="1bca1-122">Specifies the transition type used for transitioning between speeds.</span></span> <span data-ttu-id="1bca1-123">請參閱 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)。</span><span class="sxs-lookup"><span data-stu-id="1bca1-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bca1-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bca1-124">Return value</span></span>

<span data-ttu-id="1bca1-125">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="1bca1-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="1bca1-126">優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="1bca1-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="1bca1-127">如果有一或多個輸入參數無效，或沒有可用的事件，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1bca1-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bca1-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bca1-128">Requirements</span></span>



| <span data-ttu-id="1bca1-129">需求</span><span class="sxs-lookup"><span data-stu-id="1bca1-129">Requirement</span></span> | <span data-ttu-id="1bca1-130">值</span><span class="sxs-lookup"><span data-stu-id="1bca1-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bca1-131">標頭</span><span class="sxs-lookup"><span data-stu-id="1bca1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1bca1-132"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bca1-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1bca1-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="1bca1-133">Library</span></span><br/> | <dl> <span data-ttu-id="1bca1-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bca1-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bca1-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bca1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bca1-136">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="1bca1-136">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

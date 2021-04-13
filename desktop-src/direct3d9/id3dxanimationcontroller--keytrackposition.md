---
description: 設定事件索引鍵，以變更動畫播放軌的當地時間。
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'ID3DXAnimationController：： KeyTrackPosition 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323180"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a><span data-ttu-id="77bbf-103">ID3DXAnimationController：： KeyTrackPosition 方法</span><span class="sxs-lookup"><span data-stu-id="77bbf-103">ID3DXAnimationController::KeyTrackPosition method</span></span>

<span data-ttu-id="77bbf-104">設定事件索引鍵，以變更動畫播放軌的當地時間。</span><span class="sxs-lookup"><span data-stu-id="77bbf-104">Sets an event key that changes the local time of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="77bbf-105">語法</span><span class="sxs-lookup"><span data-stu-id="77bbf-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="77bbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="77bbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77bbf-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77bbf-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77bbf-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77bbf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77bbf-109">要修改之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="77bbf-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="77bbf-110">*NewPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77bbf-110">*NewPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77bbf-111">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77bbf-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77bbf-112">動畫播放軌的新當地時間。</span><span class="sxs-lookup"><span data-stu-id="77bbf-112">New local time of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="77bbf-113">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77bbf-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77bbf-114">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77bbf-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77bbf-115">全域時間索引鍵。</span><span class="sxs-lookup"><span data-stu-id="77bbf-115">Global time key.</span></span> <span data-ttu-id="77bbf-116">指定將進行變更的全域時間。</span><span class="sxs-lookup"><span data-stu-id="77bbf-116">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77bbf-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="77bbf-117">Return value</span></span>

<span data-ttu-id="77bbf-118">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="77bbf-118">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="77bbf-119">優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="77bbf-119">Event handle to the priority blend event.</span></span> <span data-ttu-id="77bbf-120">如果 Track 無效，或如果沒有可用的事件，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="77bbf-120">**NULL** is returned if Track is invalid, or if no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="77bbf-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="77bbf-121">Requirements</span></span>



| <span data-ttu-id="77bbf-122">需求</span><span class="sxs-lookup"><span data-stu-id="77bbf-122">Requirement</span></span> | <span data-ttu-id="77bbf-123">值</span><span class="sxs-lookup"><span data-stu-id="77bbf-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77bbf-124">標頭</span><span class="sxs-lookup"><span data-stu-id="77bbf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="77bbf-125"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="77bbf-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="77bbf-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="77bbf-126">Library</span></span><br/> | <dl> <span data-ttu-id="77bbf-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="77bbf-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="77bbf-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77bbf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77bbf-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="77bbf-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

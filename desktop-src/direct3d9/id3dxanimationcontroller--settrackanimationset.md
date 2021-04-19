---
description: 將動畫集套用至指定的曲目。
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController：： SetTrackAnimationSet 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988207"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a><span data-ttu-id="ce7ff-103">ID3DXAnimationController：： SetTrackAnimationSet 方法</span><span class="sxs-lookup"><span data-stu-id="ce7ff-103">ID3DXAnimationController::SetTrackAnimationSet method</span></span>

<span data-ttu-id="ce7ff-104">將動畫集套用至指定的曲目。</span><span class="sxs-lookup"><span data-stu-id="ce7ff-104">Applies the animation set to the specified track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7ff-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce7ff-105">Syntax</span></span>


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="ce7ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="ce7ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce7ff-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce7ff-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7ff-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce7ff-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce7ff-109">套用動畫集之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce7ff-109">Identifier of the track to which the animation set is applied.</span></span>

</dd> <dt>

<span data-ttu-id="ce7ff-110">*pAnimSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce7ff-110">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7ff-111">類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="ce7ff-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="ce7ff-112">要加入至曲目的 [**ID3DXAnimationSet**](id3dxanimationset.md) 動畫指標。</span><span class="sxs-lookup"><span data-stu-id="ce7ff-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to be added to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce7ff-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce7ff-113">Return value</span></span>

<span data-ttu-id="ce7ff-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce7ff-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce7ff-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ce7ff-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ce7ff-116">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ce7ff-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce7ff-117">備註</span><span class="sxs-lookup"><span data-stu-id="ce7ff-117">Remarks</span></span>

<span data-ttu-id="ce7ff-118">這個方法會將動畫設定為混合的指定追蹤。</span><span class="sxs-lookup"><span data-stu-id="ce7ff-118">This method sets the animation set to the specified track for mixing.</span></span> <span data-ttu-id="ce7ff-119">當呼叫 [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) 時，每個追蹤的動畫集都會根據追蹤加權和速度進行混合。</span><span class="sxs-lookup"><span data-stu-id="ce7ff-119">The animation set for each track is blended according to the track weight and speed when [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7ff-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce7ff-120">Requirements</span></span>



| <span data-ttu-id="ce7ff-121">需求</span><span class="sxs-lookup"><span data-stu-id="ce7ff-121">Requirement</span></span> | <span data-ttu-id="ce7ff-122">值</span><span class="sxs-lookup"><span data-stu-id="ce7ff-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7ff-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ce7ff-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ce7ff-124"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce7ff-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ce7ff-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce7ff-125">Library</span></span><br/> | <dl> <span data-ttu-id="ce7ff-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce7ff-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce7ff-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce7ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce7ff-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ce7ff-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

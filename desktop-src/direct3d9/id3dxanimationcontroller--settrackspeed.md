---
description: 設定追蹤速度。 追蹤速度類似于用來加速播放播放軌或減緩播放速度的乘數。
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'ID3DXAnimationController：： SetTrackSpeed 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323359"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a><span data-ttu-id="07f56-104">ID3DXAnimationController：： SetTrackSpeed 方法</span><span class="sxs-lookup"><span data-stu-id="07f56-104">ID3DXAnimationController::SetTrackSpeed method</span></span>

<span data-ttu-id="07f56-105">設定追蹤速度。</span><span class="sxs-lookup"><span data-stu-id="07f56-105">Sets the track speed.</span></span> <span data-ttu-id="07f56-106">追蹤速度類似于用來加速播放播放軌或減緩播放速度的乘數。</span><span class="sxs-lookup"><span data-stu-id="07f56-106">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f56-107">語法</span><span class="sxs-lookup"><span data-stu-id="07f56-107">Syntax</span></span>


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a><span data-ttu-id="07f56-108">參數</span><span class="sxs-lookup"><span data-stu-id="07f56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07f56-109">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07f56-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07f56-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07f56-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07f56-111">要設定速度的曲目識別碼。</span><span class="sxs-lookup"><span data-stu-id="07f56-111">Identifier of the track to set the speed on.</span></span>

</dd> <dt>

<span data-ttu-id="07f56-112">*速度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07f56-112">*Speed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07f56-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07f56-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07f56-114">新的速度。</span><span class="sxs-lookup"><span data-stu-id="07f56-114">New speed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07f56-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="07f56-115">Return value</span></span>

<span data-ttu-id="07f56-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07f56-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07f56-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="07f56-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="07f56-118">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="07f56-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f56-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="07f56-119">Requirements</span></span>



| <span data-ttu-id="07f56-120">需求</span><span class="sxs-lookup"><span data-stu-id="07f56-120">Requirement</span></span> | <span data-ttu-id="07f56-121">值</span><span class="sxs-lookup"><span data-stu-id="07f56-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07f56-122">標頭</span><span class="sxs-lookup"><span data-stu-id="07f56-122">Header</span></span><br/>  | <dl> <span data-ttu-id="07f56-123"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="07f56-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="07f56-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="07f56-124">Library</span></span><br/> | <dl> <span data-ttu-id="07f56-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07f56-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07f56-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07f56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f56-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="07f56-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

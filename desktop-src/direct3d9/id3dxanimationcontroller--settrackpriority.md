---
description: 設定指定動畫播放軌的優先順序混合加權。
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'ID3DXAnimationController：： SetTrackPriority 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986131"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a><span data-ttu-id="226b7-103">ID3DXAnimationController：： SetTrackPriority 方法</span><span class="sxs-lookup"><span data-stu-id="226b7-103">ID3DXAnimationController::SetTrackPriority method</span></span>

<span data-ttu-id="226b7-104">設定指定動畫播放軌的優先順序混合加權。</span><span class="sxs-lookup"><span data-stu-id="226b7-104">Sets the priority blending weight for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="226b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="226b7-105">Syntax</span></span>


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a><span data-ttu-id="226b7-106">參數</span><span class="sxs-lookup"><span data-stu-id="226b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="226b7-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="226b7-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="226b7-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="226b7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="226b7-109">追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="226b7-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="226b7-110">*優先順序* \[在\]</span><span class="sxs-lookup"><span data-stu-id="226b7-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="226b7-111">類型： **[ **D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="226b7-111">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

<span data-ttu-id="226b7-112">追蹤優先權。</span><span class="sxs-lookup"><span data-stu-id="226b7-112">Track priority.</span></span> <span data-ttu-id="226b7-113">這個參數應該設定為 [**D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="226b7-113">This parameter should be set to one of the constants from [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="226b7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="226b7-114">Return value</span></span>

<span data-ttu-id="226b7-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="226b7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="226b7-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="226b7-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="226b7-117">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="226b7-117">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="226b7-118">備註</span><span class="sxs-lookup"><span data-stu-id="226b7-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="226b7-119">需求</span><span class="sxs-lookup"><span data-stu-id="226b7-119">Requirements</span></span>



| <span data-ttu-id="226b7-120">需求</span><span class="sxs-lookup"><span data-stu-id="226b7-120">Requirement</span></span> | <span data-ttu-id="226b7-121">值</span><span class="sxs-lookup"><span data-stu-id="226b7-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="226b7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="226b7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="226b7-123"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="226b7-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="226b7-124">Library</span></span><br/> | <dl> <span data-ttu-id="226b7-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="226b7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="226b7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226b7-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="226b7-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

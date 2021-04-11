---
description: 設定軌跡加權。 權數用來決定如何將多個追蹤混合在一起。
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'ID3DXAnimationController：： SetTrackWeight 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696852"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a><span data-ttu-id="26e80-104">ID3DXAnimationController：： SetTrackWeight 方法</span><span class="sxs-lookup"><span data-stu-id="26e80-104">ID3DXAnimationController::SetTrackWeight method</span></span>

<span data-ttu-id="26e80-105">設定軌跡加權。</span><span class="sxs-lookup"><span data-stu-id="26e80-105">Sets the track weight.</span></span> <span data-ttu-id="26e80-106">權數用來決定如何將多個追蹤混合在一起。</span><span class="sxs-lookup"><span data-stu-id="26e80-106">The weight is used to determine how to blend multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e80-107">語法</span><span class="sxs-lookup"><span data-stu-id="26e80-107">Syntax</span></span>


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a><span data-ttu-id="26e80-108">參數</span><span class="sxs-lookup"><span data-stu-id="26e80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e80-109">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26e80-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e80-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26e80-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26e80-111">要設定權數的追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="26e80-111">Identifier of the track to set the weight on.</span></span>

</dd> <dt>

<span data-ttu-id="26e80-112">*權數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26e80-112">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e80-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26e80-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26e80-114">加權值。</span><span class="sxs-lookup"><span data-stu-id="26e80-114">Weight value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e80-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="26e80-115">Return value</span></span>

<span data-ttu-id="26e80-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26e80-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26e80-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="26e80-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="26e80-118">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="26e80-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e80-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="26e80-119">Requirements</span></span>



| <span data-ttu-id="26e80-120">需求</span><span class="sxs-lookup"><span data-stu-id="26e80-120">Requirement</span></span> | <span data-ttu-id="26e80-121">值</span><span class="sxs-lookup"><span data-stu-id="26e80-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e80-122">標頭</span><span class="sxs-lookup"><span data-stu-id="26e80-122">Header</span></span><br/>  | <dl> <span data-ttu-id="26e80-123"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="26e80-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="26e80-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="26e80-124">Library</span></span><br/> | <dl> <span data-ttu-id="26e80-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26e80-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26e80-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26e80-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e80-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="26e80-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

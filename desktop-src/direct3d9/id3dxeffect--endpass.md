---
description: 結束主動傳遞。
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect：： EndPass 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322980"
---
# <a name="id3dxeffectendpass-method"></a><span data-ttu-id="e3641-103">ID3DXEffect：： EndPass 方法</span><span class="sxs-lookup"><span data-stu-id="e3641-103">ID3DXEffect::EndPass method</span></span>

<span data-ttu-id="e3641-104">結束主動傳遞。</span><span class="sxs-lookup"><span data-stu-id="e3641-104">End an active pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3641-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3641-105">Syntax</span></span>


```C++
HRESULT EndPass();
```



## <a name="parameters"></a><span data-ttu-id="e3641-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3641-106">Parameters</span></span>

<span data-ttu-id="e3641-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e3641-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3641-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3641-108">Return value</span></span>

<span data-ttu-id="e3641-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3641-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3641-110">這個方法一律會傳回值 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e3641-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3641-111">備註</span><span class="sxs-lookup"><span data-stu-id="e3641-111">Remarks</span></span>

<span data-ttu-id="e3641-112">應用程式會藉由呼叫 **ID3DXEffect：： EndPass** 來表示呈現作用中階段的結束。</span><span class="sxs-lookup"><span data-stu-id="e3641-112">An application signals the end of rendering an active pass by calling **ID3DXEffect::EndPass**.</span></span> <span data-ttu-id="e3641-113">每個 **ID3DXEffect：： EndPass** 都必須是成對的 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 和 **ID3DXEffect：： EndPass** 呼叫的一部分。</span><span class="sxs-lookup"><span data-stu-id="e3641-113">Each **ID3DXEffect::EndPass** must be part of a matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls.</span></span>

<span data-ttu-id="e3641-114">每一組相符的 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 和 **ID3DXEffect：： EndPass** 呼叫都必須位於成對的 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 呼叫中。</span><span class="sxs-lookup"><span data-stu-id="e3641-114">Each matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls must be located within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="e3641-115">如果應用程式使用 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)ID3DXEffect：： EndPass 比對配對內的任何 [**effect：： Setx**](id3dxeffect.md)方法變更任何效果狀態 /  ，則在轉譯之前，應用程式必須呼叫 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) ，才能將狀態變更傳播至裝置。</span><span class="sxs-lookup"><span data-stu-id="e3641-115">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/**ID3DXEffect::EndPass** matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3641-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3641-116">Requirements</span></span>



| <span data-ttu-id="e3641-117">需求</span><span class="sxs-lookup"><span data-stu-id="e3641-117">Requirement</span></span> | <span data-ttu-id="e3641-118">值</span><span class="sxs-lookup"><span data-stu-id="e3641-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3641-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e3641-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e3641-120"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3641-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e3641-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3641-121">Library</span></span><br/> | <dl> <span data-ttu-id="e3641-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3641-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e3641-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3641-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3641-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e3641-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 





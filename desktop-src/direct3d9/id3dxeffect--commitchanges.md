---
description: 在轉譯之前，將作用中傳遞內發生的狀態變更傳播至裝置。
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'ID3DXEffect：： CommitChanges 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196289"
---
# <a name="id3dxeffectcommitchanges-method"></a><span data-ttu-id="2d11e-103">ID3DXEffect：： CommitChanges 方法</span><span class="sxs-lookup"><span data-stu-id="2d11e-103">ID3DXEffect::CommitChanges method</span></span>

<span data-ttu-id="2d11e-104">在轉譯之前，將作用中傳遞內發生的狀態變更傳播至裝置。</span><span class="sxs-lookup"><span data-stu-id="2d11e-104">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d11e-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d11e-105">Syntax</span></span>


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a><span data-ttu-id="2d11e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d11e-106">Parameters</span></span>

<span data-ttu-id="2d11e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2d11e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d11e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d11e-108">Return value</span></span>

<span data-ttu-id="2d11e-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d11e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d11e-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2d11e-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d11e-111">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="2d11e-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d11e-112">備註</span><span class="sxs-lookup"><span data-stu-id="2d11e-112">Remarks</span></span>

<span data-ttu-id="2d11e-113">如果應用程式使用 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)ID3DXEffect：： EndPass 比對配對內的任何 [**ID3DXEffect：： Setx**](id3dxeffect.md)方法變更任何效果狀態 / [](id3dxeffect--endpass.md) ，則在轉譯之前，應用程式必須呼叫 **ID3DXEffect：： CommitChanges** ，才能將狀態變更傳播至裝置。</span><span class="sxs-lookup"><span data-stu-id="2d11e-113">If the application changes any effect state using any of the [**ID3DXEffect::Setx**](id3dxeffect.md) methods inside of an [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call **ID3DXEffect::CommitChanges** before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span> <span data-ttu-id="2d11e-114">如果 **ID3DXEffect：： BeginPass** 和 **ID3DXEffect：： EndPass** 比對配對中沒有發生狀態變更，則不需要呼叫 **ID3DXEffect：： CommitChanges**。</span><span class="sxs-lookup"><span data-stu-id="2d11e-114">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

<span data-ttu-id="2d11e-115">這對複製效果中的任何共用參數稍有不同。</span><span class="sxs-lookup"><span data-stu-id="2d11e-115">This is slightly different for any shared parameters in a cloned effect.</span></span> <span data-ttu-id="2d11e-116">當某個技術在複製的效果上處於作用中狀態時 (也就是，呼叫 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 但未呼叫 [**ID3DXEffect：： End**](id3dxeffect--end.md) 時) ， **ID3DXEffect：： CommitChanges** 會更新未如預期般共用的參數。</span><span class="sxs-lookup"><span data-stu-id="2d11e-116">When a technique is active on a cloned effect (that is, when [**ID3DXEffect::Begin**](id3dxeffect--begin.md) has been called but and [**ID3DXEffect::End**](id3dxeffect--end.md) has not been called), **ID3DXEffect::CommitChanges** updates parameters that are not shared as expected.</span></span> <span data-ttu-id="2d11e-117">若要更新共用參數 (僅適用于其技術為使用中) 的複製效果，請呼叫 **ID3DXEffect：： End** 以停用此技術，並使用 **ID3DXEffect：： Begin** 在呼叫 **ID3DXEffect：： CommitChanges** 之前重新啟用該技術。</span><span class="sxs-lookup"><span data-stu-id="2d11e-117">To update a shared parameter (only for a cloned effect whose technique is active), call **ID3DXEffect::End** to deactivate the technique and **ID3DXEffect::Begin** to reactivate the technique before calling **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d11e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d11e-118">Requirements</span></span>



| <span data-ttu-id="2d11e-119">需求</span><span class="sxs-lookup"><span data-stu-id="2d11e-119">Requirement</span></span> | <span data-ttu-id="2d11e-120">值</span><span class="sxs-lookup"><span data-stu-id="2d11e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d11e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2d11e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2d11e-122"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d11e-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2d11e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d11e-123">Library</span></span><br/> | <dl> <span data-ttu-id="2d11e-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d11e-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2d11e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d11e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d11e-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2d11e-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 





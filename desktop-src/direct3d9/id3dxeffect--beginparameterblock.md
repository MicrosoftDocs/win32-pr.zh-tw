---
description: 開始在參數區塊中捕捉狀態變更。
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'ID3DXEffect：： BeginParameterBlock 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035362"
---
# <a name="id3dxeffectbeginparameterblock-method"></a><span data-ttu-id="88289-103">ID3DXEffect：： BeginParameterBlock 方法</span><span class="sxs-lookup"><span data-stu-id="88289-103">ID3DXEffect::BeginParameterBlock method</span></span>

<span data-ttu-id="88289-104">開始在參數區塊中捕捉狀態變更。</span><span class="sxs-lookup"><span data-stu-id="88289-104">Start capturing state changes in a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="88289-105">語法</span><span class="sxs-lookup"><span data-stu-id="88289-105">Syntax</span></span>


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="88289-106">參數</span><span class="sxs-lookup"><span data-stu-id="88289-106">Parameters</span></span>

<span data-ttu-id="88289-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="88289-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88289-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="88289-108">Return value</span></span>

<span data-ttu-id="88289-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88289-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88289-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="88289-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="88289-111">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="88289-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="88289-112">備註</span><span class="sxs-lookup"><span data-stu-id="88289-112">Remarks</span></span>

<span data-ttu-id="88289-113">在呼叫 EndParameterBlock 之前，會變更 Capture 效果參數狀態。</span><span class="sxs-lookup"><span data-stu-id="88289-113">Capture effect parameter state changes until EndParameterBlock is called.</span></span> <span data-ttu-id="88289-114">效果參數包含任何階段以外的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="88289-114">Effect parameters include any state changes outside of a pass.</span></span> <span data-ttu-id="88289-115">如果呼叫 DeleteParameterBlock 不再需要參數區塊，請加以刪除。</span><span class="sxs-lookup"><span data-stu-id="88289-115">Delete parameter blocks if they are no longer needed by calling DeleteParameterBlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="88289-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="88289-116">Requirements</span></span>



| <span data-ttu-id="88289-117">需求</span><span class="sxs-lookup"><span data-stu-id="88289-117">Requirement</span></span> | <span data-ttu-id="88289-118">值</span><span class="sxs-lookup"><span data-stu-id="88289-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88289-119">標頭</span><span class="sxs-lookup"><span data-stu-id="88289-119">Header</span></span><br/>  | <dl> <span data-ttu-id="88289-120"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="88289-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="88289-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="88289-121">Library</span></span><br/> | <dl> <span data-ttu-id="88289-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="88289-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="88289-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88289-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88289-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="88289-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="88289-125">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="88289-125">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="88289-126">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="88289-126">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="88289-127">**ID3DXEffect：:D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="88289-127">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 





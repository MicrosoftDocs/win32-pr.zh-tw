---
description: 停止捕獲效果參數狀態變更。
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'ID3DXEffect：： EndParameterBlock 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946118"
---
# <a name="id3dxeffectendparameterblock-method"></a><span data-ttu-id="e6e5e-103">ID3DXEffect：： EndParameterBlock 方法</span><span class="sxs-lookup"><span data-stu-id="e6e5e-103">ID3DXEffect::EndParameterBlock method</span></span>

<span data-ttu-id="e6e5e-104">停止捕獲效果參數狀態變更。</span><span class="sxs-lookup"><span data-stu-id="e6e5e-104">Stop capturing effect parameter state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e5e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6e5e-105">Syntax</span></span>


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="e6e5e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e6e5e-106">Parameters</span></span>

<span data-ttu-id="e6e5e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e6e5e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6e5e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6e5e-108">Return value</span></span>

<span data-ttu-id="e6e5e-109">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e5e-109">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e6e5e-110">傳回參數狀態欄塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e6e5e-110">Returns a handle to the parameter state block.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e5e-111">備註</span><span class="sxs-lookup"><span data-stu-id="e6e5e-111">Remarks</span></span>

<span data-ttu-id="e6e5e-112">在呼叫 BeginParameterBlock 之後，以及在呼叫 EndParameterBlock) 之前變更狀態 (的所有效果參數，都會儲存在效果參數狀態欄塊中。</span><span class="sxs-lookup"><span data-stu-id="e6e5e-112">All effect parameters that change state (after calling BeginParameterBlock and before calling EndParameterBlock) will be saved in an effect parameter state block.</span></span> <span data-ttu-id="e6e5e-113">使用 ApplyParameterBlock 將此狀態變更區塊套用至效果系統。</span><span class="sxs-lookup"><span data-stu-id="e6e5e-113">Use ApplyParameterBlock to apply this block of state changes to the effect system.</span></span> <span data-ttu-id="e6e5e-114">當您完成狀態欄塊之後，請使用 DeleteParameterBlock 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="e6e5e-114">Once you are finished with a state block use DeleteParameterBlock to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e5e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6e5e-115">Requirements</span></span>



| <span data-ttu-id="e6e5e-116">需求</span><span class="sxs-lookup"><span data-stu-id="e6e5e-116">Requirement</span></span> | <span data-ttu-id="e6e5e-117">值</span><span class="sxs-lookup"><span data-stu-id="e6e5e-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e5e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e6e5e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e6e5e-119"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e5e-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e6e5e-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6e5e-120">Library</span></span><br/> | <dl> <span data-ttu-id="e6e5e-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6e5e-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e6e5e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6e5e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e5e-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e6e5e-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="e6e5e-124">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e6e5e-124">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="e6e5e-125">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e6e5e-125">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="e6e5e-126">**ID3DXEffect：:D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e6e5e-126">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 





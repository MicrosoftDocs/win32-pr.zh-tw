---
description: 將狀態欄塊中的值套用至目前的效果系統狀態。
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'ID3DXEffect：： ApplyParameterBlock 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988592"
---
# <a name="id3dxeffectapplyparameterblock-method"></a><span data-ttu-id="119e8-103">ID3DXEffect：： ApplyParameterBlock 方法</span><span class="sxs-lookup"><span data-stu-id="119e8-103">ID3DXEffect::ApplyParameterBlock method</span></span>

<span data-ttu-id="119e8-104">將狀態欄塊中的值套用至目前的效果系統狀態。</span><span class="sxs-lookup"><span data-stu-id="119e8-104">Apply the values in a state block to the current effect system state.</span></span>

## <a name="syntax"></a><span data-ttu-id="119e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="119e8-105">Syntax</span></span>


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="119e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="119e8-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="119e8-107">*hParameterBlock* \[在\]</span><span class="sxs-lookup"><span data-stu-id="119e8-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="119e8-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="119e8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="119e8-109">參數區塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="119e8-109">A handle to the parameter block.</span></span> <span data-ttu-id="119e8-110">這是 [**ID3DXEffect：： EndParameterBlock**](id3dxeffect--endparameterblock.md)所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="119e8-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="119e8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="119e8-111">Return value</span></span>

<span data-ttu-id="119e8-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="119e8-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="119e8-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="119e8-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="119e8-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="119e8-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="119e8-115">備註</span><span class="sxs-lookup"><span data-stu-id="119e8-115">Remarks</span></span>

<span data-ttu-id="119e8-116">藉由呼叫 BeginParameterBlock，在參數區塊中捕捉效果參數狀態變更;藉由呼叫 EndParameterBlock 來停止捕捉狀態變更。</span><span class="sxs-lookup"><span data-stu-id="119e8-116">Capture effect parameter state changes in a parameter block by calling BeginParameterBlock; stop capturing state changes by calling EndParameterBlock.</span></span> <span data-ttu-id="119e8-117">這些狀態變更包括在技術內發生的任何效果參數變更， (包括通過) 以外的變更。</span><span class="sxs-lookup"><span data-stu-id="119e8-117">These state changes include any effect parameter changes that occur inside of a technique (including those outside of a pass).</span></span> <span data-ttu-id="119e8-118">完成參數區塊之後，請呼叫 DeleteParameterBlock 來復原記憶體。</span><span class="sxs-lookup"><span data-stu-id="119e8-118">Once you are done with the parameter block, call DeleteParameterBlock to recover memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="119e8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="119e8-119">Requirements</span></span>



| <span data-ttu-id="119e8-120">需求</span><span class="sxs-lookup"><span data-stu-id="119e8-120">Requirement</span></span> | <span data-ttu-id="119e8-121">值</span><span class="sxs-lookup"><span data-stu-id="119e8-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="119e8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="119e8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="119e8-123"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="119e8-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="119e8-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="119e8-124">Library</span></span><br/> | <dl> <span data-ttu-id="119e8-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="119e8-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="119e8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="119e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119e8-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="119e8-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="119e8-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="119e8-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="119e8-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="119e8-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="119e8-130">**ID3DXEffect：:D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="119e8-130">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 





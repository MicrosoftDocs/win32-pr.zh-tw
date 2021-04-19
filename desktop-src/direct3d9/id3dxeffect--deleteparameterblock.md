---
description: 刪除參數區塊。
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: 'ID3DXEffect：:D eleteParameterBlock 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976708"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a><span data-ttu-id="ef5a3-103">ID3DXEffect：:D eleteParameterBlock 方法</span><span class="sxs-lookup"><span data-stu-id="ef5a3-103">ID3DXEffect::DeleteParameterBlock method</span></span>

<span data-ttu-id="ef5a3-104">刪除參數區塊。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-104">Delete a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef5a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef5a3-105">Syntax</span></span>


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="ef5a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef5a3-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="ef5a3-107">*hParameterBlock* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef5a3-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef5a3-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ef5a3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ef5a3-109">參數區塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-109">A handle to the parameter block.</span></span> <span data-ttu-id="ef5a3-110">這是 [**ID3DXEffect：： EndParameterBlock**](id3dxeffect--endparameterblock.md)所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef5a3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef5a3-111">Return value</span></span>

<span data-ttu-id="ef5a3-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef5a3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef5a3-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ef5a3-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef5a3-115">備註</span><span class="sxs-lookup"><span data-stu-id="ef5a3-115">Remarks</span></span>

<span data-ttu-id="ef5a3-116">參數區塊是作用中狀態的區塊。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-116">Parameter blocks are blocks of effect states.</span></span> <span data-ttu-id="ef5a3-117">您可以使用參數區塊來記錄狀態變更，以在稍後使用單一 API 呼叫來套用它們。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-117">Use a parameter block to record state changes so that they can be applied later on with a single API call.</span></span> <span data-ttu-id="ef5a3-118">當不再需要時，請刪除參數區塊以減少記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="ef5a3-118">When no longer needed, delete the parameter block to reduce memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef5a3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef5a3-119">Requirements</span></span>



| <span data-ttu-id="ef5a3-120">需求</span><span class="sxs-lookup"><span data-stu-id="ef5a3-120">Requirement</span></span> | <span data-ttu-id="ef5a3-121">值</span><span class="sxs-lookup"><span data-stu-id="ef5a3-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5a3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ef5a3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ef5a3-123"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef5a3-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ef5a3-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef5a3-124">Library</span></span><br/> | <dl> <span data-ttu-id="ef5a3-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef5a3-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ef5a3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef5a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef5a3-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="ef5a3-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="ef5a3-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="ef5a3-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="ef5a3-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="ef5a3-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 





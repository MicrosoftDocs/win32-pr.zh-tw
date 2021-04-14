---
description: 搜尋下一個有效的技巧，從指定技術之後的技巧開始。
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'ID3DXEffect：： FindNextValidTechnique 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386467"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a><span data-ttu-id="88704-103">ID3DXEffect：： FindNextValidTechnique 方法</span><span class="sxs-lookup"><span data-stu-id="88704-103">ID3DXEffect::FindNextValidTechnique method</span></span>

<span data-ttu-id="88704-104">搜尋下一個有效的技巧，從指定技術之後的技巧開始。</span><span class="sxs-lookup"><span data-stu-id="88704-104">Searches for the next valid technique, starting at the technique after the specified technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="88704-105">語法</span><span class="sxs-lookup"><span data-stu-id="88704-105">Syntax</span></span>


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="88704-106">參數</span><span class="sxs-lookup"><span data-stu-id="88704-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88704-107">*hTechnique* \[在\]</span><span class="sxs-lookup"><span data-stu-id="88704-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88704-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="88704-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="88704-109">技術的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="88704-109">Unique identifier to a technique.</span></span> <span data-ttu-id="88704-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="88704-110">See [Handles (Direct3D 9)](handles.md).</span></span> <span data-ttu-id="88704-111">請為此參數指定 **Null** ，以找出第一個有效的技巧。</span><span class="sxs-lookup"><span data-stu-id="88704-111">Specify **NULL** for this parameter to find the first valid technique.</span></span>

</dd> <dt>

<span data-ttu-id="88704-112">*pTechnique* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="88704-112">*pTechnique* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88704-113">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span><span class="sxs-lookup"><span data-stu-id="88704-113">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span></span>

<span data-ttu-id="88704-114">下一項技術的識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="88704-114">Pointer to an identifier for the next technique.</span></span> <span data-ttu-id="88704-115">如果這是最後一項技術，就會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="88704-115">**NULL** is returned if this is the last technique.</span></span> <span data-ttu-id="88704-116">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="88704-116">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88704-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="88704-117">Return value</span></span>

<span data-ttu-id="88704-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88704-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88704-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="88704-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="88704-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="88704-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="88704-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="88704-121">Requirements</span></span>



| <span data-ttu-id="88704-122">需求</span><span class="sxs-lookup"><span data-stu-id="88704-122">Requirement</span></span> | <span data-ttu-id="88704-123">值</span><span class="sxs-lookup"><span data-stu-id="88704-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88704-124">標頭</span><span class="sxs-lookup"><span data-stu-id="88704-124">Header</span></span><br/>  | <dl> <span data-ttu-id="88704-125"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="88704-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="88704-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="88704-126">Library</span></span><br/> | <dl> <span data-ttu-id="88704-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="88704-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="88704-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88704-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88704-129">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="88704-129">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="88704-130">**D3DXTECHNIQUE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="88704-130">**D3DXTECHNIQUE\_DESC**</span></span>](d3dxtechnique-desc.md)
</dt> <dt>

[<span data-ttu-id="88704-131">**ID3DXEffect::ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="88704-131">**ID3DXEffect::ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 





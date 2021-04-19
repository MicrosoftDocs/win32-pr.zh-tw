---
description: 驗證技巧。
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'ID3DXEffect：： ValidateTechnique 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997615"
---
# <a name="id3dxeffectvalidatetechnique-method"></a><span data-ttu-id="288fc-103">ID3DXEffect：： ValidateTechnique 方法</span><span class="sxs-lookup"><span data-stu-id="288fc-103">ID3DXEffect::ValidateTechnique method</span></span>

<span data-ttu-id="288fc-104">驗證技巧。</span><span class="sxs-lookup"><span data-stu-id="288fc-104">Validate a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="288fc-105">語法</span><span class="sxs-lookup"><span data-stu-id="288fc-105">Syntax</span></span>


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="288fc-106">參數</span><span class="sxs-lookup"><span data-stu-id="288fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="288fc-107">*hTechnique* \[在\]</span><span class="sxs-lookup"><span data-stu-id="288fc-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="288fc-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="288fc-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="288fc-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="288fc-109">Unique identifier.</span></span> <span data-ttu-id="288fc-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="288fc-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="288fc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="288fc-111">Return value</span></span>

<span data-ttu-id="288fc-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="288fc-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="288fc-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="288fc-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="288fc-114">如果方法失敗，傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ CONFLICTINGRENDERSTATE、D3DERR \_ CONFLICTINGTEXTUREFILTER、D3DERR \_ DEVICELOST、D3DERR \_ DRIVERINTERNALERROR、D3DERR \_ TOOMANYOPERATIONS、D3DERR UNSUPPORTEDALPHAARG、 \_ D3DERR \_ \_ \_ \_ \_ UNSUPPORTEDALPHAOPERATION、D3DERR UNSUPPORTEDCOLORARG、D3DERR UNSUPPORTEDCOLOROPERATION、D3DERR UNSUPPORTEDFACTORVALUE、D3DERR UNSUPPORTEDTEXTUREFILTER 和 D3DERR \_ WRONGTEXTUREFORMAT。</span><span class="sxs-lookup"><span data-stu-id="288fc-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_CONFLICTINGRENDERSTATE, D3DERR\_CONFLICTINGTEXTUREFILTER, D3DERR\_DEVICELOST, D3DERR\_DRIVERINTERNALERROR, D3DERR\_TOOMANYOPERATIONS, D3DERR\_UNSUPPORTEDALPHAARG, D3DERR\_UNSUPPORTEDALPHAOPERATION, D3DERR\_UNSUPPORTEDCOLORARG, D3DERR\_UNSUPPORTEDCOLOROPERATION, D3DERR\_UNSUPPORTEDFACTORVALUE, D3DERR\_UNSUPPORTEDTEXTUREFILTER, and D3DERR\_WRONGTEXTUREFORMAT.</span></span>

## <a name="requirements"></a><span data-ttu-id="288fc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="288fc-115">Requirements</span></span>



| <span data-ttu-id="288fc-116">需求</span><span class="sxs-lookup"><span data-stu-id="288fc-116">Requirement</span></span> | <span data-ttu-id="288fc-117">值</span><span class="sxs-lookup"><span data-stu-id="288fc-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="288fc-118">標頭</span><span class="sxs-lookup"><span data-stu-id="288fc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="288fc-119"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="288fc-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="288fc-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="288fc-120">Library</span></span><br/> | <dl> <span data-ttu-id="288fc-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="288fc-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="288fc-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="288fc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288fc-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="288fc-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="288fc-124">**ID3DXEffect::SetTechnique**</span><span class="sxs-lookup"><span data-stu-id="288fc-124">**ID3DXEffect::SetTechnique**</span></span>](id3dxeffect--settechnique.md)
</dt> </dl>

 

 





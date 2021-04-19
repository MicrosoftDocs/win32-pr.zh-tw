---
description: 設定布林值。
ms.assetid: bb7c4860-50a0-416a-b9e0-5a2bec113e3c
title: 'ID3DXBaseEffect：： SetBool 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: be137ac210297b9fce12dafaffb6fead61d39512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974830"
---
# <a name="id3dxbaseeffectsetbool-method"></a><span data-ttu-id="363e8-103">ID3DXBaseEffect：： SetBool 方法</span><span class="sxs-lookup"><span data-stu-id="363e8-103">ID3DXBaseEffect::SetBool method</span></span>

<span data-ttu-id="363e8-104">設定布林值。</span><span class="sxs-lookup"><span data-stu-id="363e8-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="363e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="363e8-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="363e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="363e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="363e8-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="363e8-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363e8-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="363e8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="363e8-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="363e8-109">Unique identifier.</span></span> <span data-ttu-id="363e8-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="363e8-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="363e8-111">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="363e8-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363e8-112">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363e8-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="363e8-113">布林值。</span><span class="sxs-lookup"><span data-stu-id="363e8-113">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="363e8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="363e8-114">Return value</span></span>

<span data-ttu-id="363e8-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="363e8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="363e8-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="363e8-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="363e8-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="363e8-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="363e8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="363e8-118">Requirements</span></span>



| <span data-ttu-id="363e8-119">需求</span><span class="sxs-lookup"><span data-stu-id="363e8-119">Requirement</span></span> | <span data-ttu-id="363e8-120">值</span><span class="sxs-lookup"><span data-stu-id="363e8-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="363e8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="363e8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="363e8-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="363e8-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="363e8-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="363e8-123">Library</span></span><br/> | <dl> <span data-ttu-id="363e8-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="363e8-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="363e8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="363e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363e8-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="363e8-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="363e8-127">**GetBool**</span><span class="sxs-lookup"><span data-stu-id="363e8-127">**GetBool**</span></span>](id3dxbaseeffect--getbool.md)
</dt> </dl>

 

 

---
description: ID3DXBaseEffect：： SetIntArray 方法：設定整數的陣列。
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'ID3DXBaseEffect：： SetIntArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093756"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="16a94-103">ID3DXBaseEffect：： SetIntArray 方法</span><span class="sxs-lookup"><span data-stu-id="16a94-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="16a94-104">設定整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="16a94-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a94-105">語法</span><span class="sxs-lookup"><span data-stu-id="16a94-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="16a94-106">參數</span><span class="sxs-lookup"><span data-stu-id="16a94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a94-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16a94-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a94-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="16a94-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="16a94-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="16a94-109">Unique identifier.</span></span> <span data-ttu-id="16a94-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="16a94-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="16a94-111">*pn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16a94-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a94-112">類型： **Const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="16a94-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16a94-113">整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="16a94-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="16a94-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16a94-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a94-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16a94-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16a94-116">陣列中的整數數目。</span><span class="sxs-lookup"><span data-stu-id="16a94-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a94-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="16a94-117">Return value</span></span>

<span data-ttu-id="16a94-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16a94-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16a94-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="16a94-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="16a94-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="16a94-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a94-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="16a94-121">Requirements</span></span>



| <span data-ttu-id="16a94-122">需求</span><span class="sxs-lookup"><span data-stu-id="16a94-122">Requirement</span></span> | <span data-ttu-id="16a94-123">值</span><span class="sxs-lookup"><span data-stu-id="16a94-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a94-124">標頭</span><span class="sxs-lookup"><span data-stu-id="16a94-124">Header</span></span><br/>  | <dl> <span data-ttu-id="16a94-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="16a94-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="16a94-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="16a94-126">Library</span></span><br/> | <dl> <span data-ttu-id="16a94-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16a94-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="16a94-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16a94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a94-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="16a94-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="16a94-130">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="16a94-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 

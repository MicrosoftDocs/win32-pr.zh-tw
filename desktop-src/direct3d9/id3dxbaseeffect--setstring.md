---
description: 設定字串。
ms.assetid: 7e8eef70-85ee-461d-bf8c-44cda5f184cd
title: 'ID3DXBaseEffect：： SetString 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a7c4f86c6b7fa78c869eb1d5bd49634ec4b496d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998577"
---
# <a name="id3dxbaseeffectsetstring-method"></a><span data-ttu-id="3d07e-103">ID3DXBaseEffect：： SetString 方法</span><span class="sxs-lookup"><span data-stu-id="3d07e-103">ID3DXBaseEffect::SetString method</span></span>

<span data-ttu-id="3d07e-104">設定字串。</span><span class="sxs-lookup"><span data-stu-id="3d07e-104">Sets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d07e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d07e-105">Syntax</span></span>


```C++
HRESULT SetString(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pString
);
```



## <a name="parameters"></a><span data-ttu-id="3d07e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d07e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d07e-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d07e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d07e-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3d07e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3d07e-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d07e-109">Unique identifier.</span></span> <span data-ttu-id="3d07e-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="3d07e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d07e-111">*pString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d07e-111">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d07e-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d07e-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d07e-113">要設定的字串。</span><span class="sxs-lookup"><span data-stu-id="3d07e-113">String to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d07e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d07e-114">Return value</span></span>

<span data-ttu-id="3d07e-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d07e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d07e-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3d07e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3d07e-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="3d07e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d07e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d07e-118">Requirements</span></span>



| <span data-ttu-id="3d07e-119">需求</span><span class="sxs-lookup"><span data-stu-id="3d07e-119">Requirement</span></span> | <span data-ttu-id="3d07e-120">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d07e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3d07e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3d07e-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d07e-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3d07e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3d07e-123">Library</span></span><br/> | <dl> <span data-ttu-id="3d07e-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d07e-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3d07e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d07e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d07e-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3d07e-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="3d07e-127">**GetString**</span><span class="sxs-lookup"><span data-stu-id="3d07e-127">**GetString**</span></span>](id3dxbaseeffect--getstring.md)
</dt> </dl>

 

 

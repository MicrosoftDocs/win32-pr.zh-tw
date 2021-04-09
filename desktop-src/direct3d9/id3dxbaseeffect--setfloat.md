---
description: 設定浮點值。
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'ID3DXBaseEffect：： SetFloat 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af955748fff66e67e0e2f5650b869a746168de54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853963"
---
# <a name="id3dxbaseeffectsetfloat-method"></a><span data-ttu-id="5fe43-103">ID3DXBaseEffect：： SetFloat 方法</span><span class="sxs-lookup"><span data-stu-id="5fe43-103">ID3DXBaseEffect::SetFloat method</span></span>

<span data-ttu-id="5fe43-104">設定浮點值。</span><span class="sxs-lookup"><span data-stu-id="5fe43-104">Sets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe43-105">語法</span><span class="sxs-lookup"><span data-stu-id="5fe43-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="5fe43-106">參數</span><span class="sxs-lookup"><span data-stu-id="5fe43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fe43-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fe43-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe43-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe43-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5fe43-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5fe43-109">Unique identifier.</span></span> <span data-ttu-id="5fe43-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="5fe43-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fe43-111">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fe43-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe43-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe43-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fe43-113">浮點值。</span><span class="sxs-lookup"><span data-stu-id="5fe43-113">Floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fe43-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fe43-114">Return value</span></span>

<span data-ttu-id="5fe43-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fe43-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fe43-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5fe43-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5fe43-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5fe43-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe43-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fe43-118">Requirements</span></span>



| <span data-ttu-id="5fe43-119">需求</span><span class="sxs-lookup"><span data-stu-id="5fe43-119">Requirement</span></span> | <span data-ttu-id="5fe43-120">值</span><span class="sxs-lookup"><span data-stu-id="5fe43-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe43-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5fe43-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5fe43-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="5fe43-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5fe43-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="5fe43-123">Library</span></span><br/> | <dl> <span data-ttu-id="5fe43-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fe43-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5fe43-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fe43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe43-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5fe43-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5fe43-127">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="5fe43-127">**GetFloat**</span></span>](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 

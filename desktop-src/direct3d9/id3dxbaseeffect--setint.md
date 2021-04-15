---
description: 設定整數。
ms.assetid: 1090d4a6-b4f5-4e15-a49f-e2724f1c3f95
title: 'ID3DXBaseEffect：： SetInt 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3c27d66544d4064c8d6c682db168b57b88d213cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322620"
---
# <a name="id3dxbaseeffectsetint-method"></a><span data-ttu-id="5ab47-103">ID3DXBaseEffect：： SetInt 方法</span><span class="sxs-lookup"><span data-stu-id="5ab47-103">ID3DXBaseEffect::SetInt method</span></span>

<span data-ttu-id="5ab47-104">設定整數。</span><span class="sxs-lookup"><span data-stu-id="5ab47-104">Sets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab47-105">語法</span><span class="sxs-lookup"><span data-stu-id="5ab47-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hParameter,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="5ab47-106">參數</span><span class="sxs-lookup"><span data-stu-id="5ab47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab47-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ab47-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab47-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5ab47-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5ab47-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ab47-109">Unique identifier.</span></span> <span data-ttu-id="5ab47-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab47-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab47-111">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ab47-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab47-112">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ab47-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ab47-113">整數值。</span><span class="sxs-lookup"><span data-stu-id="5ab47-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab47-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ab47-114">Return value</span></span>

<span data-ttu-id="5ab47-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ab47-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ab47-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5ab47-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5ab47-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5ab47-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab47-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ab47-118">Requirements</span></span>



| <span data-ttu-id="5ab47-119">需求</span><span class="sxs-lookup"><span data-stu-id="5ab47-119">Requirement</span></span> | <span data-ttu-id="5ab47-120">值</span><span class="sxs-lookup"><span data-stu-id="5ab47-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab47-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5ab47-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5ab47-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab47-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5ab47-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="5ab47-123">Library</span></span><br/> | <dl> <span data-ttu-id="5ab47-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ab47-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5ab47-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ab47-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab47-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5ab47-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5ab47-127">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="5ab47-127">**GetInt**</span></span>](id3dxbaseeffect--getint.md)
</dt> </dl>

 

 

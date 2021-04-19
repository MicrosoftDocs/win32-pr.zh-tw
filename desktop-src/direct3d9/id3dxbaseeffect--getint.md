---
description: 取得整數。
ms.assetid: 8074758a-f650-4698-8a75-aa0ffb14cb21
title: 'ID3DXBaseEffect：： GetInt 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c0fe1fa01260be936b9d7f8be394d0c43a781680
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981257"
---
# <a name="id3dxbaseeffectgetint-method"></a><span data-ttu-id="cf7bf-103">ID3DXBaseEffect：： GetInt 方法</span><span class="sxs-lookup"><span data-stu-id="cf7bf-103">ID3DXBaseEffect::GetInt method</span></span>

<span data-ttu-id="cf7bf-104">取得整數。</span><span class="sxs-lookup"><span data-stu-id="cf7bf-104">Gets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf7bf-105">Syntax</span></span>


```C++
HRESULT GetInt(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn
);
```



## <a name="parameters"></a><span data-ttu-id="cf7bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf7bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7bf-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf7bf-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf7bf-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cf7bf-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cf7bf-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf7bf-109">Unique identifier.</span></span> <span data-ttu-id="cf7bf-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="cf7bf-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf7bf-111">*pn* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf7bf-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf7bf-112">類型： **[ **INT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf7bf-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cf7bf-113">傳回整數。</span><span class="sxs-lookup"><span data-stu-id="cf7bf-113">Returns an integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7bf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf7bf-114">Return value</span></span>

<span data-ttu-id="cf7bf-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf7bf-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf7bf-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="cf7bf-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cf7bf-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="cf7bf-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7bf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf7bf-118">Requirements</span></span>



| <span data-ttu-id="cf7bf-119">需求</span><span class="sxs-lookup"><span data-stu-id="cf7bf-119">Requirement</span></span> | <span data-ttu-id="cf7bf-120">值</span><span class="sxs-lookup"><span data-stu-id="cf7bf-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7bf-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cf7bf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cf7bf-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf7bf-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cf7bf-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf7bf-123">Library</span></span><br/> | <dl> <span data-ttu-id="cf7bf-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf7bf-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cf7bf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf7bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7bf-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="cf7bf-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="cf7bf-127">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="cf7bf-127">**SetInt**</span></span>](id3dxbaseeffect--setint.md)
</dt> </dl>

 

 

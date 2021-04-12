---
description: 取得整數的陣列。
ms.assetid: c02b5343-db4f-4e8c-989c-6aba8c19c234
title: 'ID3DXBaseEffect：： GetIntArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f13c6b8717c2108920d7b914da20b99f0451f5d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323336"
---
# <a name="id3dxbaseeffectgetintarray-method"></a><span data-ttu-id="84c72-103">ID3DXBaseEffect：： GetIntArray 方法</span><span class="sxs-lookup"><span data-stu-id="84c72-103">ID3DXBaseEffect::GetIntArray method</span></span>

<span data-ttu-id="84c72-104">取得整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="84c72-104">Gets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c72-105">語法</span><span class="sxs-lookup"><span data-stu-id="84c72-105">Syntax</span></span>


```C++
HRESULT GetIntArray(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="84c72-106">參數</span><span class="sxs-lookup"><span data-stu-id="84c72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c72-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84c72-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c72-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="84c72-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="84c72-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="84c72-109">Unique identifier.</span></span> <span data-ttu-id="84c72-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="84c72-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="84c72-111">*pn* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="84c72-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84c72-112">類型： **[ **INT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84c72-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84c72-113">傳回整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="84c72-113">Returns an array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="84c72-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84c72-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c72-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84c72-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84c72-116">陣列中的整數數目。</span><span class="sxs-lookup"><span data-stu-id="84c72-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c72-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="84c72-117">Return value</span></span>

<span data-ttu-id="84c72-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84c72-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84c72-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="84c72-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="84c72-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="84c72-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c72-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="84c72-121">Requirements</span></span>



| <span data-ttu-id="84c72-122">需求</span><span class="sxs-lookup"><span data-stu-id="84c72-122">Requirement</span></span> | <span data-ttu-id="84c72-123">值</span><span class="sxs-lookup"><span data-stu-id="84c72-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c72-124">標頭</span><span class="sxs-lookup"><span data-stu-id="84c72-124">Header</span></span><br/>  | <dl> <span data-ttu-id="84c72-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="84c72-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="84c72-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="84c72-126">Library</span></span><br/> | <dl> <span data-ttu-id="84c72-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="84c72-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="84c72-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84c72-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c72-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="84c72-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="84c72-130">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="84c72-130">**SetIntArray**</span></span>](id3dxbaseeffect--setintarray.md)
</dt> </dl>

 

 

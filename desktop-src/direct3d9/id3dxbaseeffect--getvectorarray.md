---
description: 取得向量的陣列。
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'ID3DXBaseEffect：： GetVectorArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322627"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a><span data-ttu-id="a330b-103">ID3DXBaseEffect：： GetVectorArray 方法</span><span class="sxs-lookup"><span data-stu-id="a330b-103">ID3DXBaseEffect::GetVectorArray method</span></span>

<span data-ttu-id="a330b-104">取得向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="a330b-104">Gets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a330b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a330b-105">Syntax</span></span>


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="a330b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a330b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a330b-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a330b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a330b-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a330b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a330b-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a330b-109">Unique identifier.</span></span> <span data-ttu-id="a330b-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="a330b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a330b-111">*pVector* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a330b-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a330b-112">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a330b-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a330b-113">傳回4D 浮點數向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="a330b-113">Returns an array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="a330b-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a330b-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a330b-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a330b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a330b-116">陣列中的向量數目。</span><span class="sxs-lookup"><span data-stu-id="a330b-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a330b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a330b-117">Return value</span></span>

<span data-ttu-id="a330b-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a330b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a330b-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a330b-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a330b-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a330b-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a330b-121">備註</span><span class="sxs-lookup"><span data-stu-id="a330b-121">Remarks</span></span>

<span data-ttu-id="a330b-122">如果目的地向量大於來源向量，則只會填入每個目的地向量的初始元件，而其餘的目的地向量元件會設定為零。</span><span class="sxs-lookup"><span data-stu-id="a330b-122">If the destination vectors are larger than the source vectors, only the initial components of each destination vector will be filled, and the remaining destination vector components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a330b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a330b-123">Requirements</span></span>



| <span data-ttu-id="a330b-124">需求</span><span class="sxs-lookup"><span data-stu-id="a330b-124">Requirement</span></span> | <span data-ttu-id="a330b-125">值</span><span class="sxs-lookup"><span data-stu-id="a330b-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a330b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a330b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a330b-127"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="a330b-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a330b-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="a330b-128">Library</span></span><br/> | <dl> <span data-ttu-id="a330b-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a330b-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a330b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a330b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a330b-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a330b-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a330b-132">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="a330b-132">**SetVectorArray**</span></span>](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 

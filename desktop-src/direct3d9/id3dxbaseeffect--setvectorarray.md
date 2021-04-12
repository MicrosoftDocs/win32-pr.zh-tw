---
description: 設定向量的陣列。
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: 'ID3DXBaseEffect：： SetVectorArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4c5deace65608ee547b8fdcc4fb236b11d38c810
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946172"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a><span data-ttu-id="866b3-103">ID3DXBaseEffect：： SetVectorArray 方法</span><span class="sxs-lookup"><span data-stu-id="866b3-103">ID3DXBaseEffect::SetVectorArray method</span></span>

<span data-ttu-id="866b3-104">設定向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="866b3-104">Sets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="866b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="866b3-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="866b3-106">參數</span><span class="sxs-lookup"><span data-stu-id="866b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="866b3-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="866b3-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866b3-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="866b3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="866b3-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="866b3-109">Unique identifier.</span></span> <span data-ttu-id="866b3-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="866b3-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="866b3-111">*pVector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="866b3-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866b3-112">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="866b3-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="866b3-113">4D 浮點數向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="866b3-113">Array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="866b3-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="866b3-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866b3-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="866b3-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="866b3-116">陣列中的向量數目。</span><span class="sxs-lookup"><span data-stu-id="866b3-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="866b3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="866b3-117">Return value</span></span>

<span data-ttu-id="866b3-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="866b3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="866b3-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="866b3-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="866b3-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="866b3-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="866b3-121">備註</span><span class="sxs-lookup"><span data-stu-id="866b3-121">Remarks</span></span>

<span data-ttu-id="866b3-122">如果目的地向量小於來源向量，則會忽略來源向量的其他元件。</span><span class="sxs-lookup"><span data-stu-id="866b3-122">If the destination vectors are smaller than the source vectors, the additional components of the source vectors will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="866b3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="866b3-123">Requirements</span></span>



| <span data-ttu-id="866b3-124">需求</span><span class="sxs-lookup"><span data-stu-id="866b3-124">Requirement</span></span> | <span data-ttu-id="866b3-125">值</span><span class="sxs-lookup"><span data-stu-id="866b3-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="866b3-126">標頭</span><span class="sxs-lookup"><span data-stu-id="866b3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="866b3-127"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="866b3-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="866b3-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="866b3-128">Library</span></span><br/> | <dl> <span data-ttu-id="866b3-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="866b3-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="866b3-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="866b3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866b3-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="866b3-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="866b3-132">**GetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="866b3-132">**GetVectorArray**</span></span>](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 

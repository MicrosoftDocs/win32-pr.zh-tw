---
description: ID3DXBaseEffect：： SetBoolArray 方法：設定布林值的陣列。
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'ID3DXBaseEffect：： SetBoolArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cad6846914d348dd49d6362d70271c5af078e35d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093826"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="14f3a-103">ID3DXBaseEffect：： SetBoolArray 方法</span><span class="sxs-lookup"><span data-stu-id="14f3a-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="14f3a-104">設定布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="14f3a-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="14f3a-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="14f3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="14f3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f3a-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14f3a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f3a-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="14f3a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="14f3a-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="14f3a-109">Unique identifier.</span></span> <span data-ttu-id="14f3a-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="14f3a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="14f3a-111">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14f3a-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f3a-112">類型： **Const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="14f3a-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="14f3a-113">布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="14f3a-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="14f3a-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14f3a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f3a-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14f3a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14f3a-116">陣列中的布林值數目。</span><span class="sxs-lookup"><span data-stu-id="14f3a-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f3a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="14f3a-117">Return value</span></span>

<span data-ttu-id="14f3a-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14f3a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14f3a-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="14f3a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14f3a-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="14f3a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="14f3a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="14f3a-121">Requirements</span></span>



| <span data-ttu-id="14f3a-122">需求</span><span class="sxs-lookup"><span data-stu-id="14f3a-122">Requirement</span></span> | <span data-ttu-id="14f3a-123">值</span><span class="sxs-lookup"><span data-stu-id="14f3a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f3a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="14f3a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="14f3a-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="14f3a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="14f3a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="14f3a-126">Library</span></span><br/> | <dl> <span data-ttu-id="14f3a-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="14f3a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="14f3a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14f3a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f3a-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="14f3a-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="14f3a-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="14f3a-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 

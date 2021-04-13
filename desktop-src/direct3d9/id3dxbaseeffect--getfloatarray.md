---
description: 取得浮點值的陣列。
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'ID3DXBaseEffect：： GetFloatArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2ea71daa3b207a8f7716bf0a0db3608554c0b9f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323344"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a><span data-ttu-id="8952c-103">ID3DXBaseEffect：： GetFloatArray 方法</span><span class="sxs-lookup"><span data-stu-id="8952c-103">ID3DXBaseEffect::GetFloatArray method</span></span>

<span data-ttu-id="8952c-104">取得浮點值的陣列。</span><span class="sxs-lookup"><span data-stu-id="8952c-104">Gets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8952c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8952c-105">Syntax</span></span>


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="8952c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8952c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8952c-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8952c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8952c-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8952c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8952c-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8952c-109">Unique identifier.</span></span> <span data-ttu-id="8952c-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="8952c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8952c-111">*pf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8952c-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8952c-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8952c-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8952c-113">傳回浮點值的陣列。</span><span class="sxs-lookup"><span data-stu-id="8952c-113">Returns an array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="8952c-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8952c-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8952c-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8952c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8952c-116">陣列中的浮點值數目。</span><span class="sxs-lookup"><span data-stu-id="8952c-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8952c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8952c-117">Return value</span></span>

<span data-ttu-id="8952c-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8952c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8952c-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8952c-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8952c-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="8952c-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8952c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8952c-121">Requirements</span></span>



| <span data-ttu-id="8952c-122">需求</span><span class="sxs-lookup"><span data-stu-id="8952c-122">Requirement</span></span> | <span data-ttu-id="8952c-123">值</span><span class="sxs-lookup"><span data-stu-id="8952c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8952c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8952c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8952c-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="8952c-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8952c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8952c-126">Library</span></span><br/> | <dl> <span data-ttu-id="8952c-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8952c-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8952c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8952c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8952c-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8952c-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8952c-130">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="8952c-130">**SetFloatArray**</span></span>](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 

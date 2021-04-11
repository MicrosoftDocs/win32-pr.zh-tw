---
description: 設定浮點值的陣列。
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'ID3DXBaseEffect：： SetFloatArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196175"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a><span data-ttu-id="30ca9-103">ID3DXBaseEffect：： SetFloatArray 方法</span><span class="sxs-lookup"><span data-stu-id="30ca9-103">ID3DXBaseEffect::SetFloatArray method</span></span>

<span data-ttu-id="30ca9-104">設定浮點值的陣列。</span><span class="sxs-lookup"><span data-stu-id="30ca9-104">Sets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ca9-105">語法</span><span class="sxs-lookup"><span data-stu-id="30ca9-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="30ca9-106">參數</span><span class="sxs-lookup"><span data-stu-id="30ca9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ca9-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30ca9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ca9-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="30ca9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="30ca9-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="30ca9-109">Unique identifier.</span></span> <span data-ttu-id="30ca9-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="30ca9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="30ca9-111">*pf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30ca9-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ca9-112">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="30ca9-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="30ca9-113">浮點值的陣列。</span><span class="sxs-lookup"><span data-stu-id="30ca9-113">Array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="30ca9-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30ca9-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ca9-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30ca9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30ca9-116">陣列中的浮點值數目。</span><span class="sxs-lookup"><span data-stu-id="30ca9-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ca9-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="30ca9-117">Return value</span></span>

<span data-ttu-id="30ca9-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30ca9-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30ca9-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="30ca9-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30ca9-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="30ca9-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ca9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="30ca9-121">Requirements</span></span>



| <span data-ttu-id="30ca9-122">需求</span><span class="sxs-lookup"><span data-stu-id="30ca9-122">Requirement</span></span> | <span data-ttu-id="30ca9-123">值</span><span class="sxs-lookup"><span data-stu-id="30ca9-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ca9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="30ca9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="30ca9-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="30ca9-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="30ca9-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="30ca9-126">Library</span></span><br/> | <dl> <span data-ttu-id="30ca9-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="30ca9-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="30ca9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30ca9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ca9-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="30ca9-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="30ca9-130">**GetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="30ca9-130">**GetFloatArray**</span></span>](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 

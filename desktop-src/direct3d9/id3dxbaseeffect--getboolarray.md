---
description: 取得 BOOL 值的陣列。
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: 'ID3DXBaseEffect：： GetBoolArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f714dfa91baba14524f12b6c3b2cb85211484cf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976745"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a><span data-ttu-id="75a8a-103">ID3DXBaseEffect：： GetBoolArray 方法</span><span class="sxs-lookup"><span data-stu-id="75a8a-103">ID3DXBaseEffect::GetBoolArray method</span></span>

<span data-ttu-id="75a8a-104">取得 BOOL 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="75a8a-104">Gets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a8a-105">語法</span><span class="sxs-lookup"><span data-stu-id="75a8a-105">Syntax</span></span>


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="75a8a-106">參數</span><span class="sxs-lookup"><span data-stu-id="75a8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a8a-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75a8a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a8a-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="75a8a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="75a8a-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="75a8a-109">Unique identifier.</span></span> <span data-ttu-id="75a8a-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="75a8a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="75a8a-111">*pB* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="75a8a-111">*pB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75a8a-112">類型： **[ **BOOL**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="75a8a-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="75a8a-113">傳回布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="75a8a-113">Returns an array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="75a8a-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75a8a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a8a-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75a8a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75a8a-116">陣列中的布林值數目。</span><span class="sxs-lookup"><span data-stu-id="75a8a-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a8a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="75a8a-117">Return value</span></span>

<span data-ttu-id="75a8a-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75a8a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75a8a-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="75a8a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="75a8a-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="75a8a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a8a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="75a8a-121">Requirements</span></span>



| <span data-ttu-id="75a8a-122">需求</span><span class="sxs-lookup"><span data-stu-id="75a8a-122">Requirement</span></span> | <span data-ttu-id="75a8a-123">值</span><span class="sxs-lookup"><span data-stu-id="75a8a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a8a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="75a8a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="75a8a-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="75a8a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="75a8a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="75a8a-126">Library</span></span><br/> | <dl> <span data-ttu-id="75a8a-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="75a8a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="75a8a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75a8a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a8a-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="75a8a-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="75a8a-130">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="75a8a-130">**SetBoolArray**</span></span>](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 

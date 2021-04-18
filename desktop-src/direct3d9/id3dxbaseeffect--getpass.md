---
description: 取得傳遞的控制碼。
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'ID3DXBaseEffect：： GetPass 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386520"
---
# <a name="id3dxbaseeffectgetpass-method"></a><span data-ttu-id="ffe3e-103">ID3DXBaseEffect：： GetPass 方法</span><span class="sxs-lookup"><span data-stu-id="ffe3e-103">ID3DXBaseEffect::GetPass method</span></span>

<span data-ttu-id="ffe3e-104">取得傳遞的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ffe3e-104">Gets the handle of a pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe3e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ffe3e-105">Syntax</span></span>


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="ffe3e-106">參數</span><span class="sxs-lookup"><span data-stu-id="ffe3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe3e-107">*hTechnique* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffe3e-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe3e-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ffe3e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ffe3e-109">父技術的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ffe3e-109">Handle of the parent technique.</span></span> <span data-ttu-id="ffe3e-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe3e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffe3e-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffe3e-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe3e-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ffe3e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ffe3e-113">傳遞的索引。</span><span class="sxs-lookup"><span data-stu-id="ffe3e-113">Index for the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe3e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffe3e-114">Return value</span></span>

<span data-ttu-id="ffe3e-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ffe3e-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ffe3e-116">傳回指定之技術內所指定傳遞的控制碼，如果索引無效，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ffe3e-116">Returns the handle of the specified pass inside the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="ffe3e-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe3e-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe3e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffe3e-118">Requirements</span></span>



| <span data-ttu-id="ffe3e-119">需求</span><span class="sxs-lookup"><span data-stu-id="ffe3e-119">Requirement</span></span> | <span data-ttu-id="ffe3e-120">值</span><span class="sxs-lookup"><span data-stu-id="ffe3e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe3e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ffe3e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ffe3e-122"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe3e-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ffe3e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="ffe3e-123">Library</span></span><br/> | <dl> <span data-ttu-id="ffe3e-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffe3e-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ffe3e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffe3e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe3e-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ffe3e-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

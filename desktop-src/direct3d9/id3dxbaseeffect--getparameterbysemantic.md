---
description: 藉由使用不區分大小寫的搜尋來查閱其語義，取得最上層參數或結構成員參數的控制碼。
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect：： GetParameterBySemantic 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323328"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a><span data-ttu-id="c9830-103">ID3DXBaseEffect：： GetParameterBySemantic 方法</span><span class="sxs-lookup"><span data-stu-id="c9830-103">ID3DXBaseEffect::GetParameterBySemantic method</span></span>

<span data-ttu-id="c9830-104">藉由使用不區分大小寫的搜尋來查閱其語義，取得最上層參數或結構成員參數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c9830-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its semantic with a case-insensitive search.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9830-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9830-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a><span data-ttu-id="c9830-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9830-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9830-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9830-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9830-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c9830-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c9830-109">參數的控制碼，或最上層參數的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c9830-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="c9830-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="c9830-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9830-111">*pSemantic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9830-111">*pSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9830-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9830-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9830-113">包含語義名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="c9830-113">String containing the semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9830-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9830-114">Return value</span></span>

<span data-ttu-id="c9830-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c9830-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c9830-116">傳回符合指定之語義的第一個參數的控制碼，如果找不到語義，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="c9830-116">Returns the handle of the first parameter that matches the specified semantic, or **NULL** if the semantic was not found.</span></span> <span data-ttu-id="c9830-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="c9830-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9830-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9830-118">Requirements</span></span>



| <span data-ttu-id="c9830-119">需求</span><span class="sxs-lookup"><span data-stu-id="c9830-119">Requirement</span></span> | <span data-ttu-id="c9830-120">值</span><span class="sxs-lookup"><span data-stu-id="c9830-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9830-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c9830-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c9830-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9830-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c9830-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9830-123">Library</span></span><br/> | <dl> <span data-ttu-id="c9830-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9830-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c9830-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9830-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9830-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c9830-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

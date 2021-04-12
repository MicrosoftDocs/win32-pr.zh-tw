---
description: 取得陣列元素參數的控制碼。
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'ID3DXBaseEffect：： GetParameterElement 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323327"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a><span data-ttu-id="4786c-103">ID3DXBaseEffect：： GetParameterElement 方法</span><span class="sxs-lookup"><span data-stu-id="4786c-103">ID3DXBaseEffect::GetParameterElement method</span></span>

<span data-ttu-id="4786c-104">取得陣列元素參數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4786c-104">Get the handle of an array element parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4786c-105">語法</span><span class="sxs-lookup"><span data-stu-id="4786c-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4786c-106">參數</span><span class="sxs-lookup"><span data-stu-id="4786c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4786c-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4786c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4786c-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4786c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4786c-109">陣列的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4786c-109">Handle of the array.</span></span> <span data-ttu-id="4786c-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="4786c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="4786c-111">*ElementIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4786c-111">*ElementIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4786c-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4786c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4786c-113">陣列元素索引。</span><span class="sxs-lookup"><span data-stu-id="4786c-113">Array element index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4786c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4786c-114">Return value</span></span>

<span data-ttu-id="4786c-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4786c-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4786c-116">傳回指定之參數的控制碼，如果 hParameter 或 ElementIndex 無效，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="4786c-116">Returns the handle of the specified parameter, or **NULL** if either hParameter or ElementIndex is invalid.</span></span> <span data-ttu-id="4786c-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="4786c-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4786c-118">備註</span><span class="sxs-lookup"><span data-stu-id="4786c-118">Remarks</span></span>

<span data-ttu-id="4786c-119">這個方法是用來取得屬於陣列之參數的元素。</span><span class="sxs-lookup"><span data-stu-id="4786c-119">This method is used to get an element of a parameter that is an array.</span></span>

## <a name="requirements"></a><span data-ttu-id="4786c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4786c-120">Requirements</span></span>



| <span data-ttu-id="4786c-121">需求</span><span class="sxs-lookup"><span data-stu-id="4786c-121">Requirement</span></span> | <span data-ttu-id="4786c-122">值</span><span class="sxs-lookup"><span data-stu-id="4786c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4786c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4786c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4786c-124"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="4786c-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4786c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4786c-125">Library</span></span><br/> | <dl> <span data-ttu-id="4786c-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4786c-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4786c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4786c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4786c-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="4786c-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

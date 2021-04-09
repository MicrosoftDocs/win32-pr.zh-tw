---
description: 取得最上層參數或結構成員參數的控制碼。
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect：： GetParameter 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035432"
---
# <a name="id3dxbaseeffectgetparameter-method"></a><span data-ttu-id="a2348-103">ID3DXBaseEffect：： GetParameter 方法</span><span class="sxs-lookup"><span data-stu-id="a2348-103">ID3DXBaseEffect::GetParameter method</span></span>

<span data-ttu-id="a2348-104">取得最上層參數或結構成員參數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a2348-104">Gets the handle of a top-level parameter or a structure member parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2348-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2348-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="a2348-106">參數</span><span class="sxs-lookup"><span data-stu-id="a2348-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2348-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2348-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2348-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a2348-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a2348-109">參數的控制碼，或最上層參數的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a2348-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="a2348-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="a2348-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2348-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2348-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2348-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2348-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2348-113">參數索引。</span><span class="sxs-lookup"><span data-stu-id="a2348-113">Parameter index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2348-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2348-114">Return value</span></span>

<span data-ttu-id="a2348-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a2348-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a2348-116">傳回指定之參數的控制碼，如果索引無效，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="a2348-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="a2348-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="a2348-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2348-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2348-118">Requirements</span></span>



| <span data-ttu-id="a2348-119">需求</span><span class="sxs-lookup"><span data-stu-id="a2348-119">Requirement</span></span> | <span data-ttu-id="a2348-120">值</span><span class="sxs-lookup"><span data-stu-id="a2348-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2348-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a2348-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a2348-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2348-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a2348-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2348-123">Library</span></span><br/> | <dl> <span data-ttu-id="a2348-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2348-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a2348-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2348-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2348-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a2348-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

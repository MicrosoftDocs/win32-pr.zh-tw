---
description: 藉由查詢名稱來取得技術的控制碼。
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'ID3DXBaseEffect：： GetTechniqueByName 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985915"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a><span data-ttu-id="c8eb4-103">ID3DXBaseEffect：： GetTechniqueByName 方法</span><span class="sxs-lookup"><span data-stu-id="c8eb4-103">ID3DXBaseEffect::GetTechniqueByName method</span></span>

<span data-ttu-id="c8eb4-104">藉由查詢名稱來取得技術的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-104">Gets the handle of a technique by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8eb4-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8eb4-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="c8eb4-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8eb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8eb4-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8eb4-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8eb4-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8eb4-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8eb4-109">包含技術名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-109">String containing the technique name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8eb4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8eb4-110">Return value</span></span>

<span data-ttu-id="c8eb4-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c8eb4-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c8eb4-112">傳回具有指定名稱之第一個技術的控制碼，如果找不到名稱，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-112">Returns the handle of the first technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="c8eb4-113">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8eb4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8eb4-114">Requirements</span></span>



| <span data-ttu-id="c8eb4-115">需求</span><span class="sxs-lookup"><span data-stu-id="c8eb4-115">Requirement</span></span> | <span data-ttu-id="c8eb4-116">值</span><span class="sxs-lookup"><span data-stu-id="c8eb4-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8eb4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="c8eb4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c8eb4-118"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8eb4-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c8eb4-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8eb4-119">Library</span></span><br/> | <dl> <span data-ttu-id="c8eb4-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8eb4-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c8eb4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8eb4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8eb4-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c8eb4-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

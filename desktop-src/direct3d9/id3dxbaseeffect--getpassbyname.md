---
description: 藉由查詢名稱來取得傳遞的控制碼。
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'ID3DXBaseEffect：： GetPassByName 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985727"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a><span data-ttu-id="05f6c-103">ID3DXBaseEffect：： GetPassByName 方法</span><span class="sxs-lookup"><span data-stu-id="05f6c-103">ID3DXBaseEffect::GetPassByName method</span></span>

<span data-ttu-id="05f6c-104">藉由查詢名稱來取得傳遞的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05f6c-104">Gets the handle of a pass by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f6c-105">語法</span><span class="sxs-lookup"><span data-stu-id="05f6c-105">Syntax</span></span>


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="05f6c-106">參數</span><span class="sxs-lookup"><span data-stu-id="05f6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f6c-107">*hTechnique* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05f6c-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f6c-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="05f6c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="05f6c-109">父技術的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05f6c-109">Handle of the parent technique.</span></span> <span data-ttu-id="05f6c-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="05f6c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="05f6c-111">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05f6c-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f6c-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05f6c-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05f6c-113">包含傳遞名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="05f6c-113">String containing the pass name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f6c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="05f6c-114">Return value</span></span>

<span data-ttu-id="05f6c-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="05f6c-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="05f6c-116">傳回具有指定名稱之指定技術內第一個傳遞的控制碼，如果找不到名稱，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="05f6c-116">Returns the handle of the first pass inside the specified technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="05f6c-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="05f6c-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05f6c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f6c-118">Requirements</span></span>



| <span data-ttu-id="05f6c-119">需求</span><span class="sxs-lookup"><span data-stu-id="05f6c-119">Requirement</span></span> | <span data-ttu-id="05f6c-120">值</span><span class="sxs-lookup"><span data-stu-id="05f6c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f6c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="05f6c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="05f6c-122"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="05f6c-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="05f6c-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="05f6c-123">Library</span></span><br/> | <dl> <span data-ttu-id="05f6c-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="05f6c-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="05f6c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05f6c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f6c-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="05f6c-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

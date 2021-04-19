---
description: 取得注釋的控制碼。
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'ID3DXBaseEffect：： GetAnnotation 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001795"
---
# <a name="id3dxbaseeffectgetannotation-method"></a><span data-ttu-id="97f53-103">ID3DXBaseEffect：： GetAnnotation 方法</span><span class="sxs-lookup"><span data-stu-id="97f53-103">ID3DXBaseEffect::GetAnnotation method</span></span>

<span data-ttu-id="97f53-104">取得注釋的控制碼。</span><span class="sxs-lookup"><span data-stu-id="97f53-104">Gets the handle of an annotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f53-105">語法</span><span class="sxs-lookup"><span data-stu-id="97f53-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="97f53-106">參數</span><span class="sxs-lookup"><span data-stu-id="97f53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97f53-107">*hObject* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97f53-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f53-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="97f53-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="97f53-109">技術、傳遞或最上層參數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="97f53-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="97f53-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="97f53-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="97f53-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97f53-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f53-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97f53-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97f53-113">批註索引。</span><span class="sxs-lookup"><span data-stu-id="97f53-113">Annotation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97f53-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="97f53-114">Return value</span></span>

<span data-ttu-id="97f53-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="97f53-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="97f53-116">傳回指定之注釋的控制碼，如果索引無效，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="97f53-116">Returns the handle of the specified annotation, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="97f53-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="97f53-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97f53-118">備註</span><span class="sxs-lookup"><span data-stu-id="97f53-118">Remarks</span></span>

<span data-ttu-id="97f53-119">批註是使用者特定的資料，可附加至任何技術、傳遞或參數。</span><span class="sxs-lookup"><span data-stu-id="97f53-119">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="97f53-120">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="97f53-120">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97f53-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="97f53-121">Requirements</span></span>



| <span data-ttu-id="97f53-122">需求</span><span class="sxs-lookup"><span data-stu-id="97f53-122">Requirement</span></span> | <span data-ttu-id="97f53-123">值</span><span class="sxs-lookup"><span data-stu-id="97f53-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97f53-124">標頭</span><span class="sxs-lookup"><span data-stu-id="97f53-124">Header</span></span><br/>  | <dl> <span data-ttu-id="97f53-125"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="97f53-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="97f53-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="97f53-126">Library</span></span><br/> | <dl> <span data-ttu-id="97f53-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97f53-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="97f53-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97f53-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f53-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="97f53-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

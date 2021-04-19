---
description: 藉由查詢名稱來取得批註的控制碼。
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'ID3DXBaseEffect：： GetAnnotationByName 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981858"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a><span data-ttu-id="08c40-103">ID3DXBaseEffect：： GetAnnotationByName 方法</span><span class="sxs-lookup"><span data-stu-id="08c40-103">ID3DXBaseEffect::GetAnnotationByName method</span></span>

<span data-ttu-id="08c40-104">藉由查詢名稱來取得批註的控制碼。</span><span class="sxs-lookup"><span data-stu-id="08c40-104">Gets the handle of an annotation by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c40-105">語法</span><span class="sxs-lookup"><span data-stu-id="08c40-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="08c40-106">參數</span><span class="sxs-lookup"><span data-stu-id="08c40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c40-107">*hObject* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08c40-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c40-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="08c40-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="08c40-109">技術、傳遞或最上層參數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="08c40-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="08c40-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="08c40-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="08c40-111">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08c40-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c40-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08c40-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08c40-113">包含批註名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="08c40-113">String containing the annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c40-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="08c40-114">Return value</span></span>

<span data-ttu-id="08c40-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="08c40-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="08c40-116">傳回指定之注釋的控制碼，如果找不到名稱，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="08c40-116">Returns the handle of the specified annotation, or **NULL** if the name was not found.</span></span> <span data-ttu-id="08c40-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="08c40-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08c40-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="08c40-118">Requirements</span></span>



| <span data-ttu-id="08c40-119">需求</span><span class="sxs-lookup"><span data-stu-id="08c40-119">Requirement</span></span> | <span data-ttu-id="08c40-120">值</span><span class="sxs-lookup"><span data-stu-id="08c40-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c40-121">標頭</span><span class="sxs-lookup"><span data-stu-id="08c40-121">Header</span></span><br/>  | <dl> <span data-ttu-id="08c40-122"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="08c40-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="08c40-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="08c40-123">Library</span></span><br/> | <dl> <span data-ttu-id="08c40-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="08c40-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="08c40-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08c40-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c40-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="08c40-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

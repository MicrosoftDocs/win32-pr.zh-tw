---
description: 取得頂點宣告。
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'ID3DXSkinInfo：： GetDeclaration 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322603"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="6fdb8-103">ID3DXSkinInfo：： GetDeclaration 方法</span><span class="sxs-lookup"><span data-stu-id="6fdb8-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="6fdb8-104">取得頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="6fdb8-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdb8-105">語法</span><span class="sxs-lookup"><span data-stu-id="6fdb8-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="6fdb8-106">參數</span><span class="sxs-lookup"><span data-stu-id="6fdb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fdb8-107">宣告 \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6fdb8-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fdb8-108">類型： **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="6fdb8-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="6fdb8-109">描述網格頂點頂點格式的 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 元素陣列。</span><span class="sxs-lookup"><span data-stu-id="6fdb8-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="6fdb8-110">此宣告子陣列的上限是 [**\_ FVF \_ DECL \_ SIZE 的最大**](./max-fvf-decl-size.md)值。</span><span class="sxs-lookup"><span data-stu-id="6fdb8-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="6fdb8-111">頂點元素陣列的結尾是 [**D3DDECL \_ END**](d3ddecl-end.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="6fdb8-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fdb8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6fdb8-112">Return value</span></span>

<span data-ttu-id="6fdb8-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6fdb8-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6fdb8-114">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6fdb8-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6fdb8-115">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="6fdb8-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fdb8-116">備註</span><span class="sxs-lookup"><span data-stu-id="6fdb8-116">Remarks</span></span>

<span data-ttu-id="6fdb8-117">專案的陣列包含結束宣告的 [**D3DDECL \_ 結束**](d3ddecl-end.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="6fdb8-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fdb8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fdb8-118">Requirements</span></span>



| <span data-ttu-id="6fdb8-119">需求</span><span class="sxs-lookup"><span data-stu-id="6fdb8-119">Requirement</span></span> | <span data-ttu-id="6fdb8-120">值</span><span class="sxs-lookup"><span data-stu-id="6fdb8-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdb8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6fdb8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6fdb8-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdb8-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6fdb8-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="6fdb8-123">Library</span></span><br/> | <dl> <span data-ttu-id="6fdb8-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fdb8-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6fdb8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fdb8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fdb8-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="6fdb8-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="6fdb8-127">**ID3DXSkinInfo::SetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="6fdb8-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 

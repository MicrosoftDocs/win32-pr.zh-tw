---
description: 此常數是網格之頂點宣告子的最大數目。
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: 'MAX_FVF_DECL_SIZE 列舉 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982204"
---
# <a name="max_fvf_decl_size-enumeration"></a><span data-ttu-id="30a94-103">最大 \_ FVF \_ DECL \_ 大小列舉</span><span class="sxs-lookup"><span data-stu-id="30a94-103">MAX\_FVF\_DECL\_SIZE enumeration</span></span>

<span data-ttu-id="30a94-104">此常數是網格之頂點宣告子的最大數目。</span><span class="sxs-lookup"><span data-stu-id="30a94-104">This constant is the maximum number of vertex declarators for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a94-105">Syntax</span></span>


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a><span data-ttu-id="30a94-106">常數</span><span class="sxs-lookup"><span data-stu-id="30a94-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30a94-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**最大 \_ FVF \_ DECL \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="30a94-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**MAX\_FVF\_DECL\_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="30a94-108">頂點宣告中的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="30a94-108">The maximum number of elements in the vertex declaration.</span></span> <span data-ttu-id="30a94-109">額外的 (+ 1) 適用于 [**D3DDECL \_ END**](d3ddecl-end.md)。</span><span class="sxs-lookup"><span data-stu-id="30a94-109">The additional (+1) is for [**D3DDECL\_END**](d3ddecl-end.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30a94-110">備註</span><span class="sxs-lookup"><span data-stu-id="30a94-110">Remarks</span></span>

<span data-ttu-id="30a94-111">MAXD3DDECLLENGTH 定義為最多 64 (請參閱 d3d9types) 。</span><span class="sxs-lookup"><span data-stu-id="30a94-111">MAXD3DDECLLENGTH is defined as a maximum of 64 (see d3d9types.h).</span></span> <span data-ttu-id="30a94-112">這不包含 "end" 標記頂點元素。</span><span class="sxs-lookup"><span data-stu-id="30a94-112">This does not include the "end" marker vertex element.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a94-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="30a94-113">Requirements</span></span>



| <span data-ttu-id="30a94-114">需求</span><span class="sxs-lookup"><span data-stu-id="30a94-114">Requirement</span></span> | <span data-ttu-id="30a94-115">值</span><span class="sxs-lookup"><span data-stu-id="30a94-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30a94-116">標頭</span><span class="sxs-lookup"><span data-stu-id="30a94-116">Header</span></span><br/> | <dl> <span data-ttu-id="30a94-117"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="30a94-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a94-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30a94-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a94-119">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="30a94-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="30a94-120">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="30a94-120">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="30a94-121">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="30a94-121">**GetDeclaration**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[<span data-ttu-id="30a94-122">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="30a94-122">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[<span data-ttu-id="30a94-123">**ID3DXSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="30a94-123">**ID3DXSkinInfo**</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

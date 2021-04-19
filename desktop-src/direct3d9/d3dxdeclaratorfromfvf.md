---
description: 從彈性頂點格式傳回宣告子 (FVF) 程式碼。
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: 'D3DXDeclaratorFromFVF 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986516"
---
# <a name="d3dxdeclaratorfromfvf-function"></a><span data-ttu-id="66c37-103">D3DXDeclaratorFromFVF 函式</span><span class="sxs-lookup"><span data-stu-id="66c37-103">D3DXDeclaratorFromFVF function</span></span>

<span data-ttu-id="66c37-104">從彈性頂點格式傳回宣告子 (FVF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="66c37-104">Returns a declarator from a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c37-105">語法</span><span class="sxs-lookup"><span data-stu-id="66c37-105">Syntax</span></span>


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="66c37-106">參數</span><span class="sxs-lookup"><span data-stu-id="66c37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c37-107">*FVF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66c37-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c37-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66c37-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66c37-109">描述要從中產生所傳回宣告子陣列之 FVF 的 [D3DFVF](d3dfvf.md) 組合。</span><span class="sxs-lookup"><span data-stu-id="66c37-109">Combination of [D3DFVF](d3dfvf.md) that describes the FVF from which to generate the returned declarator array.</span></span>

</dd> <dt>

<span data-ttu-id="66c37-110">宣告 \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="66c37-110">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="66c37-111">類型： **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="66c37-111">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="66c37-112">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述網格頂點的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="66c37-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="66c37-113">此宣告子陣列的上限是 [**\_ FVF \_ DECL \_ SIZE 的最大**](./max-fvf-decl-size.md)值。</span><span class="sxs-lookup"><span data-stu-id="66c37-113">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c37-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="66c37-114">Return value</span></span>

<span data-ttu-id="66c37-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66c37-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66c37-116">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="66c37-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="66c37-117">如果函式失敗，則傳回值可以是下列其中一項： D3DXERR \_ INVALIDMESH。</span><span class="sxs-lookup"><span data-stu-id="66c37-117">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c37-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="66c37-118">Requirements</span></span>



| <span data-ttu-id="66c37-119">需求</span><span class="sxs-lookup"><span data-stu-id="66c37-119">Requirement</span></span> | <span data-ttu-id="66c37-120">值</span><span class="sxs-lookup"><span data-stu-id="66c37-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66c37-121">標頭</span><span class="sxs-lookup"><span data-stu-id="66c37-121">Header</span></span><br/>  | <dl> <span data-ttu-id="66c37-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="66c37-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="66c37-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="66c37-123">Library</span></span><br/> | <dl> <span data-ttu-id="66c37-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66c37-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66c37-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66c37-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c37-126">網格函數</span><span class="sxs-lookup"><span data-stu-id="66c37-126">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="66c37-127">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="66c37-127">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 

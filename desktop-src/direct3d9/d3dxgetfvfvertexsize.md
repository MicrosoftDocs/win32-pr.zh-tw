---
description: 傳回 (FVF) 的彈性頂點格式頂點的大小。
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: 'D3DXGetFVFVertexSize 函式 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986513"
---
# <a name="d3dxgetfvfvertexsize-function"></a><span data-ttu-id="206d9-103">D3DXGetFVFVertexSize 函式</span><span class="sxs-lookup"><span data-stu-id="206d9-103">D3DXGetFVFVertexSize function</span></span>

<span data-ttu-id="206d9-104">傳回 (FVF) 的彈性頂點格式頂點的大小。</span><span class="sxs-lookup"><span data-stu-id="206d9-104">Returns the size of a vertex for a flexible vertex format (FVF).</span></span>

## <a name="syntax"></a><span data-ttu-id="206d9-105">語法</span><span class="sxs-lookup"><span data-stu-id="206d9-105">Syntax</span></span>


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="206d9-106">參數</span><span class="sxs-lookup"><span data-stu-id="206d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="206d9-107">*FVF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="206d9-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206d9-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206d9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206d9-109">要查詢的 FVF。</span><span class="sxs-lookup"><span data-stu-id="206d9-109">FVF to be queried.</span></span> <span data-ttu-id="206d9-110">[D3DFVF](d3dfvf.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="206d9-110">A combination of [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="206d9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="206d9-111">Return value</span></span>

<span data-ttu-id="206d9-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206d9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206d9-113">FVF 頂點大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="206d9-113">The FVF vertex size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="206d9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="206d9-114">Requirements</span></span>



| <span data-ttu-id="206d9-115">需求</span><span class="sxs-lookup"><span data-stu-id="206d9-115">Requirement</span></span> | <span data-ttu-id="206d9-116">值</span><span class="sxs-lookup"><span data-stu-id="206d9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="206d9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="206d9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="206d9-118"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="206d9-118"><dt>D3dx9mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="206d9-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="206d9-119">Library</span></span><br/> | <dl> <span data-ttu-id="206d9-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="206d9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="206d9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="206d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206d9-122">網格函數</span><span class="sxs-lookup"><span data-stu-id="206d9-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

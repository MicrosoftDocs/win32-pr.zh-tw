---
description: D3DXMatrixDeterminant 函數 (D3dx9math) -傳回矩陣的行列式。
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: 'D3DXMatrixDeterminant 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d54651e11f1b3de02803d9ea123ca7eff24d7a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098166"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="f7bf5-103">D3DXMatrixDeterminant 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="f7bf5-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="f7bf5-104">傳回矩陣的行列式。</span><span class="sxs-lookup"><span data-stu-id="f7bf5-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7bf5-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7bf5-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f7bf5-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7bf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7bf5-107">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7bf5-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7bf5-108">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7bf5-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f7bf5-109">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f7bf5-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7bf5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7bf5-110">Return value</span></span>

<span data-ttu-id="f7bf5-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7bf5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7bf5-112">傳回矩陣的行列式。</span><span class="sxs-lookup"><span data-stu-id="f7bf5-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7bf5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7bf5-113">Requirements</span></span>



| <span data-ttu-id="f7bf5-114">需求</span><span class="sxs-lookup"><span data-stu-id="f7bf5-114">Requirement</span></span> | <span data-ttu-id="f7bf5-115">值</span><span class="sxs-lookup"><span data-stu-id="f7bf5-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bf5-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f7bf5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f7bf5-117"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7bf5-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f7bf5-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7bf5-118">Library</span></span><br/> | <dl> <span data-ttu-id="f7bf5-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7bf5-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7bf5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7bf5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7bf5-121">數學函數</span><span class="sxs-lookup"><span data-stu-id="f7bf5-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

---
description: D3DXMatrixDeterminant 函數 (D3DX10Math) -傳回矩陣的行列式。
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: 'D3DXMatrixDeterminant 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103456"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="f670d-103">D3DXMatrixDeterminant 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="f670d-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="f670d-104">傳回矩陣的行列式。</span><span class="sxs-lookup"><span data-stu-id="f670d-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f670d-105">語法</span><span class="sxs-lookup"><span data-stu-id="f670d-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f670d-106">參數</span><span class="sxs-lookup"><span data-stu-id="f670d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f670d-107">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f670d-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f670d-108">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f670d-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f670d-109">來源 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f670d-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f670d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f670d-110">Return value</span></span>

<span data-ttu-id="f670d-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f670d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f670d-112">傳回矩陣的行列式。</span><span class="sxs-lookup"><span data-stu-id="f670d-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f670d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f670d-113">Requirements</span></span>



| <span data-ttu-id="f670d-114">需求</span><span class="sxs-lookup"><span data-stu-id="f670d-114">Requirement</span></span> | <span data-ttu-id="f670d-115">值</span><span class="sxs-lookup"><span data-stu-id="f670d-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f670d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f670d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f670d-117"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f670d-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f670d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f670d-118">Library</span></span><br/> | <dl> <span data-ttu-id="f670d-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f670d-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f670d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f670d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f670d-121">數學函數</span><span class="sxs-lookup"><span data-stu-id="f670d-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

---
description: 建立識別矩陣。
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: 'D3DXMatrixIdentity 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946046"
---
# <a name="d3dxmatrixidentity-function"></a><span data-ttu-id="9ff70-103">D3DXMatrixIdentity 函式</span><span class="sxs-lookup"><span data-stu-id="9ff70-103">D3DXMatrixIdentity function</span></span>

<span data-ttu-id="9ff70-104">建立識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="9ff70-104">Creates an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff70-105">語法</span><span class="sxs-lookup"><span data-stu-id="9ff70-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="9ff70-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ff70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff70-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9ff70-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff70-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ff70-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9ff70-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="9ff70-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff70-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ff70-110">Return value</span></span>

<span data-ttu-id="9ff70-111">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ff70-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9ff70-112">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，該結構為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="9ff70-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the identity matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff70-113">備註</span><span class="sxs-lookup"><span data-stu-id="9ff70-113">Remarks</span></span>

<span data-ttu-id="9ff70-114">識別矩陣是一個矩陣，其中所有係數都是0，但 \[ 1、1 \] \[ 2、2 \] \[ 3、3 \] \[ 4、4個 \] 係數設定為1。</span><span class="sxs-lookup"><span data-stu-id="9ff70-114">The identity matrix is a matrix in which all coefficients are 0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.</span></span> <span data-ttu-id="9ff70-115">識別矩陣的特殊之處，就是當它套用至頂點時，不會變更。</span><span class="sxs-lookup"><span data-stu-id="9ff70-115">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="9ff70-116">身分識別矩陣可作為矩陣的起點，以修改頂點值以建立旋轉、轉譯，以及可由4個4個4個矩陣表示的任何其他轉換。</span><span class="sxs-lookup"><span data-stu-id="9ff70-116">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4 x4 matrix.</span></span>

<span data-ttu-id="9ff70-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="9ff70-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9ff70-118">如此一來， **D3DXMatrixIdentity** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="9ff70-118">In this way, the **D3DXMatrixIdentity** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff70-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ff70-119">Requirements</span></span>



| <span data-ttu-id="9ff70-120">需求</span><span class="sxs-lookup"><span data-stu-id="9ff70-120">Requirement</span></span> | <span data-ttu-id="9ff70-121">值</span><span class="sxs-lookup"><span data-stu-id="9ff70-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff70-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9ff70-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9ff70-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff70-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9ff70-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9ff70-124">Library</span></span><br/> | <dl> <span data-ttu-id="9ff70-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ff70-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ff70-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ff70-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff70-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="9ff70-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9ff70-128">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="9ff70-128">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
</dt> </dl>

 

 





---
description: 判斷矩陣是否為識別矩陣。
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: 'D3DXMatrixIsIdentity 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323151"
---
# <a name="d3dxmatrixisidentity-function"></a><span data-ttu-id="def71-103">D3DXMatrixIsIdentity 函式</span><span class="sxs-lookup"><span data-stu-id="def71-103">D3DXMatrixIsIdentity function</span></span>

<span data-ttu-id="def71-104">判斷矩陣是否為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="def71-104">Determines if a matrix is an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="def71-105">語法</span><span class="sxs-lookup"><span data-stu-id="def71-105">Syntax</span></span>


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="def71-106">參數</span><span class="sxs-lookup"><span data-stu-id="def71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def71-107">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="def71-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def71-108">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="def71-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="def71-109">將針對身分識別進行測試的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="def71-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def71-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="def71-110">Return value</span></span>

<span data-ttu-id="def71-111">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def71-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def71-112">如果矩陣是識別矩陣，此函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="def71-112">If the matrix is an identity matrix, this function returns **TRUE**.</span></span> <span data-ttu-id="def71-113">否則，此函式會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="def71-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="def71-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="def71-114">Requirements</span></span>



| <span data-ttu-id="def71-115">需求</span><span class="sxs-lookup"><span data-stu-id="def71-115">Requirement</span></span> | <span data-ttu-id="def71-116">值</span><span class="sxs-lookup"><span data-stu-id="def71-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="def71-117">標頭</span><span class="sxs-lookup"><span data-stu-id="def71-117">Header</span></span><br/>  | <dl> <span data-ttu-id="def71-118"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="def71-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="def71-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="def71-119">Library</span></span><br/> | <dl> <span data-ttu-id="def71-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="def71-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="def71-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="def71-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def71-122">數學函數</span><span class="sxs-lookup"><span data-stu-id="def71-122">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="def71-123">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="def71-123">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
</dt> </dl>

 

 

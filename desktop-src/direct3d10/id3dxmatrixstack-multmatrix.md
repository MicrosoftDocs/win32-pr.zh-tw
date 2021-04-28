---
description: ID3DXMATRIXStack：： MultMatrix 方法 (D3DX10 .h) -決定目前矩陣和指定矩陣的乘積。
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'ID3DXMATRIXStack：： MultMatrix 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 969cdebcee34add15cbf6bbcfbb1048387b2d7e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107966"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="43b59-103">ID3DXMATRIXStack：： MultMatrix 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="43b59-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="43b59-104">決定目前矩陣和指定矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="43b59-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b59-105">語法</span><span class="sxs-lookup"><span data-stu-id="43b59-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="43b59-106">參數</span><span class="sxs-lookup"><span data-stu-id="43b59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43b59-107">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43b59-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b59-108">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="43b59-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="43b59-109">要乘以目前矩陣的 D3DXMATRIX 結構指標。</span><span class="sxs-lookup"><span data-stu-id="43b59-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43b59-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="43b59-110">Return value</span></span>

<span data-ttu-id="43b59-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43b59-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43b59-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="43b59-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="43b59-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="43b59-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="43b59-114">備註</span><span class="sxs-lookup"><span data-stu-id="43b59-114">Remarks</span></span>

<span data-ttu-id="43b59-115">這個方法會將指定的矩陣靠右乘以目前的矩陣 (轉換與目前的世界原點) 有關。</span><span class="sxs-lookup"><span data-stu-id="43b59-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="43b59-116">這個方法不會將專案加入至堆疊中，它會將目前的矩陣取代為目前矩陣和指定矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="43b59-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="43b59-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="43b59-117">Requirements</span></span>



| <span data-ttu-id="43b59-118">需求</span><span class="sxs-lookup"><span data-stu-id="43b59-118">Requirement</span></span> | <span data-ttu-id="43b59-119">值</span><span class="sxs-lookup"><span data-stu-id="43b59-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43b59-120">標頭</span><span class="sxs-lookup"><span data-stu-id="43b59-120">Header</span></span><br/>  | <dl> <span data-ttu-id="43b59-121"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="43b59-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="43b59-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="43b59-122">Library</span></span><br/> | <dl> <span data-ttu-id="43b59-123"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43b59-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b59-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43b59-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b59-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="43b59-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="43b59-126">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="43b59-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

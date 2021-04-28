---
description: ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3DX10 .h) -決定給定矩陣和目前矩陣的乘積。
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107946"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="2974f-103">ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="2974f-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="2974f-104">決定給定矩陣和目前矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="2974f-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2974f-105">語法</span><span class="sxs-lookup"><span data-stu-id="2974f-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2974f-106">參數</span><span class="sxs-lookup"><span data-stu-id="2974f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2974f-107">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2974f-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2974f-108">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2974f-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2974f-109">要乘以目前矩陣的 D3DXMATRIX 結構指標。</span><span class="sxs-lookup"><span data-stu-id="2974f-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2974f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2974f-110">Return value</span></span>

<span data-ttu-id="2974f-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2974f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2974f-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2974f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2974f-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2974f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2974f-114">備註</span><span class="sxs-lookup"><span data-stu-id="2974f-114">Remarks</span></span>

<span data-ttu-id="2974f-115">這個方法會將指定的矩陣靠左乘以目前的矩陣 (轉換是關於物件) 的本機來源。</span><span class="sxs-lookup"><span data-stu-id="2974f-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="2974f-116">這個方法不會將專案加入至堆疊中，它會將目前的矩陣取代為指定矩陣和目前矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="2974f-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2974f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2974f-117">Requirements</span></span>



| <span data-ttu-id="2974f-118">需求</span><span class="sxs-lookup"><span data-stu-id="2974f-118">Requirement</span></span> | <span data-ttu-id="2974f-119">值</span><span class="sxs-lookup"><span data-stu-id="2974f-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2974f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2974f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2974f-121"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="2974f-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2974f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="2974f-122">Library</span></span><br/> | <dl> <span data-ttu-id="2974f-123"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2974f-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2974f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2974f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2974f-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2974f-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2974f-126">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="2974f-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

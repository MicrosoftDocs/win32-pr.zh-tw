---
description: ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3dx9math .h) -決定給定矩陣和目前矩陣的乘積。
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3dx9math .h) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 509aff4dd21f62033dc1e4672d29aad57445f9ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093516"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a><span data-ttu-id="dd1f5-103">ID3DXMATRIXStack：： MultMatrixLocal 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="dd1f5-103">ID3DXMATRIXStack::MultMatrixLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="dd1f5-104">決定給定矩陣和目前矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="dd1f5-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd1f5-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="dd1f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd1f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd1f5-107">*pMat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dd1f5-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1f5-108">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="dd1f5-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dd1f5-109">要乘以目前矩陣的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="dd1f5-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd1f5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd1f5-110">Return value</span></span>

<span data-ttu-id="dd1f5-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd1f5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd1f5-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="dd1f5-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dd1f5-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="dd1f5-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd1f5-114">備註</span><span class="sxs-lookup"><span data-stu-id="dd1f5-114">Remarks</span></span>

<span data-ttu-id="dd1f5-115">這個方法會將指定的矩陣靠左乘以目前的矩陣 (轉換是關於物件) 的本機來源。</span><span class="sxs-lookup"><span data-stu-id="dd1f5-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="dd1f5-116">這個方法不會將專案加入至堆疊中，它會將目前的矩陣取代為指定矩陣和目前矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="dd1f5-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1f5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd1f5-117">Requirements</span></span>



| <span data-ttu-id="dd1f5-118">需求</span><span class="sxs-lookup"><span data-stu-id="dd1f5-118">Requirement</span></span> | <span data-ttu-id="dd1f5-119">值</span><span class="sxs-lookup"><span data-stu-id="dd1f5-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1f5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="dd1f5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dd1f5-121"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd1f5-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dd1f5-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="dd1f5-122">Library</span></span><br/> | <dl> <span data-ttu-id="dd1f5-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd1f5-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd1f5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd1f5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1f5-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="dd1f5-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="dd1f5-126">**ID3DXMATRIXStack::MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="dd1f5-126">**ID3DXMATRIXStack::MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 





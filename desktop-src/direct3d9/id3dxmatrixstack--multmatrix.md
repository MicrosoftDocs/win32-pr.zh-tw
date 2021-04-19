---
description: 決定目前矩陣和指定矩陣的乘積。
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'ID3DXMATRIXStack：： MultMatrix 方法 (D3dx9math .h) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fc9b3fb49387e354645c8a3c09c7572b4da80109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986500"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a><span data-ttu-id="85a1f-103">ID3DXMATRIXStack：： MultMatrix 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="85a1f-103">ID3DXMATRIXStack::MultMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="85a1f-104">決定目前矩陣和指定矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="85a1f-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a1f-105">語法</span><span class="sxs-lookup"><span data-stu-id="85a1f-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="85a1f-106">參數</span><span class="sxs-lookup"><span data-stu-id="85a1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a1f-107">*pMat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85a1f-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a1f-108">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="85a1f-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="85a1f-109">要乘以目前矩陣的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="85a1f-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a1f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="85a1f-110">Return value</span></span>

<span data-ttu-id="85a1f-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85a1f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85a1f-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="85a1f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="85a1f-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="85a1f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="85a1f-114">備註</span><span class="sxs-lookup"><span data-stu-id="85a1f-114">Remarks</span></span>

<span data-ttu-id="85a1f-115">這個方法會將指定的矩陣靠右乘以目前的矩陣 (轉換與目前的世界原點) 有關。</span><span class="sxs-lookup"><span data-stu-id="85a1f-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="85a1f-116">這個方法不會將專案加入至堆疊中，它會將目前的矩陣取代為目前矩陣和指定矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="85a1f-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="85a1f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="85a1f-117">Requirements</span></span>



| <span data-ttu-id="85a1f-118">需求</span><span class="sxs-lookup"><span data-stu-id="85a1f-118">Requirement</span></span> | <span data-ttu-id="85a1f-119">值</span><span class="sxs-lookup"><span data-stu-id="85a1f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85a1f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="85a1f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="85a1f-121"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="85a1f-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="85a1f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="85a1f-122">Library</span></span><br/> | <dl> <span data-ttu-id="85a1f-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="85a1f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85a1f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85a1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a1f-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="85a1f-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="85a1f-126">**ID3DXMATRIXStack::MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="85a1f-126">**ID3DXMATRIXStack::MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 





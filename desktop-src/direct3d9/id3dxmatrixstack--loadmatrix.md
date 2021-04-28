---
description: ID3DXMATRIXStack：： LoadMatrix 方法 (D3dx9math .h) -將指定的矩陣載入至目前的矩陣。
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'ID3DXMATRIXStack：： LoadMatrix 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2ee7e5cae4d28b81b805faa4f113d0819f1eae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093536"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="e441e-103">ID3DXMATRIXStack：： LoadMatrix 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="e441e-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="e441e-104">將指定的矩陣載入至目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e441e-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e441e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e441e-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="e441e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e441e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e441e-107">*pMat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e441e-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e441e-108">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e441e-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e441e-109">載入至目前矩陣的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="e441e-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e441e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e441e-110">Return value</span></span>

<span data-ttu-id="e441e-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e441e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e441e-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e441e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e441e-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="e441e-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e441e-114">備註</span><span class="sxs-lookup"><span data-stu-id="e441e-114">Remarks</span></span>

<span data-ttu-id="e441e-115">請注意，這個方法不會將專案新增至堆疊。相反地，它會將目前的矩陣取代為提供的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e441e-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e441e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e441e-116">Requirements</span></span>



| <span data-ttu-id="e441e-117">需求</span><span class="sxs-lookup"><span data-stu-id="e441e-117">Requirement</span></span> | <span data-ttu-id="e441e-118">值</span><span class="sxs-lookup"><span data-stu-id="e441e-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e441e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e441e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e441e-120"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e441e-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e441e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e441e-121">Library</span></span><br/> | <dl> <span data-ttu-id="e441e-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e441e-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e441e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e441e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e441e-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e441e-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e441e-125">**ID3DXMATRIXStack::LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="e441e-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 





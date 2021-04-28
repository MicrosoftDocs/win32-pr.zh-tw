---
description: ID3DXMATRIXStack：:P ush 方法 (D3dx9math) -將矩陣新增至堆疊。
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: 'ID3DXMATRIXStack：:P ush 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093499"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="c3cf3-103">ID3DXMATRIXStack：:P ush 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="c3cf3-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="c3cf3-104">將矩陣加入至堆疊。</span><span class="sxs-lookup"><span data-stu-id="c3cf3-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cf3-105">語法</span><span class="sxs-lookup"><span data-stu-id="c3cf3-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="c3cf3-106">參數</span><span class="sxs-lookup"><span data-stu-id="c3cf3-106">Parameters</span></span>

<span data-ttu-id="c3cf3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c3cf3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3cf3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3cf3-108">Return value</span></span>

<span data-ttu-id="c3cf3-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3cf3-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3cf3-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c3cf3-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3cf3-111">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c3cf3-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3cf3-112">備註</span><span class="sxs-lookup"><span data-stu-id="c3cf3-112">Remarks</span></span>

<span data-ttu-id="c3cf3-113">這個方法會將堆疊上的專案計數遞增1，以複製目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c3cf3-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="c3cf3-114">隨著新增更多專案，堆疊會動態地成長。</span><span class="sxs-lookup"><span data-stu-id="c3cf3-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cf3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3cf3-115">Requirements</span></span>



| <span data-ttu-id="c3cf3-116">需求</span><span class="sxs-lookup"><span data-stu-id="c3cf3-116">Requirement</span></span> | <span data-ttu-id="c3cf3-117">值</span><span class="sxs-lookup"><span data-stu-id="c3cf3-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cf3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c3cf3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c3cf3-119"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3cf3-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c3cf3-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3cf3-120">Library</span></span><br/> | <dl> <span data-ttu-id="c3cf3-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3cf3-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3cf3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3cf3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cf3-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="c3cf3-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c3cf3-124">**ID3DXMATRIXStack：： Vemap.gettop**</span><span class="sxs-lookup"><span data-stu-id="c3cf3-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="c3cf3-125">**ID3DXMATRIXStack：:P op**</span><span class="sxs-lookup"><span data-stu-id="c3cf3-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 





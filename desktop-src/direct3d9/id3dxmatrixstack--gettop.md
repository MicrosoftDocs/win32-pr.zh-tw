---
description: 抓取堆疊頂端的目前矩陣。
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack：： Vemap.gettop 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977131"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="6b13a-103">ID3DXMATRIXStack：： Vemap.gettop 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="6b13a-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="6b13a-104">抓取堆疊頂端的目前矩陣。</span><span class="sxs-lookup"><span data-stu-id="6b13a-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b13a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b13a-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="6b13a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b13a-106">Parameters</span></span>

<span data-ttu-id="6b13a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6b13a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b13a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b13a-108">Return value</span></span>

<span data-ttu-id="6b13a-109">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b13a-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6b13a-110">這個方法會傳回 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標，代表目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="6b13a-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b13a-111">備註</span><span class="sxs-lookup"><span data-stu-id="6b13a-111">Remarks</span></span>

<span data-ttu-id="6b13a-112">在後續的堆疊作業之後，這個方法所傳回的 [**D3DXMATRIX**](d3dxmatrix.md) 指標不保證是有效的。</span><span class="sxs-lookup"><span data-stu-id="6b13a-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="6b13a-113">請注意，此方法不會從堆疊頂端移除目前的矩陣;相反地，它只會傳回目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="6b13a-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b13a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b13a-114">Requirements</span></span>



| <span data-ttu-id="6b13a-115">需求</span><span class="sxs-lookup"><span data-stu-id="6b13a-115">Requirement</span></span> | <span data-ttu-id="6b13a-116">值</span><span class="sxs-lookup"><span data-stu-id="6b13a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b13a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6b13a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6b13a-118"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b13a-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6b13a-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b13a-119">Library</span></span><br/> | <dl> <span data-ttu-id="6b13a-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b13a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b13a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b13a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b13a-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="6b13a-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="6b13a-123">**ID3DXMATRIXStack：:P op**</span><span class="sxs-lookup"><span data-stu-id="6b13a-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="6b13a-124">**ID3DXMATRIXStack：:P ush**</span><span class="sxs-lookup"><span data-stu-id="6b13a-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 





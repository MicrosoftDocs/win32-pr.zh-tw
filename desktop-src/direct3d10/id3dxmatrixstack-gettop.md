---
description: ID3DXMATRIXStack：： Vemap.gettop 方法 (D3DX10 .h) -在堆疊頂端抓取目前的矩陣。
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'ID3DXMATRIXStack：： Vemap.gettop 方法 (D3DX10 .h) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108036"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="c198b-103">ID3DXMATRIXStack：： Vemap.gettop 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="c198b-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="c198b-104">抓取堆疊頂端的目前矩陣。</span><span class="sxs-lookup"><span data-stu-id="c198b-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c198b-105">語法</span><span class="sxs-lookup"><span data-stu-id="c198b-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="c198b-106">參數</span><span class="sxs-lookup"><span data-stu-id="c198b-106">Parameters</span></span>

<span data-ttu-id="c198b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c198b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c198b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c198b-108">Return value</span></span>

<span data-ttu-id="c198b-109">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c198b-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c198b-110">這個方法會傳回 D3DXMATRIX 結構的指標，代表目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c198b-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c198b-111">備註</span><span class="sxs-lookup"><span data-stu-id="c198b-111">Remarks</span></span>

<span data-ttu-id="c198b-112">在後續的堆疊作業之後，這個方法所傳回的 D3DXMATRIX 指標不保證是有效的。</span><span class="sxs-lookup"><span data-stu-id="c198b-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="c198b-113">請注意，此方法不會從堆疊頂端移除目前的矩陣;相反地，它只會傳回目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c198b-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c198b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c198b-114">Requirements</span></span>



| <span data-ttu-id="c198b-115">需求</span><span class="sxs-lookup"><span data-stu-id="c198b-115">Requirement</span></span> | <span data-ttu-id="c198b-116">值</span><span class="sxs-lookup"><span data-stu-id="c198b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c198b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="c198b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c198b-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="c198b-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c198b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="c198b-119">Library</span></span><br/> | <dl> <span data-ttu-id="c198b-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c198b-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c198b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c198b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c198b-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="c198b-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c198b-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="c198b-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

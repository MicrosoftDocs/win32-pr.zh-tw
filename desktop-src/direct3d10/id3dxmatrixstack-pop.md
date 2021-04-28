---
description: ID3DXMATRIXStack：:P op 方法 (D3DX10) -從堆疊頂端移除目前的矩陣。
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: 'ID3DXMATRIXStack：:P op 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19c87cbd5fd81100682225aa16256573c7f95be0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107926"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="b3a34-103">ID3DXMATRIXStack：:P op 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="b3a34-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="b3a34-104">從堆疊頂端移除目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="b3a34-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a34-105">語法</span><span class="sxs-lookup"><span data-stu-id="b3a34-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="b3a34-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3a34-106">Parameters</span></span>

<span data-ttu-id="b3a34-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b3a34-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3a34-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3a34-108">Return value</span></span>

<span data-ttu-id="b3a34-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3a34-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3a34-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b3a34-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a34-111">備註</span><span class="sxs-lookup"><span data-stu-id="b3a34-111">Remarks</span></span>

<span data-ttu-id="b3a34-112">請注意，這個方法會將堆疊上的專案計數遞減1，有效地從堆疊頂端移除目前的矩陣，並將矩陣升階到堆疊的頂端。</span><span class="sxs-lookup"><span data-stu-id="b3a34-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="b3a34-113">如果堆疊上目前的專案計數為0，則這個方法會傳回而不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="b3a34-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="b3a34-114">如果堆疊上目前的專案計數是1，則這個方法會清空堆疊。</span><span class="sxs-lookup"><span data-stu-id="b3a34-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a34-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3a34-115">Requirements</span></span>



| <span data-ttu-id="b3a34-116">需求</span><span class="sxs-lookup"><span data-stu-id="b3a34-116">Requirement</span></span> | <span data-ttu-id="b3a34-117">值</span><span class="sxs-lookup"><span data-stu-id="b3a34-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a34-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b3a34-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b3a34-119"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a34-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3a34-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3a34-120">Library</span></span><br/> | <dl> <span data-ttu-id="b3a34-121"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3a34-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a34-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3a34-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a34-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b3a34-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b3a34-124">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="b3a34-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





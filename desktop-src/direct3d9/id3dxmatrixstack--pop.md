---
description: 從堆疊頂端移除目前的矩陣。
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: 'ID3DXMATRIXStack：:P op 方法 (D3dx9math .h) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 229892ab9b6a1ec75396b24cd9313e27667d0acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035336"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="e0851-103">ID3DXMATRIXStack：:P op 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="e0851-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="e0851-104">從堆疊頂端移除目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e0851-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0851-105">語法</span><span class="sxs-lookup"><span data-stu-id="e0851-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="e0851-106">參數</span><span class="sxs-lookup"><span data-stu-id="e0851-106">Parameters</span></span>

<span data-ttu-id="e0851-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e0851-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0851-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0851-108">Return value</span></span>

<span data-ttu-id="e0851-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0851-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0851-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e0851-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0851-111">備註</span><span class="sxs-lookup"><span data-stu-id="e0851-111">Remarks</span></span>

<span data-ttu-id="e0851-112">請注意，這個方法會將堆疊上的專案計數遞減1，有效地從堆疊頂端移除目前的矩陣，並將矩陣升階到堆疊的頂端。</span><span class="sxs-lookup"><span data-stu-id="e0851-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="e0851-113">如果堆疊上目前的專案計數為0，則這個方法會傳回而不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="e0851-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="e0851-114">如果堆疊上目前的專案計數是1，則這個方法會清空堆疊。</span><span class="sxs-lookup"><span data-stu-id="e0851-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0851-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0851-115">Requirements</span></span>



| <span data-ttu-id="e0851-116">需求</span><span class="sxs-lookup"><span data-stu-id="e0851-116">Requirement</span></span> | <span data-ttu-id="e0851-117">值</span><span class="sxs-lookup"><span data-stu-id="e0851-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0851-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e0851-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e0851-119"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0851-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e0851-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e0851-120">Library</span></span><br/> | <dl> <span data-ttu-id="e0851-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0851-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0851-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0851-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0851-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e0851-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e0851-124">**ID3DXMATRIXStack：： Vemap.gettop**</span><span class="sxs-lookup"><span data-stu-id="e0851-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="e0851-125">**ID3DXMATRIXStack：:P ush**</span><span class="sxs-lookup"><span data-stu-id="e0851-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 





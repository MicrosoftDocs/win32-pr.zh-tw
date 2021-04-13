---
description: Direct3D 10 set 函數不會保存裝置子物件的參考。
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: " (Direct3D 10) 的參考計數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6482918601f163bdea92291eb3927899ca797d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510468"
---
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="96b55-103"> (Direct3D 10) 的參考計數</span><span class="sxs-lookup"><span data-stu-id="96b55-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="96b55-104">Direct3D 10 set 函數不會保存裝置子物件的參考。</span><span class="sxs-lookup"><span data-stu-id="96b55-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="96b55-105">這表示，只要物件需要系結至管線，每個應用程式都必須保存裝置子物件的參考。</span><span class="sxs-lookup"><span data-stu-id="96b55-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="96b55-106">當物件的參考計數降至零時，該物件就會從管線解除系結並終結。</span><span class="sxs-lookup"><span data-stu-id="96b55-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="96b55-107">這種參考的樣式也稱為弱式參考，因為每個管線系結位置都持有與其系結之介面/物件的弱式參考。</span><span class="sxs-lookup"><span data-stu-id="96b55-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="96b55-108">例如：</span><span class="sxs-lookup"><span data-stu-id="96b55-108">For example:</span></span>


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





|                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96b55-109">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="96b55-109">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="96b55-110">在 Direct3D 9 中，set 函數會保存裝置物件的參考;在 Direct3D 10 中，set 函數不會保存裝置子物件的參考。</span><span class="sxs-lookup"><span data-stu-id="96b55-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="96b55-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="96b55-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b55-112"> (Direct3D 10) 的 API 功能 </span><span class="sxs-lookup"><span data-stu-id="96b55-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 





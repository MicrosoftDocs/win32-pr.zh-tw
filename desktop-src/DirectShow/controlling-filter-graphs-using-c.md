---
description: 使用 C 控制篩選圖形
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: 使用 C 控制篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385755"
---
# <a name="controlling-filter-graphs-using-c"></a><span data-ttu-id="382c7-103">使用 C 控制篩選圖形</span><span class="sxs-lookup"><span data-stu-id="382c7-103">Controlling Filter Graphs Using C</span></span>

<span data-ttu-id="382c7-104">如果您要在 C (（而不是 c + +) 中撰寫 DirectShow 應用程式，則必須使用 vtable 指標來呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="382c7-104">If you are writing a DirectShow application in C (rather than C++), you must use a vtable pointer to call methods.</span></span> <span data-ttu-id="382c7-105">下列範例說明如何從以 C 撰寫的應用程式呼叫 **IUnknown：： QueryInterface** 方法：</span><span class="sxs-lookup"><span data-stu-id="382c7-105">The following example illustrates how to call the **IUnknown::QueryInterface** method from an application written in C:</span></span>


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="382c7-106">以下顯示 c + + 中的對等呼叫：</span><span class="sxs-lookup"><span data-stu-id="382c7-106">The following shows the equivalent call in C++:</span></span>


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="382c7-107">在 C 中，COM 介面會定義為結構。</span><span class="sxs-lookup"><span data-stu-id="382c7-107">In C, COM interfaces are defined as structures.</span></span> <span data-ttu-id="382c7-108">**LpVtbl** 成員是介面方法資料表的指標， (vtable) 。</span><span class="sxs-lookup"><span data-stu-id="382c7-108">The **lpVtbl** member is a pointer to a table of interface methods (the vtable).</span></span> <span data-ttu-id="382c7-109">所有方法都採用額外的參數，也就是介面的指標。</span><span class="sxs-lookup"><span data-stu-id="382c7-109">All methods take an additional parameter, which is a pointer to the interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="382c7-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="382c7-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="382c7-111">附錄</span><span class="sxs-lookup"><span data-stu-id="382c7-111">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 




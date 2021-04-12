---
title: First_is 和 last_is 屬性
description: 您可以藉由指定第一個和最後一個元素，來判斷已傳送的元素數目。
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a2696db8e175f921b797176baaa8f3aa0263c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316315"
---
# <a name="the-first_is-and-last_is-attributes"></a><span data-ttu-id="8813b-105">\[第一個 \_ 是 \] 和 \[ 最後一個 \_ 是 \] 屬性</span><span class="sxs-lookup"><span data-stu-id="8813b-105">The \[first\_is\] and \[last\_is\] Attributes</span></span>

<span data-ttu-id="8813b-106">您可以藉由指定第一個和最後一個元素，來判斷已傳送的元素數目。</span><span class="sxs-lookup"><span data-stu-id="8813b-106">You can determine the number of transmitted elements by specifying the first and last elements.</span></span> <span data-ttu-id="8813b-107">使用 \[ [**\_ first**](/windows/desktop/Midl/first-is) \] 和 \[ [**last \_ 是**](/windows/desktop/Midl/last-is) \] 屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8813b-107">Use the \[[**first\_is**](/windows/desktop/Midl/first-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes as shown:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(4.0)
]
interface arraytest
{

  void fArray4([in]               short sSize,
               [in]               short sLast,
               [in]               short sFirst,
               [in, 
                out,
                size_is(sSize),
                first_is(sFirst),
                last_is(sLast)]   char achArray[]) ;
}
```

 

 
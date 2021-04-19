---
title: 虛擬函式資料表
description: 虛擬函式資料表
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966180"
---
# <a name="virtual-function-tables"></a><span data-ttu-id="6f87d-103">虛擬函式資料表</span><span class="sxs-lookup"><span data-stu-id="6f87d-103">Virtual Function Tables</span></span>

<span data-ttu-id="6f87d-104">虛擬函式資料表是物件所支援之方法的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="6f87d-104">A virtual function table is an array of pointers to the methods an object supports.</span></span> <span data-ttu-id="6f87d-105">如果您使用的是 C，則物件會顯示為結構，其第一個成員是虛擬函式資料表的指標 (**lpVtbl**) ;也就是說，第一個成員指向包含函式指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="6f87d-105">If you're using C, an object appears as a structure whose first member is a pointer to the virtual function table (**lpVtbl**); that is, the first member points to an array containing function pointers.</span></span> <span data-ttu-id="6f87d-106">所有方法都採用函式資料表的指標做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="6f87d-106">The methods all take a pointer to the function table as the first parameter.</span></span> <span data-ttu-id="6f87d-107">因此，下列範例會呼叫 **pStream** 物件的 **Read** 方法：</span><span class="sxs-lookup"><span data-stu-id="6f87d-107">Thus, the following example calls the **Read** method of a **pStream** object:</span></span>


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



<span data-ttu-id="6f87d-108">在 C + + 中，虛擬函式資料表的指標（ *this* 指標）是隱含的。</span><span class="sxs-lookup"><span data-stu-id="6f87d-108">In C+ +, the pointer to the virtual function table, the *this* pointer, is implicit.</span></span> <span data-ttu-id="6f87d-109">下列程式相當於使用 C + + 時的上一個範例：</span><span class="sxs-lookup"><span data-stu-id="6f87d-109">The following is equivalent to the previous example when using C+ +:</span></span>


```C++
pStream->Read(parameters) 
 
```



 

 





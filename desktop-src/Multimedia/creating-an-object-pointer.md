---
title: 建立物件指標
description: 建立物件指標
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183338"
---
# <a name="creating-an-object-pointer"></a><span data-ttu-id="46870-103">建立物件指標</span><span class="sxs-lookup"><span data-stu-id="46870-103">Creating an Object Pointer</span></span>

<span data-ttu-id="46870-104">AVIBall 會使用下列結構作為其物件指標。</span><span class="sxs-lookup"><span data-stu-id="46870-104">AVIBall uses the following structure as its object pointer.</span></span> <span data-ttu-id="46870-105">此結構的第一個成員指向 AVIBall 用來存取其函數的虛擬函式資料表。</span><span class="sxs-lookup"><span data-stu-id="46870-105">The first member of this structure points to the virtual function table that AVIBall uses to access its functions.</span></span> <span data-ttu-id="46870-106">應用程式可以將此結構轉換成 PAVISTREAM 資料類型。</span><span class="sxs-lookup"><span data-stu-id="46870-106">Applications can cast this structure to the PAVISTREAM data type.</span></span> <span data-ttu-id="46870-107">使用 PAVISTREAM 資料類型的方法只會使用虛擬函式資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="46870-107">Methods that use the PAVISTREAM data type use only the pointer to the virtual function table.</span></span> <span data-ttu-id="46870-108">AVIBall 會在內部使用虛擬函式資料表指標後面的成員。</span><span class="sxs-lookup"><span data-stu-id="46870-108">The members following the pointer to the virtual function table are used internally by AVIBall.</span></span>


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 





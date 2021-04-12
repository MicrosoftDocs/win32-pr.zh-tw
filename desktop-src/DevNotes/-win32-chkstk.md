---
description: 當您的函式中有一個以上的本機變數頁面時，由編譯器呼叫。
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk 常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936035"
---
# <a name="_chkstk-routine"></a><span data-ttu-id="58c11-103">\_chkstk 常式</span><span class="sxs-lookup"><span data-stu-id="58c11-103">\_chkstk Routine</span></span>

<span data-ttu-id="58c11-104">當您的函式中有一個以上的本機變數頁面時，由編譯器呼叫。</span><span class="sxs-lookup"><span data-stu-id="58c11-104">Called by the compiler when you have more than one page of local variables in your function.</span></span>

## <a name="remarks"></a><span data-ttu-id="58c11-105">備註</span><span class="sxs-lookup"><span data-stu-id="58c11-105">Remarks</span></span>

<span data-ttu-id="58c11-106">\_chkstk 常式是 C 編譯器的 helper 常式。</span><span class="sxs-lookup"><span data-stu-id="58c11-106">\_chkstk Routine is a helper routine for the C compiler.</span></span> <span data-ttu-id="58c11-107">For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.</span><span class="sxs-lookup"><span data-stu-id="58c11-107">For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.</span></span>

 

 




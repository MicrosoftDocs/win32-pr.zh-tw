---
description: 結構化例外狀況處理和終止處理機制是系統不可或缺的一部分;它們可讓系統穩定。 您可以使用這些機制來建立一致穩定且可靠的應用程式。
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: 關於結構化例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187642"
---
# <a name="about-structured-exception-handling"></a><span data-ttu-id="65104-104">關於結構化例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="65104-104">About Structured Exception Handling</span></span>

<span data-ttu-id="65104-105">結構化例外狀況處理和終止處理機制是系統不可或缺的一部分;它們可讓系統穩定。</span><span class="sxs-lookup"><span data-stu-id="65104-105">The structured exception handling and termination handling mechanisms are integral parts of the system; they enable the system to be robust.</span></span> <span data-ttu-id="65104-106">您可以使用這些機制來建立一致穩定且可靠的應用程式。</span><span class="sxs-lookup"><span data-stu-id="65104-106">You can use these mechanisms to create consistently robust and reliable applications.</span></span>

<span data-ttu-id="65104-107">結構化例外狀況處理主要是透過編譯器支援來提供。</span><span class="sxs-lookup"><span data-stu-id="65104-107">Structured exception handling is made available primarily through compiler support.</span></span> <span data-ttu-id="65104-108">例如，Microsoft C/c + + 優化編譯器支援用來識別程式碼受防護主體的 **\_ \_ try** 關鍵字、識別例外狀況處理常式的 **\_ \_ except** 關鍵字，以及用來識別終止處理常式的 **\_ \_ finally** 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="65104-108">For example, the Microsoft C/C++ Optimizing Compiler supports the **\_\_try** keyword that identifies a guarded body of code, the **\_\_except** keyword that identifies an exception handler, and the **\_\_finally** keyword that identifies a termination handler.</span></span> <span data-ttu-id="65104-109">雖然本總覽使用 Microsoft C/c + + 編譯器特定的範例，但其他編譯器也會提供此支援。</span><span class="sxs-lookup"><span data-stu-id="65104-109">Although this overview uses examples specific to the Microsoft C/C++ compiler, other compilers provide this support as well.</span></span>

-   [<span data-ttu-id="65104-110">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="65104-110">Exception Handling</span></span>](exception-handling.md)
-   [<span data-ttu-id="65104-111">以框架為基礎的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="65104-111">Frame-based Exception Handling</span></span>](frame-based-exception-handling.md)
-   [<span data-ttu-id="65104-112">向量式例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="65104-112">Vectored Exception Handling</span></span>](vectored-exception-handling.md)
-   [<span data-ttu-id="65104-113">終止處理</span><span class="sxs-lookup"><span data-stu-id="65104-113">Termination Handling</span></span>](termination-handling.md)
-   [<span data-ttu-id="65104-114">處理常式語法</span><span class="sxs-lookup"><span data-stu-id="65104-114">Handler Syntax</span></span>](handler-syntax.md)

 

 




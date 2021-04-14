---
title: 使用和執行 IUnknown
description: 使用和執行 IUnknown
ms.assetid: d44a6dc7-54e4-42b3-9a3d-a6569fa4128b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fc5be5ee84bacfec9e239d28263344ec902a0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371900"
---
# <a name="using-and-implementing-iunknown"></a><span data-ttu-id="ff15d-103">使用和執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff15d-103">Using and Implementing IUnknown</span></span>

<span data-ttu-id="ff15d-104">COM 提供一組豐富的標準來執行和使用物件，以及進行物件間的通訊。</span><span class="sxs-lookup"><span data-stu-id="ff15d-104">COM provides a rich set of standards for implementing and using objects and for inter-object communication.</span></span> <span data-ttu-id="ff15d-105">本節中的主題描述與執行物件相關的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="ff15d-105">The topics in this section describe basic information relating to implementing objects.</span></span> <span data-ttu-id="ff15d-106">如需有關用戶端和伺服器如何互動的詳細資訊，請參閱 [COM 用戶端和伺服器](com-clients-and-servers.md)。</span><span class="sxs-lookup"><span data-stu-id="ff15d-106">For information about how clients and servers interact, see [COM Clients and Servers](com-clients-and-servers.md).</span></span> <span data-ttu-id="ff15d-107">如需執行緒模型及其執行和使用的詳細資訊，請參閱 [進程、執行緒和單元](processes--threads--and-apartments.md)。</span><span class="sxs-lookup"><span data-stu-id="ff15d-107">For more information about threading models and their implementation and use, see [Processes, Threads, and Apartments](processes--threads--and-apartments.md).</span></span>

<span data-ttu-id="ff15d-108">如需使用和執行 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="ff15d-108">For details on using and implementing [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), see the following topics:</span></span>

-   [<span data-ttu-id="ff15d-109">QueryInterface：在物件中流覽</span><span class="sxs-lookup"><span data-stu-id="ff15d-109">QueryInterface: Navigating in an Object</span></span>](queryinterface--navigating-in-an-object.md)
-   [<span data-ttu-id="ff15d-110">執行 QueryInterface 的規則</span><span class="sxs-lookup"><span data-stu-id="ff15d-110">Rules for Implementing QueryInterface</span></span>](rules-for-implementing-queryinterface.md)
-   [<span data-ttu-id="ff15d-111">透過參考計數來管理物件存留期</span><span class="sxs-lookup"><span data-stu-id="ff15d-111">Managing Object Lifetimes Through Reference Counting</span></span>](managing-object-lifetimes-through-reference-counting.md)

 

 





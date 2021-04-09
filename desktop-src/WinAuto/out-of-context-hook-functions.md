---
title: 內容外攔截函式
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 深入瞭解：內容外攔截函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851039"
---
# <a name="out-of-context-hook-functions"></a><span data-ttu-id="0e44c-103">內容外攔截函式</span><span class="sxs-lookup"><span data-stu-id="0e44c-103">Out-of-Context Hook Functions</span></span>

<span data-ttu-id="0e44c-104">下列清單概述跨內容攔截函式的主要層面：</span><span class="sxs-lookup"><span data-stu-id="0e44c-104">The following list outlines the key aspects of out-of-context hook functions:</span></span>

-   <span data-ttu-id="0e44c-105">跨內容攔截函式位於用戶端的位址空間中，不論它是在程式碼主體或 DLL 中。</span><span class="sxs-lookup"><span data-stu-id="0e44c-105">Out-of-context hook functions are located in the client's address space, whether it is in the code body or in a DLL.</span></span>
-   <span data-ttu-id="0e44c-106">非內容攔截函式不會對應到伺服器的位址空間。</span><span class="sxs-lookup"><span data-stu-id="0e44c-106">Out-of-context hook functions are not mapped into the server's address space.</span></span>
-   <span data-ttu-id="0e44c-107">觸發事件時，攔截函式的參數會跨進程界限封送處理。</span><span class="sxs-lookup"><span data-stu-id="0e44c-107">When an event is triggered, the parameters for the hook function are marshaled across process boundaries.</span></span>
-   <span data-ttu-id="0e44c-108">由於封送處理的緣故，內容外攔截函式明顯比內容攔截函式慢。</span><span class="sxs-lookup"><span data-stu-id="0e44c-108">Out-of-context hook functions are noticeably slower than in-context hook functions due to marshaling.</span></span>
-   <span data-ttu-id="0e44c-109">系統會將事件通知排入佇列，以便 (因為執行封送處理) 所需的時間而以非同步方式抵達。</span><span class="sxs-lookup"><span data-stu-id="0e44c-109">The system queues the event notifications so that they arrive asynchronously (because of the time required to perform marshaling).</span></span>

<span data-ttu-id="0e44c-110">雖然事件通知是非同步，但 Microsoft Active Accessibility 可確保回呼函數會依照產生的順序來接收所有事件。</span><span class="sxs-lookup"><span data-stu-id="0e44c-110">Although the event notifications are asynchronous, Microsoft Active Accessibility assures that the callback function receives all events in the order in which they are generated.</span></span>

<span data-ttu-id="0e44c-111">作業系統的使用者元件會為由內容外攔截函式所處理的事件配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="0e44c-111">The USER component of the operating system allocates memory for events that are handled by out-of-context hook functions.</span></span> <span data-ttu-id="0e44c-112">當攔截函式傳回時，便會釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="0e44c-112">The memory is freed when the hook functions return.</span></span> <span data-ttu-id="0e44c-113">如果攔截函式無法快速處理事件，則會降低使用者資源，最終會導致錯誤或回應時間太慢。</span><span class="sxs-lookup"><span data-stu-id="0e44c-113">If a hook function does not process events quickly enough, USER resources are lowered, eventually resulting in a fault or extremely slow response times.</span></span> <span data-ttu-id="0e44c-114">這些問題可能會發生在下列情況：</span><span class="sxs-lookup"><span data-stu-id="0e44c-114">These problems may occur if:</span></span>

-   <span data-ttu-id="0e44c-115">事件的引發速度非常快。</span><span class="sxs-lookup"><span data-stu-id="0e44c-115">Events are fired very rapidly.</span></span>
-   <span data-ttu-id="0e44c-116">系統很慢。</span><span class="sxs-lookup"><span data-stu-id="0e44c-116">The system is slow.</span></span>
-   <span data-ttu-id="0e44c-117">攔截函式處理事件的速度很慢。</span><span class="sxs-lookup"><span data-stu-id="0e44c-117">The hook function processes events slowly.</span></span>
-   <span data-ttu-id="0e44c-118">用戶端正在 Windows 9x 上執行。</span><span class="sxs-lookup"><span data-stu-id="0e44c-118">The client is running on Windows 9x.</span></span>

 

 





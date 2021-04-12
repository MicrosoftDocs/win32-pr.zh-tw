---
title: In-Context 攔截函式
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 深入瞭解： In-Context 攔截函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195237"
---
# <a name="in-context-hook-functions"></a><span data-ttu-id="ad4cd-103">In-Context 攔截函式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-103">In-Context Hook Functions</span></span>

<span data-ttu-id="ad4cd-104">下列清單概述內容攔截函式的主要層面：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-104">The following list outlines the key aspects of in-context hook functions:</span></span>

-   <span data-ttu-id="ad4cd-105">內容內攔截函式必須位於動態連結程式庫 (DLL) ，系統會將該程式庫對應到伺服器的位址空間中。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-105">In-context hooks functions must be located in a dynamic-link library (DLL) that the system maps into the server's address space.</span></span>
-   <span data-ttu-id="ad4cd-106">內容中攔截函式與伺服器共用位址空間。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-106">In-context hook functions share the address space with the server.</span></span>
-   <span data-ttu-id="ad4cd-107">當伺服器觸發事件時，系統會呼叫攔截函式，而不需要封送處理 (封裝和傳送跨進程界限) 的介面參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-107">When the server triggers an event, the system calls a hook function without marshaling (packaging and sending interface parameters across process boundaries).</span></span>
-   <span data-ttu-id="ad4cd-108">內容攔截函式通常非常快速，而且會以同步的方式接收事件通知，因為沒有封送處理。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-108">In-context hook functions tend to be very fast and receive event notifications synchronously because there is no marshaling.</span></span>
-   <span data-ttu-id="ad4cd-109">某些事件可以跨進程傳遞，即使您要求使用 NEW-WINEVENT INCONTEXT 旗標) 來傳遞同進程 (也是一樣 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-109">Some events may be delivered out-of-process, even though you request that they be delivered in-process (using the WINEVENT\_INCONTEXT flag).</span></span> <span data-ttu-id="ad4cd-110">您可能會看到與64位和32位應用程式互通性問題以及 Windows 主控台事件有關的這種情況。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-110">You might see this situation with 64-bit and 32-bit application interoperability issues and with Windows console events.</span></span>

 

 





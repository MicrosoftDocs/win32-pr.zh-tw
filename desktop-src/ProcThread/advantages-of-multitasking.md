---
description: 對使用者而言，多工的優點是能夠讓多個應用程式同時開啟和運作。 例如，使用者可以使用一個應用程式來編輯檔案，而另一個應用程式則是重新計算試算表。
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: 多工處理的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993129"
---
# <a name="advantages-of-multitasking"></a><span data-ttu-id="74572-104">多工處理的優點</span><span class="sxs-lookup"><span data-stu-id="74572-104">Advantages of Multitasking</span></span>

<span data-ttu-id="74572-105">對使用者而言，多工的優點是能夠讓多個應用程式同時開啟和運作。</span><span class="sxs-lookup"><span data-stu-id="74572-105">To the user, the advantage of multitasking is the ability to have several applications open and working at the same time.</span></span> <span data-ttu-id="74572-106">例如，使用者可以使用一個應用程式來編輯檔案，而另一個應用程式則是重新計算試算表。</span><span class="sxs-lookup"><span data-stu-id="74572-106">For example, a user can edit a file with one application while another application is recalculating a spreadsheet.</span></span>

<span data-ttu-id="74572-107">針對應用程式開發人員，多工的優點是能夠建立使用多個進程的應用程式，並建立使用多個執行緒執行的進程。</span><span class="sxs-lookup"><span data-stu-id="74572-107">To the application developer, the advantage of multitasking is the ability to create applications that use more than one process and to create processes that use more than one thread of execution.</span></span> <span data-ttu-id="74572-108">例如，處理常式可以有使用者介面執行緒來管理與使用者的互動 (鍵盤和滑鼠輸入) ，以及在使用者介面執行緒等候使用者輸入時執行其他工作的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="74572-108">For example, a process can have a user interface thread that manages interactions with the user (keyboard and mouse input), and worker threads that perform other tasks while the user interface thread waits for user input.</span></span> <span data-ttu-id="74572-109">如果您讓使用者介面執行緒具有較高的優先順序，則應用程式將會更能回應使用者，而背景工作執行緒則會在沒有使用者輸入的時間內有效率地使用處理器。</span><span class="sxs-lookup"><span data-stu-id="74572-109">If you give the user interface thread a higher priority, the application will be more responsive to the user, while the worker threads use the processor efficiently during the times when there is no user input.</span></span>

 

 




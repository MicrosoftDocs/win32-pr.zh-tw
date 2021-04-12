---
description: 除了處理虛擬封鎖的函式以外，windows 通訊端2繼續支援所有的 Windows 通訊端1.1 語義和函式呼叫。
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows 通訊端相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191733"
---
# <a name="windows-sockets-compatibility-issues"></a><span data-ttu-id="76f2f-103">Windows 通訊端相容性問題</span><span class="sxs-lookup"><span data-stu-id="76f2f-103">Windows Sockets Compatibility Issues</span></span>

<span data-ttu-id="76f2f-104">除了處理虛擬封鎖的函式以外，windows 通訊端2繼續支援所有的 Windows 通訊端1.1 語義和函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="76f2f-104">Windows Sockets 2 continues to support all of the Windows Sockets 1.1 semantics and function calls except for those dealing with pseudo-blocking.</span></span> <span data-ttu-id="76f2f-105">由於 Windows 通訊端2只會在32位、事先排程的環境中執行，因此不需要執行 Windows 通訊端1.1 中所找到的虛擬封鎖。</span><span class="sxs-lookup"><span data-stu-id="76f2f-105">Since Windows Sockets 2 runs only in 32-bit, preemptively scheduled environments, there is no need to implement the pseudo-blocking found in Windows Sockets 1.1.</span></span> <span data-ttu-id="76f2f-106">這表示將永遠不會指出 WSAEINPROGRESS 錯誤碼，且 Windows 通訊端2應用程式無法使用下列 Windows 通訊端1.1 功能：</span><span class="sxs-lookup"><span data-stu-id="76f2f-106">This means that the WSAEINPROGRESS error code will never be indicated and that the following Windows Sockets 1.1 functions are not available to Windows Sockets 2 applications:</span></span>

-   <span data-ttu-id="76f2f-107">WSACancelBlockingCall</span><span class="sxs-lookup"><span data-stu-id="76f2f-107">WSACancelBlockingCall</span></span>
-   <span data-ttu-id="76f2f-108">WSAIsBlocking</span><span class="sxs-lookup"><span data-stu-id="76f2f-108">WSAIsBlocking</span></span>
-   <span data-ttu-id="76f2f-109">WSASetBlockingHook</span><span class="sxs-lookup"><span data-stu-id="76f2f-109">WSASetBlockingHook</span></span>
-   <span data-ttu-id="76f2f-110">WSAUnhookBlockingHook</span><span class="sxs-lookup"><span data-stu-id="76f2f-110">WSAUnhookBlockingHook</span></span>

<span data-ttu-id="76f2f-111">為了利用虛擬封鎖而撰寫的 Windows 通訊端1.1 程式，將會繼續正常運作，因為它們會連結到 Winsock.dll 或 Wsock32.dll。</span><span class="sxs-lookup"><span data-stu-id="76f2f-111">Windows Sockets 1.1 programs that are written to utilize pseudo-blocking will continue to operate correctly since they link to either Winsock.dll or Wsock32.dll.</span></span> <span data-ttu-id="76f2f-112">這兩種功能都能繼續支援一組完整的 Windows 通訊端1.1 函式。</span><span class="sxs-lookup"><span data-stu-id="76f2f-112">Both continue to support the complete set of Windows Sockets 1.1 functions.</span></span> <span data-ttu-id="76f2f-113">為了讓程式成為 Windows 通訊端2應用程式，必須進行一些修改程式碼。</span><span class="sxs-lookup"><span data-stu-id="76f2f-113">In order for programs to become Windows Sockets 2 applications, some code modification must occur.</span></span> <span data-ttu-id="76f2f-114">在大部分的情況下，可以使用執行緒的明智用法來容納使用封鎖攔截函式完成的處理。</span><span class="sxs-lookup"><span data-stu-id="76f2f-114">In most cases, the judicious use of threads can be substituted to accommodate processing that was being accomplished with a blocking hook function.</span></span>

 

 




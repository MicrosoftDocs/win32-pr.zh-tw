---
title: 處理序間通訊
description: 下列技巧可用於32位和64位應用程式之間的通訊。
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- 處理序間通訊64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376088"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a><span data-ttu-id="0c35d-104">32位和64位應用程式之間的處理序間通訊</span><span class="sxs-lookup"><span data-stu-id="0c35d-104">Interprocess Communication Between 32-bit and 64-bit Applications</span></span>

<span data-ttu-id="0c35d-105">下列技術可用於32位和64位應用程式之間的通訊：</span><span class="sxs-lookup"><span data-stu-id="0c35d-105">The following techniques can be used for communication between 32-bit and 64-bit applications:</span></span>

-   <span data-ttu-id="0c35d-106">64位版本的 Windows 會使用32位控制碼來進行互通性。</span><span class="sxs-lookup"><span data-stu-id="0c35d-106">64-bit versions of Windows use 32-bit handles for interoperability.</span></span> <span data-ttu-id="0c35d-107">當共用32位和64位應用程式之間的控制碼時，只有較低的32位是很重要的，因此在將控制碼從64位傳遞到32位時，可以安全地截斷控制碼 () 或將控制碼從32位傳遞到64位) 時，將它進行正負號擴充 (。</span><span class="sxs-lookup"><span data-stu-id="0c35d-107">When sharing a handle between 32-bit and 64-bit applications, only the lower 32 bits are significant, so it is safe to truncate the handle (when passing it from 64-bit to 32-bit) or sign-extend the handle (when passing it from 32-bit to 64-bit).</span></span> <span data-ttu-id="0c35d-108">可以共用的控制碼包括使用者物件的控制碼（例如 windows (**HWND**) ）、GDI 物件的控制碼（例如畫筆和筆刷） (**HBRUSH** 和 **HPEN**) ，以及命名物件（例如 mutex、信號和檔案控制代碼）的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0c35d-108">Handles that can be shared include handles to user objects such as windows (**HWND**), handles to GDI objects such as pens and brushes (**HBRUSH** and **HPEN**), and handles to named objects such as mutexes, semaphores, and file handles.</span></span>
-   <span data-ttu-id="0c35d-109">您可以使用 (RPC) 的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c35d-109">Remote procedure calls (RPC) can be used.</span></span>
-   <span data-ttu-id="0c35d-110">如果已針對所有使用的介面註冊32位和64位 proxy/stub Dll，則可以使用 COM LocalServers。</span><span class="sxs-lookup"><span data-stu-id="0c35d-110">COM LocalServers can be used if both 32-bit and 64-bit proxy/stub DLLs are registered for all interfaces used.</span></span>
-   <span data-ttu-id="0c35d-111">如果指標相依類型已正確轉換 (或避免) ，則可以使用共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="0c35d-111">Shared memory can be used if pointer-dependent types are converted properly (or avoided).</span></span>
-   <span data-ttu-id="0c35d-112">[**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)和 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)函式可以從32位或64位進程啟動32位和64位進程，但有某些限制。</span><span class="sxs-lookup"><span data-stu-id="0c35d-112">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) and [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) functions can launch 32-bit and 64-bit processes from either 32-bit or 64-bit processes with certain limitations.</span></span>

<span data-ttu-id="0c35d-113">位於% windir% System32 下的64位可執行檔 \\ 無法從32位進程啟動，因為檔案系統重新導向程式會重新導向路徑。</span><span class="sxs-lookup"><span data-stu-id="0c35d-113">A 64-bit executable file located under %windir%\\System32 cannot be launched from a 32-bit process, because the file system redirector redirects the path.</span></span> <span data-ttu-id="0c35d-114">請勿停用重新導向來完成此動作;請改用% windir% \\ Sysnative。</span><span class="sxs-lookup"><span data-stu-id="0c35d-114">Do not disable redirection to accomplish this; use %windir%\\Sysnative instead.</span></span> <span data-ttu-id="0c35d-115">如需詳細資訊，請參閱 [檔案系統重定向](file-system-redirector.md)程式。</span><span class="sxs-lookup"><span data-stu-id="0c35d-115">For more information, see [File System Redirector](file-system-redirector.md).</span></span>

 

 
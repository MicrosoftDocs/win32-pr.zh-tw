---
description: 錯誤模式向系統指出應用程式如何回應嚴重的錯誤。
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: 錯誤模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109977"
---
# <a name="error-mode"></a><span data-ttu-id="5fca9-103">錯誤模式</span><span class="sxs-lookup"><span data-stu-id="5fca9-103">Error Mode</span></span>

<span data-ttu-id="5fca9-104">錯誤模式向系統指出應用程式如何回應嚴重的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fca9-104">The error mode indicates to the system how the application is going to respond to serious errors.</span></span> <span data-ttu-id="5fca9-105">嚴重錯誤包括磁片故障、磁片磁碟機未就緒錯誤、資料對齊和未處理的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5fca9-105">Serious errors include disk failure, drive-not-ready errors, data misalignment, and unhandled exceptions.</span></span> <span data-ttu-id="5fca9-106">您可以透過每個執行緒或每個處理常式來管理此錯誤模式。</span><span class="sxs-lookup"><span data-stu-id="5fca9-106">This error mode can be managed by either a per-thread or per-process basis.</span></span> <span data-ttu-id="5fca9-107">應用程式可讓系統顯示訊息方塊，通知使用者發生錯誤，或可處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fca9-107">An application can let the system display a message box informing the user that an error has occurred, or it can handle the errors.</span></span>

<span data-ttu-id="5fca9-108">若要在不需要使用者介入的情況下處理這些錯誤，請使用 [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) 或執行緒特定的 [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)。</span><span class="sxs-lookup"><span data-stu-id="5fca9-108">To handle these errors without user intervention, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) or the thread-specific [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode).</span></span> <span data-ttu-id="5fca9-109">呼叫其中一個函式並指定適當的旗標之後，系統將不會顯示對應的錯誤訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="5fca9-109">After calling one of these functions and specifying appropriate flags, the system will not display the corresponding error message boxes.</span></span>

<span data-ttu-id="5fca9-110">處理常式可以使用 [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) 或 [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)來取得其錯誤模式。</span><span class="sxs-lookup"><span data-stu-id="5fca9-110">A process can retrieve its error mode using [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) or [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span></span>

<span data-ttu-id="5fca9-111">最佳做法是在啟動時，所有應用程式都會以 **SEM \_ FAILCRITICALERRORS** 的參數呼叫整個進程的 [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)函式。</span><span class="sxs-lookup"><span data-stu-id="5fca9-111">Best practice is that all applications call the process-wide [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with a parameter of **SEM\_FAILCRITICALERRORS** at startup.</span></span> <span data-ttu-id="5fca9-112">這是為了防止錯誤強制回應對話方塊讓應用程式停止回應。</span><span class="sxs-lookup"><span data-stu-id="5fca9-112">This is to prevent error mode dialogs from hanging the application.</span></span>

<span data-ttu-id="5fca9-113">相反地，呼叫端應該優先採用這些函式的執行緒特定版本，因為它們較不會干擾系統的正常行為。</span><span class="sxs-lookup"><span data-stu-id="5fca9-113">Other than that, callers should favor the thread-specific versions of these functions since they are less disruptive to the normal behavior of the system.</span></span>

 

 

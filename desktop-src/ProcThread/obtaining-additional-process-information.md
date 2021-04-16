---
description: 有各種不同的函式可取得處理常式的相關資訊。
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: 取得額外的進程資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513388"
---
# <a name="obtaining-additional-process-information"></a><span data-ttu-id="bf6d6-103">取得額外的進程資訊</span><span class="sxs-lookup"><span data-stu-id="bf6d6-103">Obtaining Additional Process Information</span></span>

<span data-ttu-id="bf6d6-104">有各種不同的函式可取得處理常式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-104">There are a variety of functions for obtaining information about processes.</span></span> <span data-ttu-id="bf6d6-105">其中有些函式只能用於呼叫進程，因為它們不會以進程控制碼作為參數。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-105">Some of these functions can be used only for the calling process, because they do not take a process handle as a parameter.</span></span> <span data-ttu-id="bf6d6-106">您可以使用採用進程控制碼的函式來取得其他進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-106">You can use functions that take a process handle to obtain information about other processes.</span></span>

-   <span data-ttu-id="bf6d6-107">若要取得目前進程的命令列字串，請使用 [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-107">To obtain the command-line string for the current process, use the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function.</span></span>
-   <span data-ttu-id="bf6d6-108">若要取得目前的進程建立時所指定的 [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) 結構，請使用 [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) 函式。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-108">To retrieve the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specified when the current process was created, use the [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) function.</span></span>
-   <span data-ttu-id="bf6d6-109">若要從可執行檔標頭取得版本資訊，請使用 [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-109">To obtain the version information from the executable header, use the [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) function.</span></span>
-   <span data-ttu-id="bf6d6-110">若要取得包含處理常式代碼之可執行檔的完整路徑和檔案名，請使用 [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-110">To obtain the full path and file name for the executable file containing the process code, use the [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>
-   <span data-ttu-id="bf6d6-111">若要取得圖形使用者介面的控制碼計數 (GUI) 使用中的物件，請使用 [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-111">To obtain the count of handles to graphical user interface (GUI) objects in use, use the [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) function.</span></span>
-   <span data-ttu-id="bf6d6-112">若要判斷是否正在調試進程，請使用 [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-112">To determine whether a process is being debugged, use the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>
-   <span data-ttu-id="bf6d6-113">若要取得處理常式所執行之所有 i/o 作業的帳戶處理資訊，請使用 [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf6d6-113">To retrieve accounting information for all I/O operations performed by the process, use the [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) function.</span></span>

 

 

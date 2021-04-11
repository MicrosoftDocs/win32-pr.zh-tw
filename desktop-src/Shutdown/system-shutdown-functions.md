---
description: 下列函式可用於系統關機。
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: 系統關機功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944352"
---
# <a name="system-shutdown-functions"></a><span data-ttu-id="ecacf-103">系統關機功能</span><span class="sxs-lookup"><span data-stu-id="ecacf-103">System Shutdown Functions</span></span>

<span data-ttu-id="ecacf-104">下列函式可用於系統關機。</span><span class="sxs-lookup"><span data-stu-id="ecacf-104">The following functions are used with system shutdown.</span></span>



| <span data-ttu-id="ecacf-105">函式</span><span class="sxs-lookup"><span data-stu-id="ecacf-105">Function</span></span>                                                         | <span data-ttu-id="ecacf-106">描述</span><span class="sxs-lookup"><span data-stu-id="ecacf-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecacf-107">**AbortSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="ecacf-107">**AbortSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | <span data-ttu-id="ecacf-108">停止已起始的系統關機。</span><span class="sxs-lookup"><span data-stu-id="ecacf-108">Stops a system shutdown that has been initiated.</span></span>                                                                                    |
| [<span data-ttu-id="ecacf-109">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="ecacf-109">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | <span data-ttu-id="ecacf-110">登出互動式使用者。</span><span class="sxs-lookup"><span data-stu-id="ecacf-110">Logs off the interactive user.</span></span>                                                                                                      |
| [<span data-ttu-id="ecacf-111">**ExitWindowsEx**</span><span class="sxs-lookup"><span data-stu-id="ecacf-111">**ExitWindowsEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | <span data-ttu-id="ecacf-112">登出互動式使用者、關閉系統，或關閉並重新啟動系統。</span><span class="sxs-lookup"><span data-stu-id="ecacf-112">Logs off the interactive user, shuts down the system, or shuts down and restarts the system.</span></span>                                        |
| [<span data-ttu-id="ecacf-113">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="ecacf-113">**InitiateShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | <span data-ttu-id="ecacf-114">起始指定電腦的關機和重新開機，並重新啟動任何已註冊要重新開機的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ecacf-114">Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.</span></span>    |
| [<span data-ttu-id="ecacf-115">**InitiateSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="ecacf-115">**InitiateSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | <span data-ttu-id="ecacf-116">起始指定電腦的關機和選擇性重新開機。</span><span class="sxs-lookup"><span data-stu-id="ecacf-116">Initiates a shutdown and optional restart of the specified computer.</span></span>                                                                |
| [<span data-ttu-id="ecacf-117">**InitiateSystemShutdownEx**</span><span class="sxs-lookup"><span data-stu-id="ecacf-117">**InitiateSystemShutdownEx**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | <span data-ttu-id="ecacf-118">起始指定電腦的關機和選擇性重新開機，並選擇性地記錄關機的原因。</span><span class="sxs-lookup"><span data-stu-id="ecacf-118">Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.</span></span>            |
| [<span data-ttu-id="ecacf-119">**>lockworkstation**</span><span class="sxs-lookup"><span data-stu-id="ecacf-119">**LockWorkStation**</span></span>](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | <span data-ttu-id="ecacf-120">鎖定工作站的顯示。</span><span class="sxs-lookup"><span data-stu-id="ecacf-120">Locks the workstation's display.</span></span>                                                                                                    |
| [<span data-ttu-id="ecacf-121">**ShutdownBlockReasonCreate**</span><span class="sxs-lookup"><span data-stu-id="ecacf-121">**ShutdownBlockReasonCreate**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | <span data-ttu-id="ecacf-122">指出系統無法關機，並設定當系統關機啟動時要顯示給使用者的原因字串。</span><span class="sxs-lookup"><span data-stu-id="ecacf-122">Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.</span></span> |
| [<span data-ttu-id="ecacf-123">**ShutdownBlockReasonDestroy**</span><span class="sxs-lookup"><span data-stu-id="ecacf-123">**ShutdownBlockReasonDestroy**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | <span data-ttu-id="ecacf-124">表示系統可以關閉並釋出原因字串。</span><span class="sxs-lookup"><span data-stu-id="ecacf-124">Indicates that the system can be shut down and frees the reason string.</span></span>                                                             |
| [<span data-ttu-id="ecacf-125">**ShutdownBlockReasonQuery**</span><span class="sxs-lookup"><span data-stu-id="ecacf-125">**ShutdownBlockReasonQuery**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | <span data-ttu-id="ecacf-126">抓取 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) 函數所設定的原因字串。</span><span class="sxs-lookup"><span data-stu-id="ecacf-126">Retrieves the reason string set by the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span>                     |



 

 

 




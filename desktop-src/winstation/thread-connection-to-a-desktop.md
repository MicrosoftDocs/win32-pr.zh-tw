---
title: 與桌面的執行緒連接
description: 在處理常式連接到視窗工作站之後，系統會將桌面指派給進行連接的執行緒。
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104185996"
---
# <a name="thread-connection-to-a-desktop"></a><span data-ttu-id="7227a-103">與桌面的執行緒連接</span><span class="sxs-lookup"><span data-stu-id="7227a-103">Thread Connection to a Desktop</span></span>

<span data-ttu-id="7227a-104">在處理常式連接到視窗工作站之後，系統會將桌面指派給進行連接的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7227a-104">After a process connects to a window station, the system assigns a desktop to the thread making the connection.</span></span> <span data-ttu-id="7227a-105">系統會根據下列規則，決定要指派給執行緒的桌面：</span><span class="sxs-lookup"><span data-stu-id="7227a-105">The system determines the desktop to assign to the thread according to the following rules:</span></span>

1.  <span data-ttu-id="7227a-106">如果執行緒已呼叫 [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) 函式，它會連接到指定的桌面。</span><span class="sxs-lookup"><span data-stu-id="7227a-106">If the thread has called the [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) function, it connects to the specified desktop.</span></span>
2.  <span data-ttu-id="7227a-107">如果執行緒未呼叫 [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)，它會連接到繼承自父進程的桌面。</span><span class="sxs-lookup"><span data-stu-id="7227a-107">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), it connects to the desktop inherited from the parent process.</span></span>
3.  <span data-ttu-id="7227a-108">如果執行緒未呼叫 [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) ，且未繼承桌面，系統會嘗試開啟以取得允許的最大 \_ 存取權，並連接至桌面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7227a-108">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) and did not inherit a desktop, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a desktop as follows:</span></span>
    -   <span data-ttu-id="7227a-109">如果在建立進程時所使用之 [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa)結構的 **lpDesktop** 成員中指定了桌面名稱，執行緒就會連接到指定的桌面。</span><span class="sxs-lookup"><span data-stu-id="7227a-109">If a desktop name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the thread connects to the specified desktop.</span></span>
    -   <span data-ttu-id="7227a-110">否則，執行緒會連接到進程所連接之視窗工作站的預設桌面。</span><span class="sxs-lookup"><span data-stu-id="7227a-110">Otherwise, the thread connects to the default desktop of the window station to which the process connected.</span></span>

<span data-ttu-id="7227a-111">呼叫 [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) 函式時，無法關閉在此連接過程中指派的桌面。</span><span class="sxs-lookup"><span data-stu-id="7227a-111">The desktop assigned during this connection process cannot be closed by calling the [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) function.</span></span>

<span data-ttu-id="7227a-112">當處理常式連接到桌面時，系統會在進程的控制碼資料表中搜尋繼承的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7227a-112">When a process is connecting to a desktop, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="7227a-113">系統會使用它所找到的第一個桌面控制碼。</span><span class="sxs-lookup"><span data-stu-id="7227a-113">The system uses the first desktop handle it finds.</span></span> <span data-ttu-id="7227a-114">如果您想要讓子進程連接到特定的繼承桌面，您必須確定只將所需的控制碼標示為可繼承。</span><span class="sxs-lookup"><span data-stu-id="7227a-114">If you want a child process to connect to a particular inherited desktop, you must ensure that the only the desired handle is marked inheritable.</span></span> <span data-ttu-id="7227a-115">如果子進程繼承多個桌面控制碼，則桌面連接的結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="7227a-115">If a child process inherits multiple desktop handles, the results of the desktop connection are undefined.</span></span>

<span data-ttu-id="7227a-116">系統在將進程連接到桌面時開啟的桌面的控制碼，無法繼承。</span><span class="sxs-lookup"><span data-stu-id="7227a-116">Handles to a desktop that the system opens while connecting a process to a desktop are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7227a-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="7227a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7227a-118">處理與視窗工作站的連接</span><span class="sxs-lookup"><span data-stu-id="7227a-118">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
</dt> </dl>

 

 
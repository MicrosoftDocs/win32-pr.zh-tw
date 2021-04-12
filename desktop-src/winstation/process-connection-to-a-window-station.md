---
title: 處理與視窗工作站的連接
description: 程式會在第一次呼叫 USER32 或 GDI32 函式時，自動建立與視窗工作站和桌面的連接， (非視窗工作站和桌面函式) 。
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a87e97b19ac1210b04447652268c5f53b7e2a6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376156"
---
# <a name="process-connection-to-a-window-station"></a><span data-ttu-id="343d4-103">處理與視窗工作站的連接</span><span class="sxs-lookup"><span data-stu-id="343d4-103">Process Connection to a Window Station</span></span>

<span data-ttu-id="343d4-104">程式會在第一次呼叫 USER32 或 GDI32 函式時，自動建立與視窗工作站和桌面的連接， (非視窗工作站和桌面函式) 。</span><span class="sxs-lookup"><span data-stu-id="343d4-104">A process automatically establishes a connection to a window station and desktop when it first calls a USER32 or GDI32 function (other than the window station and desktop functions).</span></span> <span data-ttu-id="343d4-105">系統會根據下列規則，決定進程所要連接的視窗工作站：</span><span class="sxs-lookup"><span data-stu-id="343d4-105">The system determines the window station to which a process connects according to the following rules:</span></span>

1.  <span data-ttu-id="343d4-106">如果進程已呼叫 [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) 函式，它會連接到該呼叫中指定的視窗站。</span><span class="sxs-lookup"><span data-stu-id="343d4-106">If the process has called the [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) function, it connects to the window station specified in that call.</span></span>
2.  <span data-ttu-id="343d4-107">如果處理常式未呼叫 [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)，它會連接到繼承自父進程的視窗站。</span><span class="sxs-lookup"><span data-stu-id="343d4-107">If the process did not call [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation), it connects to the window station inherited from the parent process.</span></span>
3.  <span data-ttu-id="343d4-108">如果處理常式未呼叫 [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) ，且未繼承視窗工作站，系統會嘗試開啟以取得允許的最大 \_ 存取權，並連接到視窗工作站，如下所示：</span><span class="sxs-lookup"><span data-stu-id="343d4-108">If the process did not call [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) and did not inherit a window station, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a window station as follows:</span></span>
    -   <span data-ttu-id="343d4-109">如果在建立進程時所使用之 [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa)結構的 **lpDesktop** 成員中指定了視窗工作站名稱，進程會連接到指定的視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="343d4-109">If a window station name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the process connects to the specified window station.</span></span>
    -   <span data-ttu-id="343d4-110">否則，如果處理常式是在互動式使用者的登入會話中執行，則此程式會連線到互動式視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="343d4-110">Otherwise, if the process is running in the logon session of the interactive user, the process connects to the interactive window station.</span></span>
    -   <span data-ttu-id="343d4-111">如果處理常式是在非互動式登入會話中執行，則會根據登入會話識別碼來形成視窗站名稱，並嘗試開啟該視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="343d4-111">If the process is running in a noninteractive logon session, the window station name is formed based on the logon session identifier and an attempt is made to open that window station.</span></span> <span data-ttu-id="343d4-112">如果開啟作業失敗，因為此視窗工作站不存在，系統會嘗試建立視窗工作站和預設桌面。</span><span class="sxs-lookup"><span data-stu-id="343d4-112">If the open operation fails because this window station does not exist, the system tries to create the window station and a default desktop.</span></span>

<span data-ttu-id="343d4-113">呼叫 [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) 函式時，無法關閉在此連接程式期間指派的視窗站。</span><span class="sxs-lookup"><span data-stu-id="343d4-113">The window station assigned during this connection process cannot be closed by calling the [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) function.</span></span>

<span data-ttu-id="343d4-114">當進程連接到視窗站時，系統會在進程的控制碼資料表中搜尋繼承的控制碼。</span><span class="sxs-lookup"><span data-stu-id="343d4-114">When a process is connecting to a window station, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="343d4-115">系統會使用它所找到的第一個視窗工作站控制碼。</span><span class="sxs-lookup"><span data-stu-id="343d4-115">The system uses the first window station handle it finds.</span></span> <span data-ttu-id="343d4-116">如果您想要讓子進程連接到特定的繼承視窗工作站，您必須確定只將所需的控制碼標示為可繼承。</span><span class="sxs-lookup"><span data-stu-id="343d4-116">If you want a child process to connect to a particular inherited window station, you must ensure that only the desired handle is marked inheritable.</span></span> <span data-ttu-id="343d4-117">如果子進程繼承多個視窗工作站控制碼，則視窗站連接的結果會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="343d4-117">If a child process inherits multiple window station handles, the results of the window station connection are undefined.</span></span>

<span data-ttu-id="343d4-118">系統在將進程連接到視窗工作站時開啟的視窗工作站的控制碼不是可繼承的。</span><span class="sxs-lookup"><span data-stu-id="343d4-118">Handles to a window station that the system opens while connecting a process to a window station are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="343d4-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="343d4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343d4-120">與桌面的執行緒連接</span><span class="sxs-lookup"><span data-stu-id="343d4-120">Thread Connection to a Desktop</span></span>](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 
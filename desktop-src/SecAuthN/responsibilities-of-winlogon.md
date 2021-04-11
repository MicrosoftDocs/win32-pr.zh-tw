---
description: 列出並說明 Winlogon 的責任。
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Winlogon 的責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7842df1d4194dc7086f658a13f6725af8fa0d88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944136"
---
# <a name="responsibilities-of-winlogon"></a><span data-ttu-id="cdd74-103">Winlogon 的責任</span><span class="sxs-lookup"><span data-stu-id="cdd74-103">Responsibilities of Winlogon</span></span>

<span data-ttu-id="cdd74-104">[*Winlogon*](../secgloss/w-gly.md) 具有下列責任：</span><span class="sxs-lookup"><span data-stu-id="cdd74-104">[*Winlogon*](../secgloss/w-gly.md) has the following responsibilities:</span></span>

-   <span data-ttu-id="cdd74-105">視窗站和桌上型電腦保護</span><span class="sxs-lookup"><span data-stu-id="cdd74-105">Window station and desktop protection</span></span>

    <span data-ttu-id="cdd74-106">Winlogon 會設定視窗工作站和對應桌面的保護，以確保每一個都能正確存取。</span><span class="sxs-lookup"><span data-stu-id="cdd74-106">Winlogon sets the protection of the window station and corresponding desktops to ensure that each is properly accessible.</span></span> <span data-ttu-id="cdd74-107">一般而言，這表示本機系統將擁有這些物件的完整存取權，而且以互動方式登入的使用者將擁有視窗站物件的讀取權限，以及應用程式桌面物件的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="cdd74-107">In general, this means that the local system will have full access to these objects and that an interactively logged-on user will have read access to the window station object and full access to the application desktop object.</span></span>

-   <span data-ttu-id="cdd74-108">標準 SAS 辨識</span><span class="sxs-lookup"><span data-stu-id="cdd74-108">Standard SAS recognition</span></span>

    <span data-ttu-id="cdd74-109">Winlogon 在 User32 伺服器中有特殊的勾點，可讓它監視 CTRL + ALT + DEL [*安全的注意順序*](../secgloss/s-gly.md) (SAS) 事件。</span><span class="sxs-lookup"><span data-stu-id="cdd74-109">Winlogon has special hooks into the User32 server that allow it to monitor CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS) events.</span></span> <span data-ttu-id="cdd74-110">Winlogon 會將此 SAS 事件資訊提供給 Gina 使用，以作為 SAS 或其 SAS 的一部分。</span><span class="sxs-lookup"><span data-stu-id="cdd74-110">Winlogon makes this SAS event information available to GINAs to use as their SAS, or as part of their SAS.</span></span> <span data-ttu-id="cdd74-111">一般而言，Gina 應該自行監視 SASs;不過，任何具有標準 CTRL + ALT + DEL SAS 作為其辨識 SASs 的 [*GINA*](../secgloss/g-gly.md) ，都應該使用針對此用途所提供的 Winlogon 支援。</span><span class="sxs-lookup"><span data-stu-id="cdd74-111">In general, GINAs should monitor SASs on their own; however, any [*GINA*](../secgloss/g-gly.md) that has the standard CTRL+ALT+DEL SAS as one of the SASs it recognizes should use the Winlogon support provided for this purpose.</span></span>

-   <span data-ttu-id="cdd74-112">SAS 例行分派</span><span class="sxs-lookup"><span data-stu-id="cdd74-112">SAS routine dispatching</span></span>

    <span data-ttu-id="cdd74-113">當 Winlogon 遇到 SAS 事件或 GINA 提供 SAS 給 Winlogon 時，Winlogon 會據以設定狀態、對 Winlogon 桌面的變更，以及呼叫 GINA 的其中一個 SAS 處理函式。</span><span class="sxs-lookup"><span data-stu-id="cdd74-113">When Winlogon encounters a SAS event or when a SAS is delivered to Winlogon by the GINA, Winlogon sets the state accordingly, changes to the Winlogon desktop, and calls one of the SAS processing functions of the GINA.</span></span>

-   <span data-ttu-id="cdd74-114">使用者設定檔載入</span><span class="sxs-lookup"><span data-stu-id="cdd74-114">User profile loading</span></span>

    <span data-ttu-id="cdd74-115">當使用者登入時，其使用者設定檔會載入至登錄中。</span><span class="sxs-lookup"><span data-stu-id="cdd74-115">When users log on, their user profiles are loaded into the registry.</span></span> <span data-ttu-id="cdd74-116">如此一來，使用者的處理常式就可以使用特殊的登錄機碼 HKEY \_ 目前的 \_ 使用者。</span><span class="sxs-lookup"><span data-stu-id="cdd74-116">In this way, the processes of the user can use the special registry key HKEY\_CURRENT\_USER.</span></span> <span data-ttu-id="cdd74-117">Winlogon 會在成功登入之後，但在啟用新登入使用者的 shell 之前自動執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="cdd74-117">Winlogon does this automatically after a successful logon but before activation of the shell for the newly logged-on user.</span></span>

-   <span data-ttu-id="cdd74-118">將安全性指派給使用者 shell</span><span class="sxs-lookup"><span data-stu-id="cdd74-118">Assignment of security to user shell</span></span>

    <span data-ttu-id="cdd74-119">當使用者登入時，GINA 會負責為該使用者建立一或多個初始進程。</span><span class="sxs-lookup"><span data-stu-id="cdd74-119">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="cdd74-120">Winlogon 會為 GINA 提供支援功能，以將新登入之使用者的安全性套用至這些處理常式。</span><span class="sxs-lookup"><span data-stu-id="cdd74-120">Winlogon provides a support function for the GINA to apply the security of the newly logged-on user to these processes.</span></span> <span data-ttu-id="cdd74-121">不過，最好的方法是讓 GINA 呼叫 Windows 函式 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)，並讓系統提供服務。</span><span class="sxs-lookup"><span data-stu-id="cdd74-121">However, the preferred way to do this is for the GINA to call the Windows function [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera), and let the system provide the service.</span></span>

-   <span data-ttu-id="cdd74-122">螢幕保護裝置控制項</span><span class="sxs-lookup"><span data-stu-id="cdd74-122">Screen saver control</span></span>

    <span data-ttu-id="cdd74-123">Winlogon 會監視鍵盤和滑鼠活動，以決定何時要啟動畫面保護。</span><span class="sxs-lookup"><span data-stu-id="cdd74-123">Winlogon monitors keyboard and mouse activity to determine when to activate screen savers.</span></span> <span data-ttu-id="cdd74-124">啟用螢幕保護裝置之後，Winlogon 會繼續監視鍵盤和滑鼠活動，以判斷何時終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="cdd74-124">After the screen saver is activated, Winlogon continues to monitor keyboard and mouse activity to determine when to terminate the screen saver.</span></span> <span data-ttu-id="cdd74-125">如果螢幕保護裝置標示為安全，則 Winlogon 會將工作站視為鎖定。</span><span class="sxs-lookup"><span data-stu-id="cdd74-125">If the screen saver is marked as secure, Winlogon treats the workstation as locked.</span></span> <span data-ttu-id="cdd74-126">當有滑鼠或鍵盤活動時，Winlogon 會叫用 GINA 的 [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) 函式，而鎖定的工作站行為會繼續。</span><span class="sxs-lookup"><span data-stu-id="cdd74-126">When there is mouse or keyboard activity, Winlogon invokes the [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) function of the GINA and locked workstation behavior resumes.</span></span> <span data-ttu-id="cdd74-127">如果螢幕保護裝置不安全，任何鍵盤或滑鼠活動都會終止螢幕保護裝置，而不會通知 GINA。</span><span class="sxs-lookup"><span data-stu-id="cdd74-127">If the screen saver is not secure, any keyboard or mouse activity terminates the screen saver without notification to the GINA.</span></span>

-   <span data-ttu-id="cdd74-128">多個網路提供者支援</span><span class="sxs-lookup"><span data-stu-id="cdd74-128">Multiple network provider support</span></span>

    <span data-ttu-id="cdd74-129">在 Windows 系統上安裝的多個網路可以包含在驗證程式和密碼更新作業中。</span><span class="sxs-lookup"><span data-stu-id="cdd74-129">Multiple networks installed on a Windows system can be included in the authentication process and in password-updating operations.</span></span> <span data-ttu-id="cdd74-130">這項包含可讓其他網路在正常登入期間，使用 Winlogon 的安全桌面，同時收集識別和驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="cdd74-130">This inclusion lets additional networks gather identification and authentication information all at once during normal logon, using the secure desktop of Winlogon.</span></span> <span data-ttu-id="cdd74-131">Gina 可供您明確支援這些額外網路提供者的 Winlogon 服務中所需的某些參數。</span><span class="sxs-lookup"><span data-stu-id="cdd74-131">Some of the parameters required in the Winlogon services available to GINAs explicitly support these additional network providers.</span></span>

 

 

---
description: Winlogon 會維護 GINA 所使用的工作站狀態，以判斷需要哪些驗證動作。
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Winlogon 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556227"
---
# <a name="winlogon-states"></a><span data-ttu-id="4af27-103">Winlogon 狀態</span><span class="sxs-lookup"><span data-stu-id="4af27-103">Winlogon States</span></span>

<span data-ttu-id="4af27-104">[*Winlogon*](../secgloss/w-gly.md) 會維護 [*GINA*](../secgloss/g-gly.md) 所使用的工作站狀態，以判斷需要哪些驗證動作。</span><span class="sxs-lookup"><span data-stu-id="4af27-104">[*Winlogon*](../secgloss/w-gly.md) maintains the workstation state that is used by the [*GINA*](../secgloss/g-gly.md) to determine what authentication actions are required.</span></span>

<span data-ttu-id="4af27-105">在任何時間點，Winlogon 都處於下列三種狀態之一：</span><span class="sxs-lookup"><span data-stu-id="4af27-105">At any point in time, Winlogon is in one of three states:</span></span>

-   [<span data-ttu-id="4af27-106">已登出狀態</span><span class="sxs-lookup"><span data-stu-id="4af27-106">Logged-Off State</span></span>](#logged-off-state)
-   [<span data-ttu-id="4af27-107">登入狀態</span><span class="sxs-lookup"><span data-stu-id="4af27-107">Logged-On State</span></span>](#logged-on-state)
-   [<span data-ttu-id="4af27-108">工作站鎖定狀態</span><span class="sxs-lookup"><span data-stu-id="4af27-108">Workstation-Locked State</span></span>](#workstation-locked-state)

<span data-ttu-id="4af27-109">下圖顯示這三種狀態。</span><span class="sxs-lookup"><span data-stu-id="4af27-109">These three states are shown in the following illustration.</span></span>

![winlogon 州](images/winlogonst.png)

## <a name="logged-off-state"></a><span data-ttu-id="4af27-111">Logged-Off 狀態</span><span class="sxs-lookup"><span data-stu-id="4af27-111">Logged-Off State</span></span>

<span data-ttu-id="4af27-112">當 Winlogon 處於已登出狀態時，系統會提示使用者識別自己並提供驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="4af27-112">When Winlogon is in the logged-off state, users are prompted to identify themselves and provide authentication information.</span></span> <span data-ttu-id="4af27-113">如果使用者提供正確的使用者帳戶資訊，且沒有任何限制，則使用者會登入，而 shell 程式 (例如 Windows 檔案總管) 會在應用程式桌面上執行。</span><span class="sxs-lookup"><span data-stu-id="4af27-113">If a user provides correct user account information and no restrictions prevent it, the user is logged on and a shell program (such as Windows Explorer) is executed in the application desktop.</span></span> <span data-ttu-id="4af27-114">Winlogon 變更為登入狀態。</span><span class="sxs-lookup"><span data-stu-id="4af27-114">Winlogon changes to the logged-on state.</span></span>

## <a name="logged-on-state"></a><span data-ttu-id="4af27-115">Logged-On 狀態</span><span class="sxs-lookup"><span data-stu-id="4af27-115">Logged-On State</span></span>

<span data-ttu-id="4af27-116">當 Winlogon 處於登入狀態時，使用者可以與 shell 互動、啟動其他應用程式，以及執行其工作。</span><span class="sxs-lookup"><span data-stu-id="4af27-116">When Winlogon is in the logged-on state, users can interact with the shell, activate additional applications, and do their work.</span></span> <span data-ttu-id="4af27-117">從登入狀態中，使用者可以停止所有工作並登出，或鎖定工作站 (將所有工作保留) 。</span><span class="sxs-lookup"><span data-stu-id="4af27-117">From the logged-on state, users can either stop all work and log off, or lock their workstations (leaving all work in place).</span></span> <span data-ttu-id="4af27-118">如果使用者決定登出，則 Winlogon 將會終止與該 [*登入會話*](../secgloss/l-gly.md) 相關聯的所有進程，而且工作站將可供其他使用者使用。</span><span class="sxs-lookup"><span data-stu-id="4af27-118">If the user decides to log off, Winlogon will terminate all processes associated with that [*logon session*](../secgloss/l-gly.md) and the workstation will be available for another user.</span></span> <span data-ttu-id="4af27-119">相反地，如果使用者決定鎖定工作站，則 Winlogon 會變更為工作站鎖定狀態。</span><span class="sxs-lookup"><span data-stu-id="4af27-119">If, instead, the user decides to lock the workstation, Winlogon changes to the workstation-locked state.</span></span>

## <a name="workstation-locked-state"></a><span data-ttu-id="4af27-120">Workstation-Locked 狀態</span><span class="sxs-lookup"><span data-stu-id="4af27-120">Workstation-Locked State</span></span>

<span data-ttu-id="4af27-121">當 Winlogon 處於工作站鎖定狀態時，會顯示安全桌面，直到使用者解除鎖定工作站，方法是提供與原本登入的使用者相同的識別和驗證資訊，或在系統管理員強制登出之前。</span><span class="sxs-lookup"><span data-stu-id="4af27-121">When Winlogon is in the workstation-locked state, a secure desktop is displayed until the user unlocks the workstation by providing the same identification and authentication information as the user who originally logged on, or until an administrator forces a logoff.</span></span> <span data-ttu-id="4af27-122">如果工作站已解除鎖定，則會顯示應用程式桌面，而且可以繼續工作。</span><span class="sxs-lookup"><span data-stu-id="4af27-122">If the workstation is unlocked, the application desktop is displayed, and work can resume.</span></span> <span data-ttu-id="4af27-123">但是，如果系統管理員藉由提供系統管理員帳戶) 的識別和驗證資訊來解除鎖定工作站 (，已登入使用者的處理常式會終止，而 Winlogon 會變更為已登出狀態。</span><span class="sxs-lookup"><span data-stu-id="4af27-123">If, however, an administrator unlocks the workstation (by providing the identification and authentication information of an administrator account), the processes of the logged-on user are terminated, and Winlogon changes to the logged-off state.</span></span>

<span data-ttu-id="4af27-124">您可以在每個 Winlogon 狀態中執行許多不同的動作。</span><span class="sxs-lookup"><span data-stu-id="4af27-124">A number of different actions can be performed in each of the Winlogon states.</span></span> <span data-ttu-id="4af27-125">GINA DLL 可執行不屬於標準 Windows 作業系統的動作。</span><span class="sxs-lookup"><span data-stu-id="4af27-125">A GINA DLL may implement actions that are not part of the standard Windows operating system.</span></span> <span data-ttu-id="4af27-126">例如，高安全性系統可能會每隔10分鐘自動鎖定工作站，並強制使用者自行重新驗證。</span><span class="sxs-lookup"><span data-stu-id="4af27-126">For example, a high security system could automatically lock a workstation every 10 minutes and force users to reauthenticate themselves.</span></span>

<span data-ttu-id="4af27-127">如需建立桌上型電腦以及註冊 (SAS) 之 [*安全注意順序*](../secgloss/s-gly.md) 的相關資訊，請參閱 [初始化 Winlogon](initializing-winlogon.md)。</span><span class="sxs-lookup"><span data-stu-id="4af27-127">For information about creating desktops and registering a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), see [Initializing Winlogon](initializing-winlogon.md).</span></span> <span data-ttu-id="4af27-128">如需超時作業的相關資訊，請參閱 [支援的對話方塊服務超時作業](supported-dialog-box-service-time-out-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="4af27-128">For information about time-out operations, see [Supported Dialog Box Service Time-out Operations](supported-dialog-box-service-time-out-operations.md).</span></span> <span data-ttu-id="4af27-129">如需在顯示對話方塊時將訊息傳送至 GINA 的詳細資訊，請參閱將 [訊息傳送至 GINA](sending-messages-to-the-gina.md)。</span><span class="sxs-lookup"><span data-stu-id="4af27-129">For information about sending messages to the GINA while a dialog box is displayed, see [Sending Messages to the GINA](sending-messages-to-the-gina.md).</span></span> <span data-ttu-id="4af27-130">如需支援函式的詳細資訊，請參閱 [Winlogon 支援功能](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="4af27-130">For information about support functions, see [Winlogon Support Functions](authentication-functions.md).</span></span>

 

 

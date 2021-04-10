---
description: 當 Winlogon 初始化時，它會向系統 (SAS) 註冊 CTRL + ALT + DEL 安全的注意順序，然後在 WinSta0 視窗站內建立三部桌上型電腦。
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: 正在初始化 Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768983d308228e73316c797fb67b035d491a1582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194513"
---
# <a name="initializing-winlogon"></a><span data-ttu-id="3810e-103">正在初始化 Winlogon</span><span class="sxs-lookup"><span data-stu-id="3810e-103">Initializing Winlogon</span></span>

<span data-ttu-id="3810e-104">當 [Winlogon](winlogon.md) 初始化時，它會向系統 (SAS) 註冊 CTRL + ALT + DEL [*安全的注意順序*](../secgloss/s-gly.md) ，然後在 WinSta0 視窗站內建立三部桌上型電腦。</span><span class="sxs-lookup"><span data-stu-id="3810e-104">When [Winlogon](winlogon.md) initializes, it registers the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS) with the system, and then creates three desktops within the WinSta0 window station.</span></span>

<span data-ttu-id="3810e-105">註冊 CTRL + ALT + DEL 會使此初始化成為第一個進程，因此可確保沒有任何其他應用程式已與該金鑰順序連結。</span><span class="sxs-lookup"><span data-stu-id="3810e-105">Registering CTRL+ALT+DEL makes this initialization the first process, thus ensuring that no other application has hooked that key sequence.</span></span>

<span data-ttu-id="3810e-106">WinSta0 是代表實體螢幕、鍵盤和滑鼠的視窗站物件名稱。</span><span class="sxs-lookup"><span data-stu-id="3810e-106">WinSta0 is the name of the window station object that represents the physical screen, keyboard and mouse.</span></span> <span data-ttu-id="3810e-107">Winlogon 會在 WinSta0 物件中建立下列桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-107">Winlogon creates the following desktops in the WinSta0 object.</span></span>



| <span data-ttu-id="3810e-108">桌面</span><span class="sxs-lookup"><span data-stu-id="3810e-108">Desktop</span></span>              | <span data-ttu-id="3810e-109">Description</span><span class="sxs-lookup"><span data-stu-id="3810e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3810e-110">Winlogon 桌面</span><span class="sxs-lookup"><span data-stu-id="3810e-110">Winlogon desktop</span></span>     | <span data-ttu-id="3810e-111">這是 Winlogon 和 [*GINA*](../secgloss/g-gly.md) 用於互動式識別和驗證以及其他安全對話方塊的桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-111">This is the desktop that Winlogon and [*GINA*](../secgloss/g-gly.md) use for interactive identification and authentication, and other secure dialog boxes.</span></span> <span data-ttu-id="3810e-112">Winlogon 會在收到 SAS 事件通知時自動切換到此桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-112">Winlogon automatically switches to this desktop when it receives SAS event notification.</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3810e-113">應用程式桌面</span><span class="sxs-lookup"><span data-stu-id="3810e-113">Application desktop</span></span>  | <span data-ttu-id="3810e-114">每次使用者成功登入時，就會為該 [*登入會話*](../secgloss/l-gly.md)建立應用程式桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-114">Each time a user successfully logs on, an application desktop is created for that [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="3810e-115">應用程式桌面也稱為預設或使用者桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-115">The application desktop is also known as the default or user desktop.</span></span> <span data-ttu-id="3810e-116">此桌面是所有使用者活動發生的位置。</span><span class="sxs-lookup"><span data-stu-id="3810e-116">This desktop is where all user activity takes place.</span></span> <span data-ttu-id="3810e-117">應用程式桌面受保護;只有系統和互動式登入會話可以存取它。</span><span class="sxs-lookup"><span data-stu-id="3810e-117">The application desktop is protected; only the system and the interactive logon session have access to it.</span></span> <span data-ttu-id="3810e-118">請注意，只有已登入使用者的特定實例可以存取桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-118">Note that only a particular instance of the logged-on user has access to the desktop.</span></span> <span data-ttu-id="3810e-119">如果互動式使用者使用服務控制器啟動處理常式，該服務應用程式將無法存取應用程式桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-119">If the interactive user activates a process using the service controller, that service application will not have access to the application desktop.</span></span> |
| <span data-ttu-id="3810e-120">螢幕保護裝置桌面</span><span class="sxs-lookup"><span data-stu-id="3810e-120">Screen saver desktop</span></span> | <span data-ttu-id="3810e-121">當螢幕保護裝置正在執行時，這是目前的桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-121">This is the current desktop when a screen saver is running.</span></span> <span data-ttu-id="3810e-122">如果使用者已登入，則系統和互動式登入會話都可以存取桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-122">If a user is logged on, both the system and the interactive logon session have access to the desktop.</span></span> <span data-ttu-id="3810e-123">否則，只有系統可以存取桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-123">Otherwise, only the system has access to the desktop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

<span data-ttu-id="3810e-124">Winlogon 是這些桌面的擁有者，可以將目前或可見的桌面切換至三部桌上型電腦，並允許 GINA 存取這項功能。</span><span class="sxs-lookup"><span data-stu-id="3810e-124">As the owner of these desktops, Winlogon can switch the current, or visible, desktop to any of the three desktops and allow the GINA access to this functionality.</span></span> <span data-ttu-id="3810e-125">一般而言，GINA 開發人員不會變更目前的桌面，因為 Winlogon 會在與 GINA 通訊之前適當設定桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-125">In general, GINA developers will not change the current desktop because Winlogon sets the desktop appropriately before communicating with the GINA.</span></span> <span data-ttu-id="3810e-126">每個 GINA 函式的描述會指出該呼叫的最新桌面。</span><span class="sxs-lookup"><span data-stu-id="3810e-126">The description of each GINA function indicates which desktop is current for that call.</span></span>



| <span data-ttu-id="3810e-127">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="3810e-127">For information about</span></span>                                    | <span data-ttu-id="3810e-128">請參閱</span><span class="sxs-lookup"><span data-stu-id="3810e-128">See</span></span>                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3810e-129">Winlogon 可以執行的不同狀態</span><span class="sxs-lookup"><span data-stu-id="3810e-129">The different states in which Winlogon can run</span></span>           | [<span data-ttu-id="3810e-130">Winlogon 狀態</span><span class="sxs-lookup"><span data-stu-id="3810e-130">Winlogon States</span></span>](winlogon-states.md)                                                                   |
| <span data-ttu-id="3810e-131">超時作業</span><span class="sxs-lookup"><span data-stu-id="3810e-131">Time out operations</span></span>                                      | [<span data-ttu-id="3810e-132">支援的對話方塊服務超時作業</span><span class="sxs-lookup"><span data-stu-id="3810e-132">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md) |
| <span data-ttu-id="3810e-133">顯示對話方塊時將訊息傳送至 GINA</span><span class="sxs-lookup"><span data-stu-id="3810e-133">Sending messages to GINA while a dialog box is displayed</span></span> | [<span data-ttu-id="3810e-134">將訊息傳送至 GINA</span><span class="sxs-lookup"><span data-stu-id="3810e-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)                                         |
| <span data-ttu-id="3810e-135">支援函式</span><span class="sxs-lookup"><span data-stu-id="3810e-135">Support functions</span></span>                                        | [<span data-ttu-id="3810e-136">Winlogon 支援函式</span><span class="sxs-lookup"><span data-stu-id="3810e-136">Winlogon Support Functions</span></span>](authentication-functions.md)                    |



 

 

 

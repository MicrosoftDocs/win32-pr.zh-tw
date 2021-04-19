---
title: 桌上型電腦
description: 桌面具有邏輯顯示介面，且包含使用者介面物件，例如 windows、功能表和勾點;可以用來建立和管理 windows。
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- 桌面物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ca0b390ec4d34cc943c9d18d958cdea6466634
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966256"
---
# <a name="desktops"></a><span data-ttu-id="b36f4-104">桌上型電腦</span><span class="sxs-lookup"><span data-stu-id="b36f4-104">Desktops</span></span>

<span data-ttu-id="b36f4-105">*桌面* 具有邏輯顯示介面，且包含使用者介面物件，例如 windows、功能表和勾點;可以用來建立和管理 windows。</span><span class="sxs-lookup"><span data-stu-id="b36f4-105">A *desktop* has a logical display surface and contains user interface objects such as windows, menus, and hooks; it can be used to create and manage windows.</span></span> <span data-ttu-id="b36f4-106">每個桌面物件都是安全物件。</span><span class="sxs-lookup"><span data-stu-id="b36f4-106">Each desktop object is a securable object.</span></span> <span data-ttu-id="b36f4-107">建立桌面時，它會與目前呼叫進程的 [視窗站](window-stations.md) 相關聯，並指派給呼叫的執行緒。</span><span class="sxs-lookup"><span data-stu-id="b36f4-107">When a desktop is created, it is associated with the current [window station](window-stations.md) of the calling process and assigned to the calling thread.</span></span>

<span data-ttu-id="b36f4-108">視窗訊息只能在相同桌面上的進程之間傳送。</span><span class="sxs-lookup"><span data-stu-id="b36f4-108">Window messages can be sent only between processes that are on the same desktop.</span></span> <span data-ttu-id="b36f4-109">此外，在特定桌上型電腦上執行之處理常式的攔截程式，只能接收在相同桌面上建立之 windows 的訊息。</span><span class="sxs-lookup"><span data-stu-id="b36f4-109">In addition, the hook procedure of a process running on a particular desktop can only receive messages intended for windows created in the same desktop.</span></span>

<span data-ttu-id="b36f4-110">您可以建立與互動式視窗工作站 Winsta0 相關聯的桌面，以顯示使用者介面並接收使用者輸入，但一次只能有一部桌上型電腦處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="b36f4-110">The desktops associated with the interactive window station, Winsta0, can be made to display a user interface and receive user input, but only one of these desktops at a time is active.</span></span> <span data-ttu-id="b36f4-111">此作用中的桌面（也稱為 *輸入桌面*）是使用者目前看到的使用者，以及接收使用者輸入的桌面。</span><span class="sxs-lookup"><span data-stu-id="b36f4-111">This active desktop, also known as the *input desktop*, is the one that is currently visible to the user and that receives user input.</span></span> <span data-ttu-id="b36f4-112">應用程式可以使用 [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) 函式來取得輸入桌面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b36f4-112">Applications can use the [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function to get a handle to the input desktop.</span></span> <span data-ttu-id="b36f4-113">具有必要存取權的應用程式可以使用 [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) 函數來指定不同的輸入桌面。</span><span class="sxs-lookup"><span data-stu-id="b36f4-113">Applications that have the required access can use the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function to specify a different input desktop.</span></span>

<span data-ttu-id="b36f4-114">根據預設，互動式視窗工作站中有三個桌面：預設、螢幕保護裝置和 Winlogon。</span><span class="sxs-lookup"><span data-stu-id="b36f4-114">By default, there are three desktops in the interactive window station: Default, ScreenSaver, and Winlogon.</span></span>

<span data-ttu-id="b36f4-115">當 Winlogon 以登入的使用者身分啟動初始進程時，就會建立預設桌面。</span><span class="sxs-lookup"><span data-stu-id="b36f4-115">The Default desktop is created when Winlogon starts the initial process as the logged-on user.</span></span> <span data-ttu-id="b36f4-116">屆時，預設桌面會變成作用中狀態，並用來與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="b36f4-116">At that point, the Default desktop becomes active, and it is used to interact with the user.</span></span>

<span data-ttu-id="b36f4-117">當安全的螢幕保護裝置啟動時，系統會自動切換到螢幕保護裝置程式桌面，以防止未經授權的使用者使用預設桌面上的進程。</span><span class="sxs-lookup"><span data-stu-id="b36f4-117">Whenever a secure screen saver activates, the system automatically switches to the ScreenSaver desktop, which protects the processes on the default desktop from unauthorized users.</span></span> <span data-ttu-id="b36f4-118">不安全的螢幕保護裝置會在 Winsta0 預設上執行 \\ 。</span><span class="sxs-lookup"><span data-stu-id="b36f4-118">Unsecured screen savers run on Winsta0\\Default.</span></span>

<span data-ttu-id="b36f4-119">當使用者登入時，Winlogon 桌面會處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="b36f4-119">The Winlogon desktop is active while a user logs on.</span></span> <span data-ttu-id="b36f4-120">當 shell 指出它已準備好顯示某個東西，或30秒後（以先發生者為准）時，系統會切換至預設桌面。</span><span class="sxs-lookup"><span data-stu-id="b36f4-120">The system switches to the default desktop when the shell indicates that it is ready to display something, or after thirty seconds, whichever comes first.</span></span> <span data-ttu-id="b36f4-121">在使用者會話期間，當使用者按下 CTRL + ALT + DEL 鍵序列，或開啟 [使用者帳戶控制] (UAC) ] 對話方塊時，系統會切換至 Winlogon 桌面。</span><span class="sxs-lookup"><span data-stu-id="b36f4-121">During the user's session, the system switches to the Winlogon desktop when the user presses the CTRL+ALT+DEL key sequence, or when the User Account Control (UAC) dialog box is open.</span></span>

<span data-ttu-id="b36f4-122">**Windows Server 2003 和 WINDOWS XP/2000：** 不支援 UAC 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b36f4-122">**Windows Server 2003 and Windows XP/2000:** The UAC dialog box is not supported.</span></span>

<span data-ttu-id="b36f4-123">Winlogon 桌面的安全描述項允許存取一組非常受限制的帳戶，包括 [LocalSystem 帳戶](/windows/desktop/Services/localsystem-account)。</span><span class="sxs-lookup"><span data-stu-id="b36f4-123">The Winlogon desktop's security descriptor allows access to a very restricted set of accounts, including the [LocalSystem account](/windows/desktop/Services/localsystem-account).</span></span> <span data-ttu-id="b36f4-124">應用程式通常不會在其權杖中攜帶任何這些帳戶的 Sid，因此無法存取 Winlogon 桌面或在 Winlogon 桌面作用中時切換至不同的桌面。</span><span class="sxs-lookup"><span data-stu-id="b36f4-124">Applications generally do not carry any of these accounts' SIDs in their tokens and therefore cannot access the Winlogon desktop or switch to a different desktop while the Winlogon desktop is active.</span></span>

<span data-ttu-id="b36f4-125">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="b36f4-125">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b36f4-126">視窗工作站和桌面建立</span><span class="sxs-lookup"><span data-stu-id="b36f4-126">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="b36f4-127">與桌面的執行緒連接</span><span class="sxs-lookup"><span data-stu-id="b36f4-127">Thread Connection to a Desktop</span></span>](thread-connection-to-a-desktop.md)
-   [<span data-ttu-id="b36f4-128">桌面安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="b36f4-128">Desktop Security and Access Rights</span></span>](desktop-security-and-access-rights.md)

 

 
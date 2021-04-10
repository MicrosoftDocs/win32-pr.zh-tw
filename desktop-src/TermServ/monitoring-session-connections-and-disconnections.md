---
title: 監視會話連線和中斷連接
description: 若要向遠端桌面服務註冊應用程式，請新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中。
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023580"
---
# <a name="monitoring-session-connections-and-disconnections"></a><span data-ttu-id="95089-103">監視會話連線和中斷連接</span><span class="sxs-lookup"><span data-stu-id="95089-103">Monitoring session connections and disconnections</span></span>

<span data-ttu-id="95089-104">針對服務應用程式（例如虛擬通道伺服器應用程式），若要監視會話連線和中斷連接，您必須向遠端桌面服務註冊。</span><span class="sxs-lookup"><span data-stu-id="95089-104">For a service application, such as a virtual channel server application, to monitor session connections and disconnections, you must register it with Remote Desktop Services.</span></span> <span data-ttu-id="95089-105">若要向遠端桌面服務註冊應用程式，請在下列位置下新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中：</span><span class="sxs-lookup"><span data-stu-id="95089-105">To register the application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="95089-106">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **TerminalServer** \\ **載入** 宏</span><span class="sxs-lookup"><span data-stu-id="95089-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**</span></span>

<span data-ttu-id="95089-107">子機碼可以有任何名稱。</span><span class="sxs-lookup"><span data-stu-id="95089-107">The subkey can have any name.</span></span> <span data-ttu-id="95089-108">它必須有一個包含應用程式符號名稱的 **REG \_ SZ** 值 **name**。</span><span class="sxs-lookup"><span data-stu-id="95089-108">It must have a **REG\_SZ** value, **Name**, that contains the symbolic name of the application.</span></span>

``` syntax
Name = AddinName
```

<span data-ttu-id="95089-109">子機碼和 **Name** 值的最大長度為99個字元。</span><span class="sxs-lookup"><span data-stu-id="95089-109">The maximum length of both the subkey and the value of **Name** is 99 characters.</span></span>

<span data-ttu-id="95089-110">子機碼也必須有指示伺服器應用程式類型的 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="95089-110">The subkey must also have a **REG\_DWORD** value that indicates the type of server application.</span></span>

``` syntax
Type = AddinType
```

<span data-ttu-id="95089-111">*AddinType* 必須是下列值。</span><span class="sxs-lookup"><span data-stu-id="95089-111">*AddinType* must be the following value.</span></span>



| <span data-ttu-id="95089-112">值</span><span class="sxs-lookup"><span data-stu-id="95089-112">Value</span></span> | <span data-ttu-id="95089-113">意義</span><span class="sxs-lookup"><span data-stu-id="95089-113">Meaning</span></span>                               |
|-------|---------------------------------------|
| <span data-ttu-id="95089-114">3</span><span class="sxs-lookup"><span data-stu-id="95089-114">3</span></span>     | <span data-ttu-id="95089-115">使用者模式應用程式、會話空間。</span><span class="sxs-lookup"><span data-stu-id="95089-115">User-mode application, session space.</span></span> |



 

<span data-ttu-id="95089-116">服務應用程式的註冊只會在執行註冊之後建立的會話中生效。</span><span class="sxs-lookup"><span data-stu-id="95089-116">Registration of the service application takes effect only in sessions created after the registration was performed.</span></span>

<span data-ttu-id="95089-117">針對每個已註冊的服務應用程式，遠端桌面服務會在用戶端連接或中斷會話的連線時，發出一組事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="95089-117">For each registered service application, Remote Desktop Services will signal a set of event objects when a client connects or disconnects from the session.</span></span> <span data-ttu-id="95089-118">每個虛擬通道外掛程式都必須註冊自己，並藉由呼叫 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)來建立通知事件。</span><span class="sxs-lookup"><span data-stu-id="95089-118">Each virtual channel plug-in must register itself and create the notification events by calling [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span></span> <span data-ttu-id="95089-119">這些事件物件的名稱會遵循下列格式。</span><span class="sxs-lookup"><span data-stu-id="95089-119">The names of these event objects adhere to the following format.</span></span>

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

<span data-ttu-id="95089-120">*AddinName* 是在註冊伺服器應用程式所用之登錄子機碼的 **名稱** 值中所指定的字串。</span><span class="sxs-lookup"><span data-stu-id="95089-120">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="95089-121">在會話下建立這些事件，會在特定的每個會話事件目錄中建立這些事件。</span><span class="sxs-lookup"><span data-stu-id="95089-121">Creating these events under a session causes them to be created in a special per-session event directory.</span></span> <span data-ttu-id="95089-122">事件目錄可以防止其他會話中的應用程式修改這些事件的狀態，以提供額外的安全性。</span><span class="sxs-lookup"><span data-stu-id="95089-122">The event directory provides added security by preventing applications in other sessions from modifying the state of these events.</span></span>

<span data-ttu-id="95089-123">若要控制是否要在伺服器上收到重新連接和中斷連接事件，您可以在登錄中將 **RemoteControlPersistent** 旗標放在下列機碼底下：</span><span class="sxs-lookup"><span data-stu-id="95089-123">To control whether RECONNECT and DISCONNECT events are received on the server, you can place the **RemoteControlPersistent** flag in the registry under the following key:</span></span>

<span data-ttu-id="95089-124">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **TerminalServer** \\ **載入** 宏 \\ *addinname*</span><span class="sxs-lookup"><span data-stu-id="95089-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**\\*addinname*</span></span>

<span data-ttu-id="95089-125">旗標可啟用或停用在用戶端會話啟動或停止時發出的重新連接和中斷線上活動。</span><span class="sxs-lookup"><span data-stu-id="95089-125">The flag enables or disables RECONNECT and DISCONNECT events from being signaled when a client session starts or stops.</span></span> <span data-ttu-id="95089-126">**REG \_ DWORD** 值的語法如下所示。</span><span class="sxs-lookup"><span data-stu-id="95089-126">The syntax of the **REG\_DWORD** value is the following.</span></span>

``` syntax
RemoteControlPersistent = flag
```

<span data-ttu-id="95089-127">*旗* 標的值可以是一或零。</span><span class="sxs-lookup"><span data-stu-id="95089-127">The value of *flag* can be one or zero.</span></span> <span data-ttu-id="95089-128">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="95089-128">Zero is the default value.</span></span> <span data-ttu-id="95089-129">如果設定為1，當用戶端會話啟動或停止時，服務應用程式將不會收到通知。</span><span class="sxs-lookup"><span data-stu-id="95089-129">If set to one, the service application will not be notified if the client session is started or stopped.</span></span> <span data-ttu-id="95089-130">如果設定為零，當用戶端會話啟動時，重新連接事件就會收到信號，並在用戶端會話停止時發出中斷線上活動。</span><span class="sxs-lookup"><span data-stu-id="95089-130">If set to zero, a RECONNECT event is signaled when the client session starts, and a DISCONNECT event is signaled when the client session stops.</span></span>

<span data-ttu-id="95089-131">在 Windows Server 2008 中仍支援先前的事件物件名稱格式，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="95089-131">The previous event-object name format is still supported in Windows Server 2008 for backward compatibility.</span></span> <span data-ttu-id="95089-132">建議您使用較新的 Windows Server 2008 格式，因為它比較安全。</span><span class="sxs-lookup"><span data-stu-id="95089-132">It is recommended that you use the newer Windows Server 2008 format because it is more secure.</span></span>

<span data-ttu-id="95089-133">先前的事件格式如下所示。</span><span class="sxs-lookup"><span data-stu-id="95089-133">The previous event format is as follows.</span></span>

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

<span data-ttu-id="95089-134">*AddinName* 是在註冊伺服器應用程式所用之登錄子機碼的 **名稱** 值中所指定的字串。</span><span class="sxs-lookup"><span data-stu-id="95089-134">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="95089-135">*SessionId* 是用戶端會話的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="95089-135">*SessionId* is the session identifier of a client session.</span></span>

 

 
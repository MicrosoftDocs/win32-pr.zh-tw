---
title: 連接狀態
description: 在連接到遠端伺服器的過程中，遠端存取連線管理員和遠端電腦上的 RAS 伺服器會執行幾個步驟來建立連線。
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4488cc020a8a1b2a7da93384a4a5be1edb5182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842515"
---
# <a name="connection-states"></a><span data-ttu-id="66330-103">連接狀態</span><span class="sxs-lookup"><span data-stu-id="66330-103">Connection States</span></span>

<span data-ttu-id="66330-104">在連接到遠端伺服器的過程中，遠端存取連線管理員和遠端電腦上的 RAS 伺服器會執行幾個步驟來建立連線。</span><span class="sxs-lookup"><span data-stu-id="66330-104">During the process of connecting to a remote server, the Remote Access Connection Manager and the RAS server on the remote computer perform several steps to establish the connection.</span></span> <span data-ttu-id="66330-105">每個步驟都是由連接狀態所識別。</span><span class="sxs-lookup"><span data-stu-id="66330-105">Each of these steps is identified by a connection state.</span></span> <span data-ttu-id="66330-106">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))列舉是對應至這些連接狀態的一組值。</span><span class="sxs-lookup"><span data-stu-id="66330-106">The [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumeration is a set of values that correspond to these connection states.</span></span> <span data-ttu-id="66330-107">連接狀態可以分成下列三個群組：</span><span class="sxs-lookup"><span data-stu-id="66330-107">The connection states can be divided into the following three groups:</span></span>

<dl> <dt>

<span data-ttu-id="66330-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>正在執行狀態</span><span class="sxs-lookup"><span data-stu-id="66330-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Running states</span></span>
</dt> <dd>

<span data-ttu-id="66330-109">「執行中」狀態是 RAS 自動處理的連接作業部分，例如連接到必要的裝置、驗證使用者，以及等待遠端伺服器的回呼。</span><span class="sxs-lookup"><span data-stu-id="66330-109">The running states are the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="66330-110">除非發生錯誤，否則 RAS 用戶端不需要採取任何動作，就能將通知傳遞給使用者。</span><span class="sxs-lookup"><span data-stu-id="66330-110">Unless an error occurs, the RAS client need take no action other than to pass the notification on to the user.</span></span>

</dd> <dt>

<span data-ttu-id="66330-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>暫停狀態</span><span class="sxs-lookup"><span data-stu-id="66330-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Paused states</span></span>
</dt> <dd>

<span data-ttu-id="66330-112">當遠端伺服器暫停連接作業來取得使用者的其他輸入時，就會發生 [暫停狀態](paused-states.md) 。</span><span class="sxs-lookup"><span data-stu-id="66330-112">The [paused states](paused-states.md) occur when the remote server pauses the connection operation to get additional input from the user.</span></span> <span data-ttu-id="66330-113">在暫停狀態期間，使用者可以輸入 [回呼](callback-connections.md) 號碼、在使用者驗證失敗時輸入不同的使用者名稱和密碼，或在舊密碼過期時輸入新的密碼。</span><span class="sxs-lookup"><span data-stu-id="66330-113">During a paused state, the user can type a [callback](callback-connections.md) number, a different user name and password if the user authentication fails, or a new password if the old one has expired.</span></span>

</dd> <dt>

<span data-ttu-id="66330-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>終端州</span><span class="sxs-lookup"><span data-stu-id="66330-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal states</span></span>
</dt> <dd>

<span data-ttu-id="66330-115">當成功建立連線、連接作業失敗，或 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 呼叫中斷連接時，就會發生終端機狀態。</span><span class="sxs-lookup"><span data-stu-id="66330-115">The terminal states occur when the connection has been successfully established, the connection operation has failed, or the connection has been broken by a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) call.</span></span>

</dd> </dl>

<span data-ttu-id="66330-116">有幾個機制可供 RAS 用戶端用來判斷連接操作的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="66330-116">There are several mechanisms that a RAS client can use to determine the current state of a connection operation.</span></span> <span data-ttu-id="66330-117">當 RAS 用戶端以非同步方式執行 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式時，遠端存取連線管理員會在連接狀態變更時，將進度通知傳送至用戶端的 [通知處理常式](notification-handlers.md) 。</span><span class="sxs-lookup"><span data-stu-id="66330-117">When a RAS client executes the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function asynchronously, the Remote Access Connection Manager sends progress notifications to the client's [notification handler](notification-handlers.md) whenever the connection state changes.</span></span> <span data-ttu-id="66330-118">此外，用戶端可以使用 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函式來取得任何 RAS 連接作業的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="66330-118">In addition, the client can use the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the current state of any RAS connection operation.</span></span>

 

 
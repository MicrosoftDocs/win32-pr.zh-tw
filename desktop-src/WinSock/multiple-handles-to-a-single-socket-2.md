---
description: 由於複製的內容是通訊端描述項，而不是基礎通訊端，因此與通訊端相關聯的所有狀態都會保留在所有描述項的通用範圍內。
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: 單一通訊端的多個控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970167"
---
# <a name="multiple-handles-to-a-single-socket"></a><span data-ttu-id="83bc0-103">單一通訊端的多個控制碼</span><span class="sxs-lookup"><span data-stu-id="83bc0-103">Multiple Handles to a Single Socket</span></span>

<span data-ttu-id="83bc0-104">由於複製的內容是通訊端描述項，而不是基礎通訊端，因此與通訊端相關聯的所有狀態都會保留在所有描述項的通用範圍內。</span><span class="sxs-lookup"><span data-stu-id="83bc0-104">Since what are duplicated are the socket descriptors and not the underlying sockets, all of the states associated with a socket are held in common across all the descriptors.</span></span> <span data-ttu-id="83bc0-105">例如，使用一個描述項執行的 [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) 作業，之後會使用來自任何或所有描述項的 [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) 來顯示。</span><span class="sxs-lookup"><span data-stu-id="83bc0-105">For example a [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) operation performed using one descriptor is subsequently visible using a [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) from any or all descriptors.</span></span>

<span data-ttu-id="83bc0-106">共用通訊端上的通知會受到 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) 和 [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))的一般限制。</span><span class="sxs-lookup"><span data-stu-id="83bc0-106">Notification on shared sockets is subject to the usual constraints of [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="83bc0-107">使用任何共用描述項來發出上述其中一項呼叫，就會取消通訊端先前的任何事件註冊，無論使用哪一個描述項進行註冊。</span><span class="sxs-lookup"><span data-stu-id="83bc0-107">Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration.</span></span> <span data-ttu-id="83bc0-108">例如，可能無法讓進程收到「接收 FD \_ 讀取事件」和「進程 B 接收 fd」 \_ 寫入事件。</span><span class="sxs-lookup"><span data-stu-id="83bc0-108">Thus, for example, it would not be possible to have process A receive FD\_READ events and process B receive FD\_WRITE events.</span></span> <span data-ttu-id="83bc0-109">在需要這類緊密協調的情況下，建議開發人員考慮使用執行緒，而不是個別的進程。</span><span class="sxs-lookup"><span data-stu-id="83bc0-109">For situations when such tight coordination is required, it is suggested that developers consider using threads instead of separate processes.</span></span>

 

 

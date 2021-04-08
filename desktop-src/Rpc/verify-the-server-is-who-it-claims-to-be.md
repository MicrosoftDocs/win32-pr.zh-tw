---
title: 確認伺服器是否為其宣稱的身分
description: 最好是使用相互驗證，進而確認伺服器的身分識別。
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673251"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a><span data-ttu-id="0a831-103">確認伺服器是否為其宣稱的身分</span><span class="sxs-lookup"><span data-stu-id="0a831-103">Verify the Server is Who it Claims to Be</span></span>

<span data-ttu-id="0a831-104">最好是使用相互驗證，進而確認伺服器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a831-104">It is best to use mutual authentication, and thereby verify the identity of the server.</span></span> <span data-ttu-id="0a831-105">失敗的常見錯誤範例，就是具有用戶端呼叫的本機服務的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0a831-105">An example of a common mistake that fails to do this is applications that have a local service into which clients call.</span></span> <span data-ttu-id="0a831-106">在某些設定中，系統管理員可能會決定系統服務並不實用，而且可能會選擇將它停止。</span><span class="sxs-lookup"><span data-stu-id="0a831-106">In some configurations an administrator may decide that the system service is not really useful and may chose to stop it.</span></span> <span data-ttu-id="0a831-107">終端機伺服器電腦上的創意攻擊者可能會啟動在相同端點上接聽的進程，而且當用戶端連線到端點時，允許在伺服器上進行模擬，而不需要對伺服器進行相互驗證，攻擊者可以模擬用戶端並存取用戶端的資料，或代表用戶端進行網路呼叫。</span><span class="sxs-lookup"><span data-stu-id="0a831-107">An inventive attacker on a terminal server computer may launch a process that listens on the same endpoint, and when a client connects to an endpoint, allowing impersonation on the server without mutually authenticating the server, the attacker can impersonate the client and access the client's data, or make network calls on behalf of the client.</span></span> <span data-ttu-id="0a831-108">大部分的系統服務都是以已知的帳戶（例如 LocalSysyem、LocalService 或 NetworkService）來執行，您可以使用相互驗證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="0a831-108">Most system services run under a well-known account, such as LocalSysyem, LocalService, or NetworkService, which can be verified using mutual authentication.</span></span>

 

 





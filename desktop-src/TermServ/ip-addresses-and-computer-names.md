---
title: IP 位址和電腦名稱稱
description: 假設指派給電腦的電腦名稱或 IP 位址 與單一使用者相關聯並不安全，因為多個使用者可以同時登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316195"
---
# <a name="ip-addresses-and-computer-names"></a><span data-ttu-id="aebdd-103">IP 位址和電腦名稱稱</span><span class="sxs-lookup"><span data-stu-id="aebdd-103">IP addresses and computer names</span></span>

<span data-ttu-id="aebdd-104">多個使用者可以同時登入遠端桌面工作階段主機 (RD 工作階段主機) server。</span><span class="sxs-lookup"><span data-stu-id="aebdd-104">Multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="aebdd-105">因此，假設指派給電腦的電腦名稱稱或 IP 位址與單一使用者相關聯，是不安全的。</span><span class="sxs-lookup"><span data-stu-id="aebdd-105">Consequently, it is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user.</span></span> <span data-ttu-id="aebdd-106">這與單一使用者的 Windows 環境不同，因為一次只有一位使用者登入。</span><span class="sxs-lookup"><span data-stu-id="aebdd-106">This differs from a single-user Windows environment, in which only one user is logged on at a time.</span></span>

<span data-ttu-id="aebdd-107">使用電腦名稱稱或 IP 位址進行授權或識別網路上應用程式反復專案的應用程式，在遠端桌面服務環境中將無法正常運作，因為伺服器的電腦名稱稱或 IP 位址可以與許多使用者建立關聯。</span><span class="sxs-lookup"><span data-stu-id="aebdd-107">Applications that use the computer name or IP address for licensing or as a means of identifying an iteration of the application on the network will not work properly in a Remote Desktop Services environment, because the server's computer name or IP address can be associated with many users.</span></span>

<span data-ttu-id="aebdd-108">在遠端桌面服務環境中，每個用戶端終端機或終端機模擬器都有個別的 IP 位址和電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="aebdd-108">In a Remote Desktop Services environment, each client terminal or terminal emulator has a separate IP address and computer name.</span></span> <span data-ttu-id="aebdd-109">若要取得用戶端的 IP 位址和電腦名稱稱，請呼叫 [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) 函式。</span><span class="sxs-lookup"><span data-stu-id="aebdd-109">To retrieve the IP address and computer name of a client, call the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span> <span data-ttu-id="aebdd-110">其他抓取這些網路位址和電腦名稱稱的函式會取出 RD 工作階段主機伺服器的名稱和位址。</span><span class="sxs-lookup"><span data-stu-id="aebdd-110">Other functions that retrieve these network addresses and computer names retrieve the name and address of the RD Session Host server.</span></span> <span data-ttu-id="aebdd-111">例如， [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) 函數會傳回伺服器的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="aebdd-111">For example, the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function returns the computer name of the server.</span></span>

 

 
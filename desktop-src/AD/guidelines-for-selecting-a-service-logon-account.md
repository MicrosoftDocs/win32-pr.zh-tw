---
title: 選取服務登入帳戶的指導方針
description: 以 Win32 為基礎的服務可以在本機使用者帳戶、網域使用者帳戶或 LocalSystem 帳戶的安全性內容中執行。
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- 選取服務登入帳戶 AD 的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020844"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a><span data-ttu-id="d4a43-104">選取服務登入帳戶的指導方針</span><span class="sxs-lookup"><span data-stu-id="d4a43-104">Guidelines for Selecting a Service Logon Account</span></span>

<span data-ttu-id="d4a43-105">以 Win32 為基礎的服務可以在本機使用者帳戶、網域使用者帳戶或 LocalSystem 帳戶的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="d4a43-105">A Win32-based service can run in the security context of a local user account, a domain user account, or the LocalSystem account.</span></span> <span data-ttu-id="d4a43-106">若要決定要使用哪個帳戶，系統管理員應該使用執行服務作業所需的最少許可權集來安裝服務。</span><span class="sxs-lookup"><span data-stu-id="d4a43-106">To decide which account to use, an administrator should install the service with the minimum set of permissions required to perform the service operations.</span></span> <span data-ttu-id="d4a43-107">在一般啟用目錄的服務中，這表示服務安裝程式應該建立服務的網域使用者帳戶，並將服務在執行時間所需的特定存取權和許可權授與該帳戶。</span><span class="sxs-lookup"><span data-stu-id="d4a43-107">In a typical directory-enabled service, this means the service installer should create a domain user account for the service and grant that account the specific access rights and privileges required by the service at run time.</span></span> <span data-ttu-id="d4a43-108">如果服務需要系統管理許可權，或必須做為本機電腦上作業系統的一部分，則服務應該只在 LocalSystem 帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="d4a43-108">A service should only run under the LocalSystem account if the service requires administrative privileges or must act as part of the operating system on the local computer.</span></span>

<span data-ttu-id="d4a43-109">請注意，根據預設，服務安裝程式應該將服務設定為以網域使用者帳戶執行。</span><span class="sxs-lookup"><span data-stu-id="d4a43-109">Be aware that the service installer should, by default, set up the service to run under a domain user account.</span></span> <span data-ttu-id="d4a43-110">若要在 LocalSystem 帳戶下執行服務，服務安裝程式應查詢系統管理員，以取得執行此動作的許可權。</span><span class="sxs-lookup"><span data-stu-id="d4a43-110">To run the service under the LocalSystem account, the service installer should query the administrator for permission to do so.</span></span>

<span data-ttu-id="d4a43-111">如需每種帳戶類型的描述、優點和缺點的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="d4a43-111">For more information about descriptions, advantages, and disadvantages of each account type, see:</span></span>

-   <span data-ttu-id="d4a43-112">[本機使用者帳戶](local-user-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a43-112">[Local User Accounts](local-user-accounts.md).</span></span>
-   <span data-ttu-id="d4a43-113">[網域使用者帳戶](domain-user-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a43-113">[Domain User Accounts](domain-user-accounts.md).</span></span>
-   <span data-ttu-id="d4a43-114">[LocalSystem 帳戶](the-localsystem-account.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a43-114">[The LocalSystem Account](the-localsystem-account.md).</span></span>

 

 





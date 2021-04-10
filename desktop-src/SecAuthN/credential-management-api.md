---
description: 認證管理 API
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: 認證管理 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693500"
---
# <a name="credential-management-api"></a><span data-ttu-id="2f985-103">認證管理 API</span><span class="sxs-lookup"><span data-stu-id="2f985-103">Credential Management API</span></span>

<span data-ttu-id="2f985-104">認證管理函式會組成認證管理員必須執行的一組功能。</span><span class="sxs-lookup"><span data-stu-id="2f985-104">The credential management functions constitute the set of functions that a credential manager must implement.</span></span> <span data-ttu-id="2f985-105">這些警告是：</span><span class="sxs-lookup"><span data-stu-id="2f985-105">These are:</span></span>

-   <span data-ttu-id="2f985-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)，這是 MPR 在使用者登入時所呼叫的事件處理常式函數。</span><span class="sxs-lookup"><span data-stu-id="2f985-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), an event-handler function that the MPR calls when a user logs on.</span></span>
-   <span data-ttu-id="2f985-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)，這是 MPR 在帳戶密碼變更時所呼叫的事件處理常式函數。</span><span class="sxs-lookup"><span data-stu-id="2f985-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), an event-handler function the MPR calls when an account password is changed.</span></span>

<span data-ttu-id="2f985-108">認證管理函式一律會在系統內容中呼叫 (LocalSystem) 而不是使用者內容。</span><span class="sxs-lookup"><span data-stu-id="2f985-108">The credential management functions are always called in the system context (LocalSystem) rather than the user context.</span></span>

<span data-ttu-id="2f985-109">如需有關如何建立和註冊認證管理員應用程式的詳細資訊，請參閱 [執行認證管理員](implementing-a-credential-manager.md) 以及 [註冊網路提供者和認證管理員](registering-network-providers-and-credential-managers.md)。</span><span class="sxs-lookup"><span data-stu-id="2f985-109">For more information about how to create and register a credential manager application, see [Implementing a Credential Manager](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

 




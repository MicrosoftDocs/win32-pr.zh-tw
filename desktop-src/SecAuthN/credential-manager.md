---
description: 認證管理員類似于網路提供者，因為它提供多個提供者路由器呼叫的進入點， (MPR) 。 事實上，有些網路提供者也是認證管理員。
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: 認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20165a5e6145de0a2c042c38923c41d793bd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026976"
---
# <a name="credential-manager"></a><span data-ttu-id="73dda-104">認證管理員</span><span class="sxs-lookup"><span data-stu-id="73dda-104">Credential Manager</span></span>

<span data-ttu-id="73dda-105">認證管理員類似于網路提供者，因為它提供 [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) 呼叫的進入點， (MPR) 。</span><span class="sxs-lookup"><span data-stu-id="73dda-105">A credential manager is similar to a network provider in that it provides entry points that are called by the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="73dda-106">事實上，有些網路提供者也是認證管理員。</span><span class="sxs-lookup"><span data-stu-id="73dda-106">In fact, some network providers are also credential managers.</span></span>

<span data-ttu-id="73dda-107">您是否在與網路提供者函式相同的 DLL 中執行認證管理功能，取決於您的應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="73dda-107">Whether you implement the credential management functions in the same DLL as the network provider functions depends on the requirements of your application.</span></span> <span data-ttu-id="73dda-108">當驗證資訊變更時，認證管理員會收到通知。</span><span class="sxs-lookup"><span data-stu-id="73dda-108">Credential managers receive notifications when authentication information changes.</span></span> <span data-ttu-id="73dda-109">例如，當使用者登入或帳戶密碼變更時，認證管理員會收到通知。</span><span class="sxs-lookup"><span data-stu-id="73dda-109">For example, credential managers are notified when a user logs on or an account password changes.</span></span> <span data-ttu-id="73dda-110">當登入處理常式（例如 [*Winlogon*](/windows/desktop/SecGloss/w-gly)）正在登入或變更帳戶的密碼時，它會呼叫適當的 MPR Windows 網路功能 (WNet) 函式。</span><span class="sxs-lookup"><span data-stu-id="73dda-110">When a logon process, such as [*Winlogon*](/windows/desktop/SecGloss/w-gly), is in the process of logging on or changing the password for an account, it calls the appropriate MPR Windows Networking (WNet) function.</span></span> <span data-ttu-id="73dda-111">然後，MPR 會為每個認證管理員呼叫適當的進入點。</span><span class="sxs-lookup"><span data-stu-id="73dda-111">The MPR then calls the appropriate entry point for each credential manager.</span></span> <span data-ttu-id="73dda-112">這些認證管理函式一律會在系統內容 LocalSystem 中呼叫，而不是在使用者內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="73dda-112">These credential management functions will always be called in the system context, LocalSystem, rather than the user context.</span></span> <span data-ttu-id="73dda-113">如需 WNet 函式的詳細資訊，請參閱 [Windows 網路](/windows/desktop/WNet/windows-networking-wnet-)功能。</span><span class="sxs-lookup"><span data-stu-id="73dda-113">For more information about WNet functions, see [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).</span></span> <span data-ttu-id="73dda-114">如需認證管理員必須執行之介面的詳細資訊，請參閱 [**認證管理 API**](credential-management-api.md)。</span><span class="sxs-lookup"><span data-stu-id="73dda-114">For more information about the interface that credential managers must implement, see [**Credential Management API**](credential-management-api.md).</span></span>

 

 

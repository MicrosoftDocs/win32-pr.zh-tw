---
description: LocalSystem 帳戶是服務控制管理員所使用的預先定義本機帳戶。
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: LocalSystem 帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0132e70044aec7886ce6875239a6bedb502fec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943314"
---
# <a name="localsystem-account"></a><span data-ttu-id="b7d52-103">LocalSystem 帳戶</span><span class="sxs-lookup"><span data-stu-id="b7d52-103">LocalSystem Account</span></span>

<span data-ttu-id="b7d52-104">LocalSystem 帳戶是服務控制管理員所使用的預先定義本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="b7d52-104">The LocalSystem account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="b7d52-105">安全性子系統無法辨識此帳戶，因此您無法在 [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) 函式的呼叫中指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="b7d52-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="b7d52-106">它在本機電腦上具有廣泛的許可權，並且會作為網路上的電腦。</span><span class="sxs-lookup"><span data-stu-id="b7d52-106">It has extensive privileges on the local computer, and acts as the computer on the network.</span></span> <span data-ttu-id="b7d52-107">它的權杖包含 NT 授權單位 \\ 系統和內建系統 \\ 管理員 sid; 這些帳戶可以存取大部分的系統物件。</span><span class="sxs-lookup"><span data-stu-id="b7d52-107">Its token includes the NT AUTHORITY\\SYSTEM and BUILTIN\\Administrators SIDs; these accounts have access to most system objects.</span></span> <span data-ttu-id="b7d52-108">所有地區設定中的帳戶名稱為。 \\LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="b7d52-108">The name of the account in all locales is .\\LocalSystem.</span></span> <span data-ttu-id="b7d52-109">您也可以使用名稱、LocalSystem 或 *ComputerName* \\ localsystem。</span><span class="sxs-lookup"><span data-stu-id="b7d52-109">The name, LocalSystem or *ComputerName*\\LocalSystem can also be used.</span></span> <span data-ttu-id="b7d52-110">此帳戶沒有密碼。</span><span class="sxs-lookup"><span data-stu-id="b7d52-110">This account does not have a password.</span></span> <span data-ttu-id="b7d52-111">如果您在 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 或 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函式的呼叫中指定 LocalSystem 帳戶，則會忽略您提供的任何密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="b7d52-111">If you specify the LocalSystem account in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function, any password information you provide is ignored.</span></span>

<span data-ttu-id="b7d52-112">在 LocalSystem 帳戶內容中執行的服務，會繼承 SCM 的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="b7d52-112">A service that runs in the context of the LocalSystem account inherits the security context of the SCM.</span></span> <span data-ttu-id="b7d52-113">系統會從 **安全性 \_ 本機 \_ 系統 \_ RID** 值建立使用者 SID。</span><span class="sxs-lookup"><span data-stu-id="b7d52-113">The user SID is created from the **SECURITY\_LOCAL\_SYSTEM\_RID** value.</span></span> <span data-ttu-id="b7d52-114">此帳戶未與任何已登入的使用者帳戶相關聯。</span><span class="sxs-lookup"><span data-stu-id="b7d52-114">The account is not associated with any logged-on user account.</span></span> <span data-ttu-id="b7d52-115">這有下列幾個含意：</span><span class="sxs-lookup"><span data-stu-id="b7d52-115">This has several implications:</span></span>

-   <span data-ttu-id="b7d52-116">登錄機碼 **HKEY \_ 目前 \_ 使用者** 與預設使用者相關聯，而不是目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="b7d52-116">The registry key **HKEY\_CURRENT\_USER** is associated with the default user, not the current user.</span></span> <span data-ttu-id="b7d52-117">若要存取其他使用者的設定檔，請模擬使用者，然後存取 **HKEY \_ 目前的 \_ 使用者**。</span><span class="sxs-lookup"><span data-stu-id="b7d52-117">To access another user's profile, impersonate the user, then access **HKEY\_CURRENT\_USER**.</span></span>
-   <span data-ttu-id="b7d52-118">服務可以開啟登錄機碼 **HKEY \_ 本機 \_ 電腦 \\ 安全性**。</span><span class="sxs-lookup"><span data-stu-id="b7d52-118">The service can open the registry key **HKEY\_LOCAL\_MACHINE\\SECURITY**.</span></span>
-   <span data-ttu-id="b7d52-119">服務會向遠端伺服器顯示電腦的認證。</span><span class="sxs-lookup"><span data-stu-id="b7d52-119">The service presents the computer's credentials to remote servers.</span></span>
-   <span data-ttu-id="b7d52-120">如果服務開啟命令視窗並執行批次檔，則使用者可以按 CTRL + C 來終止批次檔，並取得具有 LocalSystem 許可權的命令視窗的存取權。</span><span class="sxs-lookup"><span data-stu-id="b7d52-120">If the service opens a command window and runs a batch file, the user could hit CTRL+C to terminate the batch file and gain access to a command window with LocalSystem permissions.</span></span>

<span data-ttu-id="b7d52-121">LocalSystem 帳戶具有下列許可權：</span><span class="sxs-lookup"><span data-stu-id="b7d52-121">The LocalSystem account has the following privileges:</span></span>

-   <span data-ttu-id="b7d52-122">**SE \_ASSIGNPRIMARYTOKEN \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="b7d52-122">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-123">**SE \_ (啟用審核 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-123">**SE\_AUDIT\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-124">**SE \_ (\_** 停用的備份名稱) </span><span class="sxs-lookup"><span data-stu-id="b7d52-124">**SE\_BACKUP\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-125">**SE \_ (啟用變更 \_ 通知 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-125">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-126">**SE \_ (啟用 [建立 \_ 全域 \_ 名稱** ]) </span><span class="sxs-lookup"><span data-stu-id="b7d52-126">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-127">**SE \_ (啟用) 建立 \_ 分頁檔 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="b7d52-127">**SE\_CREATE\_PAGEFILE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-128">**SE \_ (啟用) 建立 \_ 永久 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="b7d52-128">**SE\_CREATE\_PERMANENT\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-129">**SE \_ (停用) 建立 \_ 權杖 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="b7d52-129">**SE\_CREATE\_TOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-130">**SE \_ (啟用的 DEBUG \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-130">**SE\_DEBUG\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-131">**SE \_ (\_** 啟用模擬名稱) </span><span class="sxs-lookup"><span data-stu-id="b7d52-131">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-132">**SE \_啟用 (的 INC. \_ 基礎 \_ 優先順序 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-132">**SE\_INC\_BASE\_PRIORITY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-133">**SE \_ (停用) 增加 \_ 配額 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="b7d52-133">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-134">**SE \_ (停用載入 \_ 驅動程式 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-134">**SE\_LOAD\_DRIVER\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-135">**SE \_ (啟用鎖定 \_ 記憶體 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-135">**SE\_LOCK\_MEMORY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-136">**SE \_ (停用) 管理 \_ 磁片區 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="b7d52-136">**SE\_MANAGE\_VOLUME\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-137">**SE \_獲 \_ 單一 \_ 進程 \_ 名稱** (已啟用) </span><span class="sxs-lookup"><span data-stu-id="b7d52-137">**SE\_PROF\_SINGLE\_PROCESS\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-138">**SE \_ (\_** 停用的還原名稱) </span><span class="sxs-lookup"><span data-stu-id="b7d52-138">**SE\_RESTORE\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-139">**SE \_ (\_** 停用的安全性名稱) </span><span class="sxs-lookup"><span data-stu-id="b7d52-139">**SE\_SECURITY\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-140">**SE \_停用的關機 \_ 名稱** () </span><span class="sxs-lookup"><span data-stu-id="b7d52-140">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-141">**SE \_ (停用系統 \_ 環境 \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-141">**SE\_SYSTEM\_ENVIRONMENT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-142">**SE \_SYSTEMTIME \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="b7d52-142">**SE\_SYSTEMTIME\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-143">**SE \_取得 \_ 擁有權 \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="b7d52-143">**SE\_TAKE\_OWNERSHIP\_NAME** (disabled)</span></span>
-   <span data-ttu-id="b7d52-144">**SE \_ (啟用 TCB \_ 名稱**) </span><span class="sxs-lookup"><span data-stu-id="b7d52-144">**SE\_TCB\_NAME** (enabled)</span></span>
-   <span data-ttu-id="b7d52-145">**SE \_停用移除 \_ 名稱** (停用) </span><span class="sxs-lookup"><span data-stu-id="b7d52-145">**SE\_UNDOCK\_NAME** (disabled)</span></span>

<span data-ttu-id="b7d52-146">大部分的服務都不需要這類高許可權層級。</span><span class="sxs-lookup"><span data-stu-id="b7d52-146">Most services do not need such a high privilege level.</span></span> <span data-ttu-id="b7d52-147">如果您的服務不需要這些許可權，而且不是互動式服務，請考慮使用 [LocalService 帳戶](localservice-account.md) 或 [NetworkService 帳戶](networkservice-account.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d52-147">If your service does not need these privileges, and it is not an interactive service, consider using the [LocalService account](localservice-account.md) or the [NetworkService account](networkservice-account.md).</span></span> <span data-ttu-id="b7d52-148">如需詳細資訊，請參閱 [服務安全性和存取權限](service-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d52-148">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 

---
description: 每個服務都會在使用者帳戶的安全性內容中執行。
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: 服務使用者帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c72f332b8eddbc5b5929718b6688f75e226e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852063"
---
# <a name="service-user-accounts"></a><span data-ttu-id="639db-103">服務使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="639db-103">Service User Accounts</span></span>

<span data-ttu-id="639db-104">每個服務都會在使用者帳戶的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="639db-104">Each service executes in the security context of a user account.</span></span> <span data-ttu-id="639db-105">安裝服務時， [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式會指定帳戶的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="639db-105">The user name and password of an account are specified by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function at the time the service is installed.</span></span> <span data-ttu-id="639db-106">您可以使用 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函數來變更使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="639db-106">The user name and password can be changed by using the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span> <span data-ttu-id="639db-107">您可以使用 [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) 函式來取得使用者名稱 (但不是與服務物件相關聯的密碼) 。</span><span class="sxs-lookup"><span data-stu-id="639db-107">You can use the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) function to get the user name (but not the password) associated with a service object.</span></span> <span data-ttu-id="639db-108">服務控制管理員 (SCM) 會自動載入使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="639db-108">The service control manager (SCM) automatically loads the user profile.</span></span>

<span data-ttu-id="639db-109">啟動服務時，SCM 會登入與服務相關聯的帳戶。</span><span class="sxs-lookup"><span data-stu-id="639db-109">When starting a service, the SCM logs on to the account associated with the service.</span></span> <span data-ttu-id="639db-110">如果登入成功，系統會產生存取權杖，並將其附加至新的服務進程。</span><span class="sxs-lookup"><span data-stu-id="639db-110">If the log on is successful, the system produces an access token and attaches it to the new service process.</span></span> <span data-ttu-id="639db-111">此權杖會在與安全物件的所有後續互動中識別服務程式， (具有與其相關聯之安全描述項的物件) 。</span><span class="sxs-lookup"><span data-stu-id="639db-111">This token identifies the service process in all subsequent interactions with securable objects (objects that have a security descriptor associated with them).</span></span> <span data-ttu-id="639db-112">例如，如果服務嘗試開啟管道的控制碼，則系統會先將服務的存取權杖與管線的安全描述項進行比較，再授與存取權。</span><span class="sxs-lookup"><span data-stu-id="639db-112">For example, if the service tries to open a handle to a pipe, the system compares the service's access token to the pipe's security descriptor before granting access.</span></span>

<span data-ttu-id="639db-113">SCM 不會維護服務使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="639db-113">The SCM does not maintain the passwords of service user accounts.</span></span> <span data-ttu-id="639db-114">如果密碼已過期，登入將會失敗，且服務無法啟動。</span><span class="sxs-lookup"><span data-stu-id="639db-114">If a password is expired, the logon fails and the service fails to start.</span></span> <span data-ttu-id="639db-115">將帳戶指派給服務的系統管理員可以建立密碼永遠不會過期的帳戶。</span><span class="sxs-lookup"><span data-stu-id="639db-115">The system administrator who assigns accounts to services can create accounts with passwords that never expire.</span></span> <span data-ttu-id="639db-116">系統管理員也可以使用 [服務設定程式](service-configuration-programs.md) 定期變更密碼，來管理具有過期密碼的帳戶。</span><span class="sxs-lookup"><span data-stu-id="639db-116">The administrator can also manage accounts with passwords that expire by using a [service configuration program](service-configuration-programs.md) to periodically change the passwords.</span></span>

<span data-ttu-id="639db-117">如果服務需要在共用其資訊之前辨識另一項服務，則第二個服務可以使用與第一個服務相同的帳戶，也可以在屬於第一個服務所能辨識之別名的帳戶中執行。</span><span class="sxs-lookup"><span data-stu-id="639db-117">If a service needs to recognize another service before sharing its information, the second service can either use the same account as the first service, or it can run in an account belonging to an alias that is recognized by the first service.</span></span> <span data-ttu-id="639db-118">需要在網路上以分散方式執行的服務應該在全網域帳戶中執行。</span><span class="sxs-lookup"><span data-stu-id="639db-118">Services that need to run in a distributed manner across the network should run in domain-wide accounts.</span></span>

<span data-ttu-id="639db-119">您可以指定下列其中一個特殊帳戶，而不是指定服務的使用者帳戶：</span><span class="sxs-lookup"><span data-stu-id="639db-119">You can specify one of the following special accounts instead of specifying a user account for the service:</span></span>

-   [<span data-ttu-id="639db-120">LocalService</span><span class="sxs-lookup"><span data-stu-id="639db-120">LocalService</span></span>](localservice-account.md)
-   [<span data-ttu-id="639db-121">NetworkService</span><span class="sxs-lookup"><span data-stu-id="639db-121">NetworkService</span></span>](networkservice-account.md)
-   [<span data-ttu-id="639db-122">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="639db-122">LocalSystem</span></span>](localsystem-account.md)

 

 




---
title: 登入帳戶維護工作
description: 本主題說明與登入帳戶維護工作相關的問題。
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- 登入帳戶維護工作 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0f11f69d9a974fd666871833029eda0e059329
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104374925"
---
# <a name="logon-account-maintenance-tasks"></a><span data-ttu-id="b15b9-104">登入帳戶維護工作</span><span class="sxs-lookup"><span data-stu-id="b15b9-104">Logon Account Maintenance Tasks</span></span>

<span data-ttu-id="b15b9-105">本主題說明與登入帳戶維護工作相關的問題。</span><span class="sxs-lookup"><span data-stu-id="b15b9-105">This topic describes issues that pertain to logon account maintenance tasks.</span></span>

<span data-ttu-id="b15b9-106">有兩個主要問題涉及登入帳戶維護工作：</span><span class="sxs-lookup"><span data-stu-id="b15b9-106">There are two primary issues that concern logon account maintenance tasks:</span></span>

-   <span data-ttu-id="b15b9-107">更新在使用者帳戶下執行之服務實例的帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="b15b9-107">Updating the account password for a service instance that runs under a user account.</span></span> <span data-ttu-id="b15b9-108">如需詳細資訊，請參閱 [變更服務之使用者帳戶的密碼](changing-the-password-on-a-serviceampaposs-user-account.md)。</span><span class="sxs-lookup"><span data-stu-id="b15b9-108">For more information, see [Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md).</span></span>
-   <span data-ttu-id="b15b9-109">處理服務實例之登入帳戶的變更。</span><span class="sxs-lookup"><span data-stu-id="b15b9-109">Handling changes to the logon account of a service instance.</span></span>

<span data-ttu-id="b15b9-110">後者是很罕見的情況，但可能發生。</span><span class="sxs-lookup"><span data-stu-id="b15b9-110">The latter is a rare case, but can happen.</span></span> <span data-ttu-id="b15b9-111">系統提供 [電腦管理] 系統管理工具，可讓您變更服務登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="b15b9-111">The system provides the Computer Management administrative tool that enables change to a service logon account.</span></span> <span data-ttu-id="b15b9-112">此外，其他應用程式也可以使用 [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) 函數，為已安裝的服務指定新的登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="b15b9-112">In addition, other applications can use the [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) function to specify a new logon account for an installed service.</span></span> <span data-ttu-id="b15b9-113">依預設，需要本機系統管理員許可權才能變更服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="b15b9-113">By default, local administrator privileges are required to change a service account.</span></span> <span data-ttu-id="b15b9-114">如果發生這種情況，可能會以兩種方式影響您的服務：</span><span class="sxs-lookup"><span data-stu-id="b15b9-114">If this did happen, it could affect your service in two ways:</span></span>

-   <span data-ttu-id="b15b9-115">如果您已)  (Spn 註冊服務主體名稱，這些名稱會在錯誤的帳戶中註冊。</span><span class="sxs-lookup"><span data-stu-id="b15b9-115">If you have registered service principal names (SPNs), they will be registered on the wrong account.</span></span>
-   <span data-ttu-id="b15b9-116">如果您設定 Ace 來授與服務的存取權，他們現在會將存取權授與錯誤的帳戶。</span><span class="sxs-lookup"><span data-stu-id="b15b9-116">If you set ACEs to grant access to the service, they would now grant access to the wrong account.</span></span>

<span data-ttu-id="b15b9-117">其中一個方法是讓服務安裝程式為主電腦上登錄中的每個服務實例儲存註冊的 Spn。</span><span class="sxs-lookup"><span data-stu-id="b15b9-117">One approach is to have the service installer store the registered SPNs for each service instance in the registry on the host computer.</span></span> <span data-ttu-id="b15b9-118">您可以在 \_ \_ 用來儲存服務 SCP 之系結字串的 HKEY 本機電腦下使用相同的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="b15b9-118">You could use the same registry key under HKEY\_LOCAL\_MACHINE that you used to store the binding string for the service SCP.</span></span> <span data-ttu-id="b15b9-119">當服務啟動時，它會呼叫 [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) 函式來判斷其登入帳戶，然後查詢 Active Directory 伺服器，以判斷 spn 是否已在該帳戶的目錄物件上註冊。</span><span class="sxs-lookup"><span data-stu-id="b15b9-119">When the service starts, it calls the [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) function to determine its logon account and then queries the Active Directory server to determine whether the SPNs are registered on the directory object for that account.</span></span> <span data-ttu-id="b15b9-120">如果 Spn 未註冊，或已在錯誤的帳戶中註冊，則服務會拒絕啟動，並顯示一則訊息，指出網域系統管理員必須執行服務的設定程式來更新登入帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="b15b9-120">If the SPNs are not registered, or are registered on the wrong account, the service refuses to start and displays a message saying that a domain administrator must run the service's configuration program to update the logon account settings.</span></span> <span data-ttu-id="b15b9-121">請注意，這項重新設定必須由系統管理員完成，因為服務帳戶不應該有存取權來更新自己的 SPN。</span><span class="sxs-lookup"><span data-stu-id="b15b9-121">Be aware that this reconfiguration must be completed by an administrator because the service account should not have access to update its own SPN.</span></span> <span data-ttu-id="b15b9-122">也請注意，必須從舊帳戶移除 Spn，否則 Spn 將無法用於驗證，因為它們在樹系中並不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b15b9-122">Also be aware that SPNs must be removed from the old account, otherwise the SPNs will be useless for authentication because they are not unique in the forest.</span></span>

 

 
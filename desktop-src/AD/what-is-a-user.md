---
title: 什麼是使用者
description: 系統會建立使用者帳戶，並將其儲存為 Active Directory Domain Services 中的物件。
ms.assetid: da13d21a-1d8b-4d03-8880-7146e6fc4ba9
ms.tgt_platform: multiple
keywords:
- 什麼是使用者 Active Directory
- 使用者 Active Directory，使用者是什麼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c59b2ea46474860268f327bcd03d2ba67ecea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671203"
---
# <a name="what-is-a-user"></a><span data-ttu-id="a0296-105">什麼是使用者？</span><span class="sxs-lookup"><span data-stu-id="a0296-105">What is a User?</span></span>

<span data-ttu-id="a0296-106">系統會建立使用者帳戶，並將其儲存為 Active Directory Domain Services 中的物件。</span><span class="sxs-lookup"><span data-stu-id="a0296-106">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="a0296-107">使用者帳戶可以由人力使用者或程式（例如系統服務用來登入電腦）使用。</span><span class="sxs-lookup"><span data-stu-id="a0296-107">User accounts can be used by human users or programs such as system services use to log on to a computer.</span></span> <span data-ttu-id="a0296-108">當使用者登入時，系統會將使用者的密碼與使用者在 Active Directory 伺服器的使用者物件中所儲存的資料進行比較，以驗證該使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="a0296-108">When a user logs on, the system verifies the user's password by comparing it with data stored in the user's user object in the Active Directory server.</span></span> <span data-ttu-id="a0296-109">如果密碼經過驗證，也就是顯示的密碼符合使用者物件中儲存的密碼，則系統會產生存取權杖。</span><span class="sxs-lookup"><span data-stu-id="a0296-109">If the password is authenticated, that is, the password presented matches the password stored in the user object, the system produces an access token.</span></span> <span data-ttu-id="a0296-110">存取權杖是描述進程或執行緒之安全性內容的物件。</span><span class="sxs-lookup"><span data-stu-id="a0296-110">An access token is an object that describes the security context of a process or thread.</span></span> <span data-ttu-id="a0296-111">權杖中的資料包含與進程或執行緒相關聯之使用者帳戶的安全性識別和群組成員資格。</span><span class="sxs-lookup"><span data-stu-id="a0296-111">The data in a token includes the security identity and group memberships of the user account associated with the process or thread.</span></span> <span data-ttu-id="a0296-112">代表此使用者執行的每個處理常式都有此存取權杖的複本。</span><span class="sxs-lookup"><span data-stu-id="a0296-112">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="a0296-113">存取 Windows 網域中資源的每個使用者或應用程式都必須在 Active Directory 伺服器中有一個帳戶。</span><span class="sxs-lookup"><span data-stu-id="a0296-113">Each user or application that accesses resources in a Windows domain must have an account in the Active Directory server.</span></span> <span data-ttu-id="a0296-114">Windows 使用此使用者帳戶來確認使用者或應用程式有權使用資源。</span><span class="sxs-lookup"><span data-stu-id="a0296-114">Windows uses this user account to verify that the user or application has permission to use a resource.</span></span>

<span data-ttu-id="a0296-115">使用者帳戶可以用來：</span><span class="sxs-lookup"><span data-stu-id="a0296-115">A user account can be used to:</span></span>

-   <span data-ttu-id="a0296-116">讓人類使用者登入電腦，並根據該使用者帳戶的身分識別來存取資源。</span><span class="sxs-lookup"><span data-stu-id="a0296-116">Enable human users to log on to a computer and to access resources based on that user account's identity.</span></span>
-   <span data-ttu-id="a0296-117">讓程式和服務在特定的安全性內容下執行。</span><span class="sxs-lookup"><span data-stu-id="a0296-117">Enable programs and services to run under a specific security context.</span></span>
-   <span data-ttu-id="a0296-118">管理使用者對共用資源的存取，例如物件和其屬性、網路共用、檔案、目錄、印表機佇列等等。</span><span class="sxs-lookup"><span data-stu-id="a0296-118">Manage user access to shared resources such as objects and their properties, network shares, files, directories, printer queues, and so on.</span></span>

<span data-ttu-id="a0296-119">群組可以包含成員，這些成員是對使用者和其他群組的參考。</span><span class="sxs-lookup"><span data-stu-id="a0296-119">Groups can contain members, which are references to users and other groups.</span></span> <span data-ttu-id="a0296-120">群組也可以用來控制對共用資源的存取。</span><span class="sxs-lookup"><span data-stu-id="a0296-120">Groups can also be used to control access to shared resources.</span></span> <span data-ttu-id="a0296-121">指派資源的許可權（例如檔案共用、印表機等）時，系統管理員應該將這些許可權指派給群組，而不是個別的使用者。</span><span class="sxs-lookup"><span data-stu-id="a0296-121">When assigning permissions for resources, for example file shares, printers, and so on, administrators should assign those permissions to a group rather than to the individual users.</span></span> <span data-ttu-id="a0296-122">系統會將許可權指派給群組，而不是多次指派給每個個別使用者。</span><span class="sxs-lookup"><span data-stu-id="a0296-122">The permissions are assigned once to the group, instead of several times to each individual user.</span></span> <span data-ttu-id="a0296-123">這有助於簡化網路的維護和管理。</span><span class="sxs-lookup"><span data-stu-id="a0296-123">This helps simplify the maintenance and administration of a network.</span></span>

## <a name="users-compared-to-contacts"></a><span data-ttu-id="a0296-124">使用者與連絡人的比較</span><span class="sxs-lookup"><span data-stu-id="a0296-124">Users compared to Contacts</span></span>

<span data-ttu-id="a0296-125">使用者和連絡人都可以用來代表人類的使用者。</span><span class="sxs-lookup"><span data-stu-id="a0296-125">Both users and contacts can be used to represent human users.</span></span> <span data-ttu-id="a0296-126">但是，使用者是安全性主體;連絡人不是。</span><span class="sxs-lookup"><span data-stu-id="a0296-126">However, a user is a security principal; a contact is not.</span></span>

<span data-ttu-id="a0296-127">使用者可以用來讓人類使用者登入並存取共用資源。</span><span class="sxs-lookup"><span data-stu-id="a0296-127">A user can be used to enable a human user to log on and access shared resources.</span></span>

<span data-ttu-id="a0296-128">連絡人僅用於通訊群組清單和電子郵件用途。</span><span class="sxs-lookup"><span data-stu-id="a0296-128">A contact is used only for distribution list and email purposes.</span></span> <span data-ttu-id="a0296-129">不過，連絡人可以包含儲存在使用者物件中的大部分資料，例如位址、電話號碼等等，因為使用者和連絡人都衍生自 person **classSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="a0296-129">However, a contact can contain most of the data stored in a user object such as address, phone numbers, and so on because both user and contact are derived from the person **classSchema** object.</span></span> <span data-ttu-id="a0296-130">連絡人沒有安全性內容;因此，連絡人無法用來控制對共用資源的存取權，也無法用來登入電腦。</span><span class="sxs-lookup"><span data-stu-id="a0296-130">A contact has no security context; therefore, a contact cannot be used to control access to shared resources and cannot be used to log on to a computer.</span></span>

## <a name="users-compared-to-computers"></a><span data-ttu-id="a0296-131">相較于電腦的使用者</span><span class="sxs-lookup"><span data-stu-id="a0296-131">Users compared to Computers</span></span>

<span data-ttu-id="a0296-132">Computer 物件類別繼承自 user 物件類別。</span><span class="sxs-lookup"><span data-stu-id="a0296-132">The computer object class inherits from the user object class.</span></span> <span data-ttu-id="a0296-133">代表電腦的電腦物件;但是，電腦和電腦的本機服務通常需要存取網路和共用資源。</span><span class="sxs-lookup"><span data-stu-id="a0296-133">A computer object represents a computer; however, the computer and the computer's local services often require access to the network and shared resources.</span></span> <span data-ttu-id="a0296-134">當電腦存取共用資源，而不是登入電腦的使用者時，它需要存取權杖，就像使用者登入的使用者一樣。</span><span class="sxs-lookup"><span data-stu-id="a0296-134">When the computer accesses shared resources, not the user logged on to the computer, it needs an access token just as a human user logged on as a user does.</span></span> <span data-ttu-id="a0296-135">當電腦存取網路時，它會使用存取權杖，其中包含電腦的電腦帳戶的安全識別碼，以及該帳戶所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="a0296-135">When a computer accesses the network, it uses an access token that contains the security identifier for the computer's computer account and the groups that account is a member.</span></span>

<span data-ttu-id="a0296-136">服務可以在 LocalSystem 或特定服務帳戶的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="a0296-136">A service can run in the context of LocalSystem or a specific service account.</span></span> <span data-ttu-id="a0296-137">在執行 Windows 2000 的電腦上，于 LocalSystem 帳戶內容中執行的服務會使用電腦的認證。</span><span class="sxs-lookup"><span data-stu-id="a0296-137">On computers running Windows 2000, a service that runs in the context of the LocalSystem account uses the credentials of the computer.</span></span>

 

 





---
title: 服務登入帳戶
description: 服務就像任何程式一樣，有一個主要的安全性身分識別，可決定授與本機和網路資源的存取權和許可權。
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory，使用服務登入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839267"
---
# <a name="service-logon-accounts"></a><span data-ttu-id="d8d18-104">服務登入帳戶</span><span class="sxs-lookup"><span data-stu-id="d8d18-104">Service Logon Accounts</span></span>

<span data-ttu-id="d8d18-105">服務就像任何程式一樣，有一個主要的安全性身分識別，可決定授與本機和網路資源的存取權和許可權。</span><span class="sxs-lookup"><span data-stu-id="d8d18-105">A service, like any process, has a primary security identity that determines the granted access rights and privileges for local and network resources.</span></span> <span data-ttu-id="d8d18-106">此安全性身分識別或安全性內容，也會決定服務對於本機和網路資源的損害有何潛力。</span><span class="sxs-lookup"><span data-stu-id="d8d18-106">This security identity, or security context, also determines the potential the service has for damaging local and network resources.</span></span>

<span data-ttu-id="d8d18-107">Microsoft Win32 服務的安全性內容是由用來啟動服務的登入帳戶所決定。</span><span class="sxs-lookup"><span data-stu-id="d8d18-107">The security context for a Microsoft Win32 service is determined by the logon account that is used to start the service.</span></span> <span data-ttu-id="d8d18-108">本節討論與 Win32 服務所使用的服務登入帳戶相關的程式設計問題和最佳作法，並著重在啟用目錄的服務。</span><span class="sxs-lookup"><span data-stu-id="d8d18-108">This section discusses programming issues and best practices relating to the service logon account used by Win32 services, with a focus on directory-enabled services.</span></span> <span data-ttu-id="d8d18-109">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="d8d18-109">This section includes the following topics:</span></span>

-   <span data-ttu-id="d8d18-110">[關於服務登入帳戶](about-service-logon-accounts.md)-Win32 服務的服務登入帳戶和安全性內容程式設計問題的總覽。</span><span class="sxs-lookup"><span data-stu-id="d8d18-110">[About Service Logon Accounts](about-service-logon-accounts.md)—An overview of service logon accounts and security context programming issues for a Win32 service.</span></span>
-   <span data-ttu-id="d8d18-111">[針對 Win32 服務選取服務登入帳戶的指導方針](guidelines-for-selecting-a-service-logon-account.md) 。</span><span class="sxs-lookup"><span data-stu-id="d8d18-111">[Guidelines for Selecting a Service Logon Account](guidelines-for-selecting-a-service-logon-account.md) for a Win32 service.</span></span>
-   <span data-ttu-id="d8d18-112">[設定服務的使用者帳戶](setting-up-a-serviceampaposs-user-account.md)。</span><span class="sxs-lookup"><span data-stu-id="d8d18-112">[Setting up a Service's User Account](setting-up-a-serviceampaposs-user-account.md).</span></span>
-   <span data-ttu-id="d8d18-113">[在主機電腦上安裝服務](installing-a-service-on-a-host-computer.md) ，並指定服務登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="d8d18-113">[Installing a Service on a Host Computer](installing-a-service-on-a-host-computer.md) and specifying the service logon account.</span></span>
-   <span data-ttu-id="d8d18-114">將[主機電腦上的 [以服務方式登](granting-logon-as-service-right-on-the-host-computer.md)入] 許可權授與給服務的使用者帳戶，這是主機電腦上的 [以服務方式登入] 許可權。</span><span class="sxs-lookup"><span data-stu-id="d8d18-114">[Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md)—Granting the service's user account the logon as a service right on the host computer.</span></span>
-   <span data-ttu-id="d8d18-115">[測試是否正在網域控制站上執行](testing-whether-running-on-a-domain-controller.md)-在安裝時偵測是否正在安裝網域控制站上的服務實例。</span><span class="sxs-lookup"><span data-stu-id="d8d18-115">[Testing Whether Running on a Domain Controller](testing-whether-running-on-a-domain-controller.md)—Detecting at installation time whether the service instance is being installed on a domain controller.</span></span>
-   <span data-ttu-id="d8d18-116">將[存取權限授與服務登入帳戶](granting-access-rights-to-the-service-logon-account.md)—設定和維護 ace 和群組成員資格，以確保系統會將所需的本機和網路資源存取權授與執行中的服務。</span><span class="sxs-lookup"><span data-stu-id="d8d18-116">[Granting Access Rights to the Service Logon Account](granting-access-rights-to-the-service-logon-account.md)—Setting and maintaining ACEs and group memberships to ensure that the system will grant the running service access to the necessary local and network resources.</span></span>
-   <span data-ttu-id="d8d18-117">[變更服務使用者帳戶的密碼](changing-the-password-on-a-serviceampaposs-user-account.md)（在服務的使用者帳戶上變更密碼），同時在安裝服務的每部主機伺服器上更新向服務控制管理員註冊的密碼。</span><span class="sxs-lookup"><span data-stu-id="d8d18-117">[Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md)—Changing the password on a service's user account, and at the same time updating the password registered with the service control manager on each host server on which the service is installed.</span></span>
-   <span data-ttu-id="d8d18-118">[使用 Kerberos 進行相互驗證](mutual-authentication-using-kerberos.md)，在與服務的每個實例的登入帳戶相關聯的目錄物件上維護服務主體名稱 (SPN) 註冊。</span><span class="sxs-lookup"><span data-stu-id="d8d18-118">[Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md)—Maintaining service principal name (SPN) registration on the directory object associated with the logon account of each instance of your service.</span></span> <span data-ttu-id="d8d18-119">Spn 可讓用戶端使用 Kerberos 相互驗證來驗證服務。</span><span class="sxs-lookup"><span data-stu-id="d8d18-119">SPNs enable clients to authenticate a service using Kerberos mutual authentication.</span></span>
-   <span data-ttu-id="d8d18-120">[轉換網域帳戶名稱格式](converting-domain-account-name-formats.md)—例如，將辨別名稱轉換成 \*網域使用者 \*\*\*\\*\*\*\* 名稱格式，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="d8d18-120">[Converting Domain Account Name Formats](converting-domain-account-name-formats.md)—For example, converting a distinguished name to *Domain ***\\*** UserName* format, and vice versa.</span></span>

 

 





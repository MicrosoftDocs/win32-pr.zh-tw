---
title: 設定服務的使用者帳戶
description: 您的服務安裝程式可以針對服務實例建議預設登入帳戶，並允許系統管理員選取預設帳戶或指定不同的帳戶。
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- 設定服務的使用者帳戶 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705fa16d8d2cce137755f4a5086716aaaef8046a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681634"
---
# <a name="setting-up-a-services-user-account"></a><span data-ttu-id="a9111-104">設定服務的使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="a9111-104">Setting up a Service's User Account</span></span>

<span data-ttu-id="a9111-105">您的服務安裝程式可以針對服務實例建議預設登入帳戶，並允許系統管理員選取預設帳戶或指定不同的帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9111-105">Your service installer can suggest a default logon account for a service instance and allow the administrator to select the default account or specify a different one.</span></span> <span data-ttu-id="a9111-106">如果系統管理員選取使用者帳戶，而不是 LocalSystem 帳戶，則在呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 函式之前，帳戶必須存在，才能在主機伺服器上安裝服務的實例。</span><span class="sxs-lookup"><span data-stu-id="a9111-106">If the administrator selects a user account, rather than the LocalSystem account, the account must exist before you call the [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) function to install an instance of the service on a host server.</span></span> <span data-ttu-id="a9111-107">如需可在 Active Directory Domain Services 中用來建立新網域使用者物件的詳細資訊和程式碼範例，請參閱 [建立使用者](creating-a-user.md)。</span><span class="sxs-lookup"><span data-stu-id="a9111-107">For more information and a code example that can be used to create a new domain user object in Active Directory Domain Services, see [Creating a User](creating-a-user.md).</span></span>

<span data-ttu-id="a9111-108">在理想情況下，服務的每個實例（不論是主機型或可複寫服務）都應該有自己的網域使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9111-108">Ideally, each instance of a service, whether a host-based or replicable service, should have its own domain user account.</span></span> <span data-ttu-id="a9111-109">針對每個服務實例使用不同的帳戶，比讓多個實例共用相同的帳戶更安全。</span><span class="sxs-lookup"><span data-stu-id="a9111-109">Using separate accounts for each service instance is more secure than having multiple instances share the same account.</span></span> <span data-ttu-id="a9111-110">此外，使用不同的帳戶，可以讓您審核每個服務實例的活動。</span><span class="sxs-lookup"><span data-stu-id="a9111-110">Also, using separate accounts makes it possible to audit the activities of each service instance.</span></span>

<span data-ttu-id="a9111-111">當您的安裝程式建議使用預設登入帳戶時，應該為新的服務實例指定要建立之新帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9111-111">When your installer suggests a default logon account, it should specify the name of a new account to be created for the new service instance.</span></span> <span data-ttu-id="a9111-112">帳戶名稱可能是由用來撰寫服務主體名稱的相同元素所組成，例如服務類別、主機電腦和服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a9111-112">The account name could be composed from the same elements used to compose a service principal name, such as the service class, host computer, and service name.</span></span> <span data-ttu-id="a9111-113">如需詳細資訊，請參閱[服務主體名稱](service-principal-names.md)。</span><span class="sxs-lookup"><span data-stu-id="a9111-113">For more information, see [Service Principal Names](service-principal-names.md).</span></span> <span data-ttu-id="a9111-114">一般而言，您會在主機電腦網域的 [使用者] 容器中建立帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9111-114">Typically, you create the account in the Users container on the domain of the host computer.</span></span>

<span data-ttu-id="a9111-115">您必須為每個帳戶產生密碼。</span><span class="sxs-lookup"><span data-stu-id="a9111-115">You must generate a password for each account.</span></span> <span data-ttu-id="a9111-116">如需有關如何撰寫可自動化更新服務帳戶密碼之工作的詳細資訊，請參閱 [變更服務之使用者帳戶的密碼](changing-the-password-on-a-serviceampaposs-user-account.md)。</span><span class="sxs-lookup"><span data-stu-id="a9111-116">For more information about how to write a tool that automates the task of updating service account passwords, see [Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md).</span></span>

 

 
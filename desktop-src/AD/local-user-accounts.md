---
title: 使用本機使用者帳戶做為服務登入帳戶
description: 本機使用者帳戶 (名稱格式 \ 0034;。 \\UserName \ 0034; ) 只存在於主機電腦的 SAM 資料庫中;它沒有 Active Directory Domain Services 中的使用者物件。
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092209"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a><span data-ttu-id="ae7c1-103">使用本機使用者帳戶做為服務登入帳戶</span><span class="sxs-lookup"><span data-stu-id="ae7c1-103">Using a Local User Account as a Service Logon Account</span></span>

<span data-ttu-id="ae7c1-104">本機使用者帳戶 (名稱格式： "。 \\*UserName*") 只存在於主機電腦的 SAM 資料庫中;它沒有 Active Directory Domain Services 中的使用者物件。</span><span class="sxs-lookup"><span data-stu-id="ae7c1-104">A local user account (name format: ".\\*UserName*") exists only in the SAM database of the host computer; it does not have a user object in Active Directory Domain Services.</span></span> <span data-ttu-id="ae7c1-105">這表示網域無法驗證本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="ae7c1-105">This means that a local account cannot be authenticated by the domain.</span></span> <span data-ttu-id="ae7c1-106">因此，在本機使用者帳戶的安全性內容中執行的服務無法存取網路資源 (除了匿名使用者) 之外，它也無法支援用戶端用來驗證服務的 Kerberos 相互驗證。</span><span class="sxs-lookup"><span data-stu-id="ae7c1-106">Consequently, a service that runs in the security context of a local user account does not have access to network resources (except as an anonymous user), and it cannot support Kerberos mutual authentication in which the service is authenticated by its clients.</span></span> <span data-ttu-id="ae7c1-107">基於這些理由，本機使用者帳戶通常不適用於啟用目錄的服務。</span><span class="sxs-lookup"><span data-stu-id="ae7c1-107">For these reasons, local user accounts are typically inappropriate for directory-enabled services.</span></span> <span data-ttu-id="ae7c1-108">此外，服務中的 bug 無法損毀系統。</span><span class="sxs-lookup"><span data-stu-id="ae7c1-108">On the plus side, bugs in the service cannot damage the system.</span></span> <span data-ttu-id="ae7c1-109">如果您的服務可以在這些限制下執行，則應該如此。</span><span class="sxs-lookup"><span data-stu-id="ae7c1-109">If your service can run under those limitations, it should.</span></span>

 

 





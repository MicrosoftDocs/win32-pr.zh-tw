---
title: 安全性如何影響 Active Directory Domain Services 中的作業
description: Active Directory Domain Services 根據執行存取嘗試的使用者身分識別，使用存取控制來授與或拒絕物件、屬性和作業的存取權。
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory 中的安全性效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839307"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a><span data-ttu-id="7ff31-104">安全性如何影響 Active Directory Domain Services 中的作業</span><span class="sxs-lookup"><span data-stu-id="7ff31-104">How Security Affects Operations in Active Directory Domain Services</span></span>

<span data-ttu-id="7ff31-105">Active Directory Domain Services 根據執行存取嘗試的使用者身分識別，使用存取控制來授與或拒絕物件、屬性和作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="7ff31-105">Active Directory Domain Services use access control to grant or deny access to objects, properties, and operations based on the identity of the user performing the access attempt.</span></span> <span data-ttu-id="7ff31-106">當您的應用程式系結至目錄時，它會系結至特定的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="7ff31-106">When your application binds to the directory, it binds with specific user credentials.</span></span> <span data-ttu-id="7ff31-107">經過驗證後，這些認證會決定您應用程式的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="7ff31-107">When authenticated, these credentials determine your application's security context.</span></span> <span data-ttu-id="7ff31-108">無論認證是登入的使用者、指定的使用者、服務帳戶、電腦帳戶或未驗證的使用者 (Guest/Everyone) ，Active Directory 伺服器都會先確認使用者存取物件的許可權，然後再對該物件執行任何操作。</span><span class="sxs-lookup"><span data-stu-id="7ff31-108">Regardless of whether the credentials are those of the logged-on user, a specified user, a service account, a computer account, or an unauthenticated user (Guest/Everyone), the Active Directory server verifies the user's right to access an object before any operation is performed on that object.</span></span> <span data-ttu-id="7ff31-109">使用者不一定可以存取特定物件、其子系、屬性或該物件上的作業，這表示您的應用程式必須處理拒絕存取所造成的潛在錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ff31-109">The user may, or may not, have access to a particular object, its children, its properties, or operations on that object, which means that your application must handle the potential errors caused by denied access.</span></span>

<span data-ttu-id="7ff31-110">如需有關各種作業的安全性內容和存取控制影響的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="7ff31-110">For more information about security contexts and the effects of access control on various operations, see:</span></span>

-   [<span data-ttu-id="7ff31-111">存取控制和讀取作業</span><span class="sxs-lookup"><span data-stu-id="7ff31-111">Access Control and Read Operations</span></span>](access-control-and-read-operations.md)
-   [<span data-ttu-id="7ff31-112">存取控制和寫入作業</span><span class="sxs-lookup"><span data-stu-id="7ff31-112">Access Control and Write Operations</span></span>](access-control-and-write-operations.md)
-   [<span data-ttu-id="7ff31-113">存取控制和物件建立</span><span class="sxs-lookup"><span data-stu-id="7ff31-113">Access Control and Object Creation</span></span>](access-control-and-object-creation.md)
-   [<span data-ttu-id="7ff31-114">存取控制和物件刪除</span><span class="sxs-lookup"><span data-stu-id="7ff31-114">Access Control and Object Deletion</span></span>](access-control-and-object-deletion.md)

 

 





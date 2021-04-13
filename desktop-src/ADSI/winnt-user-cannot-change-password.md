---
title: '使用者無法變更 (WinNT 提供者的密碼) '
description: 使用者變更其密碼的能力是可授與或拒絕的許可權。
ms.assetid: 15905d16-aeee-4b06-8cb3-27419a8d0cb0
ms.tgt_platform: multiple
keywords:
- 使用者無法將密碼 (WinNT 提供者) ADSI
- 使用者無法變更密碼 ADSI、WinNT 提供者
- WinNT 提供者 ADSI、使用者管理範例、使用者無法變更密碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d8790f425c71f904957adcdb83d9c16af2f07f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300040"
---
# <a name="user-cannot-change-password-winnt-provider"></a><span data-ttu-id="0015e-106">使用者無法變更 (WinNT 提供者的密碼) </span><span class="sxs-lookup"><span data-stu-id="0015e-106">User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="0015e-107">使用者變更其密碼的能力是可授與或拒絕的許可權。</span><span class="sxs-lookup"><span data-stu-id="0015e-107">The ability of a user to change their password is a permission that can be granted or denied.</span></span> <span data-ttu-id="0015e-108">如需使用 WinNT 提供者以程式設計方式讀取和修改此許可權的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="0015e-108">For more information about programmatically reading and modifying this permission using the WinNT provider, see:</span></span>

-   [<span data-ttu-id="0015e-109">讀取使用者無法變更 (WinNT 提供者的密碼) </span><span class="sxs-lookup"><span data-stu-id="0015e-109">Reading User Cannot Change Password (WinNT Provider)</span></span>](reading-user-cannot-change-password-winnt-provider.md)
-   [<span data-ttu-id="0015e-110">修改使用者無法變更 (WinNT 提供者的密碼) </span><span class="sxs-lookup"><span data-stu-id="0015e-110">Modifying User Cannot Change Password (WinNT Provider)</span></span>](modifying-user-cannot-change-password-winnt-provider.md)

<span data-ttu-id="0015e-111">只有在使用 WinNT 提供者時，才可使用 user 物件的 **userFlags** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0015e-111">The **userFlags** attribute of the user object is only available when using the WinNT provider.</span></span>

<span data-ttu-id="0015e-112">您也可以使用 LDAP 提供者來讀取和修改此許可權。</span><span class="sxs-lookup"><span data-stu-id="0015e-112">It is also possible to read and modify this permission using the LDAP provider.</span></span> <span data-ttu-id="0015e-113">如需詳細資訊，請參閱 [使用者無法變更 (LDAP 提供者的密碼) ](user-cannot-change-password.md)。</span><span class="sxs-lookup"><span data-stu-id="0015e-113">For more information, see [User Cannot Change Password (LDAP Provider)](user-cannot-change-password.md).</span></span>

 

 





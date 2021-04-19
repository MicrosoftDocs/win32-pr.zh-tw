---
title: '帳戶鎖定 (LDAP 提供者) '
description: 當超過失敗的登入嘗試次數時，使用者帳戶會被鎖定一段時間（由 lockoutDuration 屬性所指定）。
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- 帳戶鎖定 (LDAP 提供者) ADSI
- 帳戶鎖定 ADSI，LDAP 提供者
- LDAP 提供者 ADSI，使用者管理範例，帳戶鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106967926"
---
# <a name="account-lockout-ldap-provider"></a><span data-ttu-id="f1793-106">帳戶鎖定 (LDAP 提供者) </span><span class="sxs-lookup"><span data-stu-id="f1793-106">Account Lockout (LDAP Provider)</span></span>

<span data-ttu-id="f1793-107">當超過失敗的登入嘗試次數時，使用者帳戶會被鎖定一段時間（由 [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) 屬性所指定）。</span><span class="sxs-lookup"><span data-stu-id="f1793-107">When the number of failed logon attempts is exceeded, the user account is locked out for a time period specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="f1793-108">[**IADsUser. IsAccountLocked**](iadsuser-property-methods.md)屬性看起來就像是用來讀取和修改使用者帳戶鎖定狀態的屬性，但是 LDAP ADSI 提供者不會正確支援 **IsAccountLocked** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f1793-108">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the LDAP ADSI provider does not accurately support the **IsAccountLocked** property.</span></span> <span data-ttu-id="f1793-109">若要取得並設定正確的帳戶鎖定資料，請使用 WinNT 提供者。</span><span class="sxs-lookup"><span data-stu-id="f1793-109">To obtain and set accurate account lockout data, use the WinNT provider.</span></span> <span data-ttu-id="f1793-110">如需搭配 WinNT 提供者使用 **IsAccountLocked** 屬性的詳細資訊，請參閱 [ (winnt 提供者的帳戶鎖定)](winnt-account-lockout.md)。</span><span class="sxs-lookup"><span data-stu-id="f1793-110">For more information about using the **IsAccountLocked** property with the WinNT provider, see [Account Lockout (WinNT Provider)](winnt-account-lockout.md).</span></span>

 

 
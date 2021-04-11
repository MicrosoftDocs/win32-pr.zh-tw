---
description: 密碼篩選
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: 密碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194922"
---
# <a name="password-filters"></a><span data-ttu-id="8af2e-103">密碼篩選</span><span class="sxs-lookup"><span data-stu-id="8af2e-103">Password Filters</span></span>

<span data-ttu-id="8af2e-104">密碼篩選器提供一種方式，讓您能夠執行密碼原則和變更通知。</span><span class="sxs-lookup"><span data-stu-id="8af2e-104">Password filters provide a way for you to implement password policy and change notification.</span></span>

<span data-ttu-id="8af2e-105">進行密碼變更要求時，「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」 (LSA) 會呼叫在系統上註冊的密碼篩選。</span><span class="sxs-lookup"><span data-stu-id="8af2e-105">When a password change request is made, the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) calls the password filters registered on the system.</span></span> <span data-ttu-id="8af2e-106">每個密碼篩選器都會呼叫兩次：先驗證新密碼，然後在所有篩選準則驗證新密碼之後，通知篩選已進行變更。</span><span class="sxs-lookup"><span data-stu-id="8af2e-106">Each password filter is called twice: first to validate the new password and then, after all filters have validated the new password, to notify the filters that the change has been made.</span></span> <span data-ttu-id="8af2e-107">下圖顯示這項程序。</span><span class="sxs-lookup"><span data-stu-id="8af2e-107">The following illustration shows this process.</span></span>

![密碼變更要求](images/pswdfilte.png)

<span data-ttu-id="8af2e-109">密碼變更通知是用來同步處理外部帳戶資料庫的密碼變更。</span><span class="sxs-lookup"><span data-stu-id="8af2e-109">Password change notification is used to synchronize password changes to foreign account databases.</span></span>

<span data-ttu-id="8af2e-110">密碼篩選器用來強制執行密碼原則。</span><span class="sxs-lookup"><span data-stu-id="8af2e-110">Password filters are used to enforce password policy.</span></span> <span data-ttu-id="8af2e-111">篩選準則會驗證新的密碼，並指出新的密碼是否符合已實行的密碼原則。</span><span class="sxs-lookup"><span data-stu-id="8af2e-111">Filters validate new passwords and indicate whether the new password conforms to the implemented password policy.</span></span>

<span data-ttu-id="8af2e-112">如需使用密碼篩選的總覽，請參閱 [使用密碼篩選器](using-password-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="8af2e-112">For an overview of using password filters, see [Using Password Filters](using-password-filters.md).</span></span>

<span data-ttu-id="8af2e-113">如需密碼篩選函數的清單，請參閱 [密碼篩選](management-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="8af2e-113">For a list of password filter functions, see [Password Filter Functions](management-functions.md).</span></span>

<span data-ttu-id="8af2e-114">下列主題提供有關密碼篩選的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="8af2e-114">The following topics provide more information about password filters:</span></span>

-   [<span data-ttu-id="8af2e-115">密碼篩選程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="8af2e-115">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
-   [<span data-ttu-id="8af2e-116">強式密碼強制執行和 Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="8af2e-116">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)

 

 

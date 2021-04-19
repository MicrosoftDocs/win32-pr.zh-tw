---
description: 說明如何執行密碼篩選匯出功能的考慮。
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: 密碼篩選程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998449"
---
# <a name="password-filter-programming-considerations"></a><span data-ttu-id="f8f43-103">密碼篩選程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="f8f43-103">Password Filter Programming Considerations</span></span>

<span data-ttu-id="f8f43-104">在執行 [*密碼篩選*](/windows/desktop/SecGloss/p-gly) 匯出函式時，請記住下列考慮：</span><span class="sxs-lookup"><span data-stu-id="f8f43-104">When implementing [*password filter*](/windows/desktop/SecGloss/p-gly) export functions, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="f8f43-105">使用 [*明文*](/windows/desktop/SecGloss/p-gly) 密碼時，請格外小心。</span><span class="sxs-lookup"><span data-stu-id="f8f43-105">Take great care when working with [*plaintext*](/windows/desktop/SecGloss/p-gly) passwords.</span></span> <span data-ttu-id="f8f43-106">透過網路傳送純文字密碼可能會危及安全性。</span><span class="sxs-lookup"><span data-stu-id="f8f43-106">Sending plaintext passwords over networks could compromise security.</span></span> <span data-ttu-id="f8f43-107">網路「嗅探程式」可以輕易地監看純文字密碼流量。</span><span class="sxs-lookup"><span data-stu-id="f8f43-107">Network "sniffers" can easily watch for plaintext password traffic.</span></span>
-   <span data-ttu-id="f8f43-108">在釋放記憶體之前呼叫 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函式，以清除用來儲存密碼的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="f8f43-108">Erase all memory used to store passwords by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function before freeing memory.</span></span>
-   <span data-ttu-id="f8f43-109">傳入密碼通知和篩選常式的所有緩衝區都應視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="f8f43-109">All buffers passed into password notification and filter routines should be treated as read-only.</span></span> <span data-ttu-id="f8f43-110">將資料寫入這些緩衝區可能會造成不穩定的行為。</span><span class="sxs-lookup"><span data-stu-id="f8f43-110">Writing data to these buffers may cause unstable behavior.</span></span>
-   <span data-ttu-id="f8f43-111">所有密碼通知和篩選常式都應該是安全線程。</span><span class="sxs-lookup"><span data-stu-id="f8f43-111">All password notification and filter routines should be thread-safe.</span></span> <span data-ttu-id="f8f43-112">使用重要區段或其他同步程式設計技術，在適當的情況下保護資料。</span><span class="sxs-lookup"><span data-stu-id="f8f43-112">Use critical sections or other synchronous programming techniques to protect data where appropriate.</span></span>
-   <span data-ttu-id="f8f43-113">密碼通知和篩選只會在裝載帳戶的電腦上進行。</span><span class="sxs-lookup"><span data-stu-id="f8f43-113">Password notification and filtering take place only on the computer that houses the account.</span></span>
-   <span data-ttu-id="f8f43-114">所有網域控制站都是可寫入的，因此密碼篩選器套件必須存在於所有網域控制站上。</span><span class="sxs-lookup"><span data-stu-id="f8f43-114">All domain controllers are writeable, therefore password filter packages must be present on all domain controllers.</span></span>

    <span data-ttu-id="f8f43-115">**Windows NT 4.0 網域：** 網域帳戶的通知只會在網域主控站上進行。</span><span class="sxs-lookup"><span data-stu-id="f8f43-115">**Windows NT 4.0 domains:** Notification on domain accounts takes place only on the primary domain controller.</span></span> <span data-ttu-id="f8f43-116">除了主域控制站以外，密碼篩選器套件應該安裝在所有備份網域控制站上，以允許在伺服器角色變更時繼續進行通知。</span><span class="sxs-lookup"><span data-stu-id="f8f43-116">In addition to the primary domain controller, the password filter packages should be installed on all backup domain controllers to allow notifications to continue in the event of server role changes.</span></span>

-   <span data-ttu-id="f8f43-117">所有密碼篩選 Dll 都是在本機系統帳戶的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 中執行。</span><span class="sxs-lookup"><span data-stu-id="f8f43-117">All password filter DLLs run in the [*security context*](/windows/desktop/SecGloss/s-gly) of the local system account.</span></span>



| <span data-ttu-id="f8f43-118">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="f8f43-118">For information about</span></span>                                                                                                                     | <span data-ttu-id="f8f43-119">請參閱</span><span class="sxs-lookup"><span data-stu-id="f8f43-119">See</span></span>                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f43-120">如何安裝及註冊您自己的 [*密碼篩選*](/windows/desktop/SecGloss/p-gly) DLL。</span><span class="sxs-lookup"><span data-stu-id="f8f43-120">How to install and register your own [*password filter*](/windows/desktop/SecGloss/p-gly) DLL.</span></span> | [<span data-ttu-id="f8f43-121">安裝和註冊密碼篩選 DLL</span><span class="sxs-lookup"><span data-stu-id="f8f43-121">Installing and Registering a Password Filter DLL</span></span>](installing-and-registering-a-password-filter-dll.md) |
| <span data-ttu-id="f8f43-122">Microsoft 提供的密碼篩選 DLL。</span><span class="sxs-lookup"><span data-stu-id="f8f43-122">The password filter DLL provided by Microsoft.</span></span>                                                                                            | [<span data-ttu-id="f8f43-123">強式密碼強制執行和 Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="f8f43-123">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)         |
| <span data-ttu-id="f8f43-124">匯出由密碼篩選 DLL 所執行的函式。</span><span class="sxs-lookup"><span data-stu-id="f8f43-124">Export functions implemented by a password filter DLL.</span></span>                                                                                    | [<span data-ttu-id="f8f43-125">密碼篩選函數</span><span class="sxs-lookup"><span data-stu-id="f8f43-125">Password Filter Functions</span></span>](management-functions.md)                          |



 

 

 

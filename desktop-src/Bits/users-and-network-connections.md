---
title: 使用者和網路連接
description: 只有當作業擁有者已登入且已建立網路連線時，BITS 才會傳送檔案。
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- 網路連接位
- 轉移工作位，擁有權
- 傳送作業位、擁有權、使用者帳戶
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7f841e3bf92004b62f3bbb576f71a45ac6b4a6bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093196"
---
# <a name="users-and-network-connections"></a><span data-ttu-id="6e676-106">使用者和網路連接</span><span class="sxs-lookup"><span data-stu-id="6e676-106">Users and Network Connections</span></span>

<span data-ttu-id="6e676-107">只有當作業擁有者已登入且已建立網路連線時，BITS 才會傳送檔案。</span><span class="sxs-lookup"><span data-stu-id="6e676-107">BITS transfers files only when the job owner is logged on and a network connection is established.</span></span> <span data-ttu-id="6e676-108">BITS 會使用作業擁有者的安全性內容來處理傳送作業。</span><span class="sxs-lookup"><span data-stu-id="6e676-108">BITS processes the transfer job using the security context of the job owner.</span></span> <span data-ttu-id="6e676-109">建立作業的使用者會被視為作業的擁有者。</span><span class="sxs-lookup"><span data-stu-id="6e676-109">The user who created the job is considered the owner of the job.</span></span> <span data-ttu-id="6e676-110">不過，具有系統管理員許可權的使用者可以取得其他使用者工作的 [**擁有權**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) 。</span><span class="sxs-lookup"><span data-stu-id="6e676-110">However, a user with administrator privileges can [**take ownership**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of another user's job.</span></span>

<span data-ttu-id="6e676-111">當擁有者登出或網路連線遺失 (BITS 不會強制) 的網路連線時，BITS 會暫停工作。</span><span class="sxs-lookup"><span data-stu-id="6e676-111">BITS suspends a job when the owner logs off or if the network connection is lost (BITS will not force a network connection).</span></span> <span data-ttu-id="6e676-112">當擁有者重新登入並建立網路連線時，BITS 會繼續執行作業。</span><span class="sxs-lookup"><span data-stu-id="6e676-112">BITS resumes the job when the owner logs back on and a network connection is established.</span></span> <span data-ttu-id="6e676-113">建立網路連線之後，在 BITS 開始傳送資料之前，可能會有短暫的延遲。</span><span class="sxs-lookup"><span data-stu-id="6e676-113">After the network connection is established, a short delay may occur before BITS begins transferring data.</span></span>

<span data-ttu-id="6e676-114">如果遺失網路連線，其狀態為 [**bg \_ 作業 \_ 狀態 \_**](/windows/desktop/api/Bits/ne-bits-bg_job_state) 為 [已佇列] 或 [ **bg \_ 工作 \_ 狀態 \_ ]** 的所有工作都會移至 [bg] **\_ 工作 \_ 狀態 \_ 暫時性 \_ 錯誤** 狀態，並出現「 [bg \_ E \_ 網路 \_ 中斷](bits-return-values.md) 連線」錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6e676-114">If the network connection is lost, all jobs whose state is [**BG\_JOB\_STATE\_QUEUED**](/windows/desktop/api/Bits/ne-bits-bg_job_state) or **BG\_JOB\_STATE\_TRANSFERRING** are moved to the **BG\_JOB\_STATE\_TRANSIENT\_ERROR** state with a [BG\_E\_NETWORK\_DISCONNECTED](bits-return-values.md) error code.</span></span> <span data-ttu-id="6e676-115">建立網路連線時， **BG \_ 工作 \_ 狀態 \_ 暫時性 \_ 錯誤** 狀態中的所有工作（可能包含任何錯誤碼）都會移至 **bg \_ 工作 \_ 狀態 \_ 佇列** 狀態。</span><span class="sxs-lookup"><span data-stu-id="6e676-115">When a network connection is established, all jobs in a **BG\_JOB\_STATE\_TRANSIENT\_ERROR** state, which may include any error code, are moved to the **BG\_JOB\_STATE\_QUEUED** state.</span></span>

<span data-ttu-id="6e676-116">若要讓 BITS 偵測到使用者已登入，使用者必須使用下列其中一個互動式登入選項：</span><span class="sxs-lookup"><span data-stu-id="6e676-116">For BITS to detect that a user is logged on, the user must use one of the following interactive logon options:</span></span>

-   <span data-ttu-id="6e676-117">透過歡迎畫面登入。</span><span class="sxs-lookup"><span data-stu-id="6e676-117">Log on through the Welcome screen.</span></span>
-   <span data-ttu-id="6e676-118">登入終端機 [服務](../termserv/terminal-services-portal.md) 用戶端。</span><span class="sxs-lookup"><span data-stu-id="6e676-118">Log on to a [terminal service](../termserv/terminal-services-portal.md) client.</span></span>
-   <span data-ttu-id="6e676-119">使用 [快速切換使用者](../shell/fast-user-switching.md)。</span><span class="sxs-lookup"><span data-stu-id="6e676-119">Use [fast user switching](../shell/fast-user-switching.md).</span></span>
-   <span data-ttu-id="6e676-120">從 Windows 10 1607 版開始，請使用遠端 Powershell 從其他裝置登入。</span><span class="sxs-lookup"><span data-stu-id="6e676-120">Starting with Windows 10, version 1607, log on from another device using Remote Powershell.</span></span> <span data-ttu-id="6e676-121">如需詳細資訊，請參閱 [管理 PowerShell 遠端會話](using-windows-powershell-to-create-bits-transfer-jobs.md) 。</span><span class="sxs-lookup"><span data-stu-id="6e676-121">See [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md) for details.</span></span>

<span data-ttu-id="6e676-122">使用 **RunAs** 命令) 以另一位 (使用者的身分執行應用程式，並不是互動式登入;BITS 不會執行與指定使用者相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="6e676-122">Running an application as another user (by using the **RunAs** command) is not an interactive logon; BITS will not run jobs associated with the specified user.</span></span>

<span data-ttu-id="6e676-123">LocalSystem、LocalService 和 NetworkService 系統帳戶一律會登入;因此，使用這些帳戶的服務所提交的作業一律會執行。</span><span class="sxs-lookup"><span data-stu-id="6e676-123">The LocalSystem, LocalService, and NetworkService system accounts are always logged on; therefore, jobs submitted by a service using these accounts always run.</span></span> <span data-ttu-id="6e676-124">如需使用服務帳戶的相關資訊和限制，請參閱 [服務帳戶和 BITS](service-accounts-and-bits.md)。</span><span class="sxs-lookup"><span data-stu-id="6e676-124">For information and limitations on using service accounts, see [Service Accounts and BITS](service-accounts-and-bits.md).</span></span>

<span data-ttu-id="6e676-125">作業擁有者可以提供協助程式權杖，以便在需要多個權杖才能完成傳輸的情況下使用，例如用於遠端主機的驗證。</span><span class="sxs-lookup"><span data-stu-id="6e676-125">Job owners can provide a helper token to be used in situations where multiple tokens are needed to complete a transfer, such as for authentication with a remote host.</span></span> <span data-ttu-id="6e676-126">如需詳細資訊，請參閱 [BITS 傳送工作的協助程式權杖](helper-tokens-for-bits-transfer-jobs.md) 。</span><span class="sxs-lookup"><span data-stu-id="6e676-126">See [Helper Tokens for BITS Transfer Jobs](helper-tokens-for-bits-transfer-jobs.md) for details.</span></span> <span data-ttu-id="6e676-127">在舊版的 Windows 中，作業擁有者實際上必須擁有系統管理員許可權，才能啟動使用 helper 權杖的工作。</span><span class="sxs-lookup"><span data-stu-id="6e676-127">In earlier versions of Windows, the job owner effectively had to have administrator privileges to start a job that used a helper token.</span></span> <span data-ttu-id="6e676-128">在 Windows 10 1607 版中，只要協助程式權杖沒有系統管理員功能，BITS 作業擁有者就可以在不是系統管理員的情況下設定 helper 權杖。</span><span class="sxs-lookup"><span data-stu-id="6e676-128">In Windows 10, version 1607, it is now possible for a BITS job owner to set helper tokens without being an administrator, as long as the helper token does not have administrator capabilities.</span></span> <span data-ttu-id="6e676-129">這將能透過讓背景下載或更新工具在具有較低權限的 NetworkService 帳戶 (而非具有系統管理員權限的帳戶) 下執行，來降低背景下載或更新工具的弱點數量。</span><span class="sxs-lookup"><span data-stu-id="6e676-129">This reduces the vulnerability footprint of background download or update tools by enabling them to run under the lower-privileged NetworkService account rather than under an account with administrative privileges.</span></span>

<span data-ttu-id="6e676-130">具有 [受限制權杖](../secauthz/restricted-tokens.md) 的使用者 (包含限制 sid 的權杖) 無法建立或修改作業。</span><span class="sxs-lookup"><span data-stu-id="6e676-130">Users with a [restricted token](../secauthz/restricted-tokens.md) (a token that contains restricting SIDs) cannot create or modify jobs.</span></span>
 

 
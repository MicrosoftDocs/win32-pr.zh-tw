---
title: 工作安全性強化
description: 使用「工作安全性強化」功能，可讓工作擁有者以最少的必要許可權來執行其工作。
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab70679d605a9ad56c6d26116245ae17d41a7a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183524"
---
# <a name="task-security-hardening"></a><span data-ttu-id="9ca93-103">工作安全性強化</span><span class="sxs-lookup"><span data-stu-id="9ca93-103">Task Security Hardening</span></span>

<span data-ttu-id="9ca93-104">使用「工作安全性強化」功能，可讓工作擁有者以最少的必要許可權來執行其工作。</span><span class="sxs-lookup"><span data-stu-id="9ca93-104">Using the tasks security hardening feature will allow task owners to run their tasks with minimum required privileges.</span></span> <span data-ttu-id="9ca93-105">請注意，這項功能預設為啟用，而且工作擁有者可以使用 [工作流程權杖安全識別碼類型] 和 [工作所需的許可權] 陣列進行進一步的調整。</span><span class="sxs-lookup"><span data-stu-id="9ca93-105">Note that this feature is enabled by default and task owners can make further adjustments by using the task process token security identifier type and task required privileges array.</span></span>

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a><span data-ttu-id="9ca93-106">工作進程權杖 SID 類型和工作所需的許可權陣列</span><span class="sxs-lookup"><span data-stu-id="9ca93-106">Task Process Token SID Type and Task Required Privileges Array</span></span>

<span data-ttu-id="9ca93-107">在工作定義層級指定 **ProcessTokenSidType** ，可讓工作擁有者要求以「無」 sid 類型或「不受限制」的 sid 類型來執行工作流程。</span><span class="sxs-lookup"><span data-stu-id="9ca93-107">Specifying **ProcessTokenSidType** at the task definition level allows task owners to request a task process to run with the "none" SID type or the "unrestricted" SID type.</span></span> <span data-ttu-id="9ca93-108">如果欄位存在於工作定義中，驗證可確保工作 UserId 包含其中一個作業系統內建服務帳戶的名稱或對應的 SID 字串：「網路服務」或「本機服務」。</span><span class="sxs-lookup"><span data-stu-id="9ca93-108">If the field is present in task definition, validation ensures that task UserId contains the name or the corresponding SID string for one of those operating system built-in service accounts: "NETWORK SERVICE" or "LOCAL SERVICE".</span></span>

<span data-ttu-id="9ca93-109">SID 類型「無」表示工作會在不包含處理常式權杖 SID 的進程中執行， (不會對處理常式權杖群組清單) 進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="9ca93-109">The SID type "none" means that the task runs in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span> <span data-ttu-id="9ca93-110">在該情況下， (LocalService/NetworkService) 的工作主體帳戶 SID 具有處理常式權杖的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="9ca93-110">The task principal account SID (LocalService/NetworkService) in that case has full access to the process token.</span></span>

<span data-ttu-id="9ca93-111">「不受限制」的 SID 類型表示工作 SID 將衍生自完整的工作路徑，並新增至「處理權杖群組」清單。</span><span class="sxs-lookup"><span data-stu-id="9ca93-111">The "unrestricted" SID type means that a task SID will be derived from the full task path and will be added to the process token groups list.</span></span> <span data-ttu-id="9ca93-112">例如，在 \\ \\ \\ \\ 本地服務帳戶中執行的 microsoft Windows RAC RACTask，工作 SID 衍生自名稱 RACTask，其中 "-" 會取代為 ""，因為 "" \\ \\ 是不正確使用者名稱字元。</span><span class="sxs-lookup"><span data-stu-id="9ca93-112">For example, the \\Microsoft\\Windows\\RAC\\RACTask which runs in the Local Service account, the task SID is derived from the name Microsoft-Windows-RAC-RACTask where a "-" is substituted for a "\\" since "\\" is an invalid user name character.</span></span> <span data-ttu-id="9ca93-113">工作 SID 的已知組名會是 "NT TASK \\ <modified full task path> " (domainname \\ username 格式) 。</span><span class="sxs-lookup"><span data-stu-id="9ca93-113">The well known group name for the task SID would be "NT TASK\\<modified full task path>" (domainname\\username format).</span></span> <span data-ttu-id="9ca93-114"> (DACL) 的程式權杖預設任意存取控制清單也會進行修改，只允許工作 SID 和本機系統 SID 的完整控制權，以及對工作主體帳戶 SID 的讀取控制。</span><span class="sxs-lookup"><span data-stu-id="9ca93-114">The process token default discretionary access control list (DACL) will also be modified to allow full control for the task SID and local system SID only and read control to the task principal account SID.</span></span> <span data-ttu-id="9ca93-115">"schtasks.exe/showsid/tn <full task path> " 將會顯示對應至工作的工作 SID。</span><span class="sxs-lookup"><span data-stu-id="9ca93-115">"schtasks.exe /showsid /tn <full task path>" will show the task SID that is corresponding to the task.</span></span>

<span data-ttu-id="9ca93-116">當非 COM 的工作動作啟動時，排程引擎會記錄工作主體帳戶、取得處理常式權杖，並查詢權杖所擁有的許可權清單，然後與 RequiredPrivileges 中指定的許可權清單進行比較。</span><span class="sxs-lookup"><span data-stu-id="9ca93-116">When a non-COM task action starts up, the scheduling engine logs on the task principal account, gets the process token and queries the list of privileges that the token has and then compares that with the privileges list specified in RequiredPrivileges.</span></span> <span data-ttu-id="9ca93-117">如果未在後者指定許可權，則會將其標示為已移除的「SE」 \_ 許可權 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9ca93-117">If a privilege is not specified in the latter, then that is marked as SE\_PRIVILEGE\_REMOVED.</span></span> <span data-ttu-id="9ca93-118">接著會使用 CreateProcessAsUser API，以產生的權杖控制碼啟動可執行檔動作。</span><span class="sxs-lookup"><span data-stu-id="9ca93-118">The executable action will then be started with the resulting token handle by using the CreateProcessAsUser API.</span></span>

<span data-ttu-id="9ca93-119">COM 工作動作啟動時，必須由 taskhost.exe 進程啟動。</span><span class="sxs-lookup"><span data-stu-id="9ca93-119">When a COM task action starts up, it must be activated by the taskhost.exe process.</span></span> <span data-ttu-id="9ca93-120">排程引擎會使用與啟動工作相同的帳戶，查詢每個執行中 taskhost.exe 的內容區塊。</span><span class="sxs-lookup"><span data-stu-id="9ca93-120">The scheduling engine queries the context block of each running taskhost.exe with the same account as the starting task.</span></span> <span data-ttu-id="9ca93-121">如果它發現主機進程是以啟動工作所需的許可權超集合來啟動，則該工作會在該進程中裝載。</span><span class="sxs-lookup"><span data-stu-id="9ca93-121">If it finds that a host process was started with a superset of privileges that the starting task needs, then that task gets hosted in that process.</span></span> <span data-ttu-id="9ca93-122">如果找不到這種處理常式，它會將工作主體帳戶下 taskhost 中執行之所有工作的強化資訊與指定的 RequiredPrivileges mask 結合，然後啟動 taskhost.exe 的新實例。</span><span class="sxs-lookup"><span data-stu-id="9ca93-122">If it does not find such a process, it combines the hardening info of all the tasks that are running in the taskhosts under the task principal account with the specified RequiredPrivileges mask and then starts up a new instance of taskhost.exe.</span></span>

<span data-ttu-id="9ca93-123">如果工作定義中沒有 RequiredPrivileges，則不含 SeImpersonatePrivilege 的工作主體帳戶預設許可權將用於工作進程。</span><span class="sxs-lookup"><span data-stu-id="9ca93-123">If RequiredPrivileges is not present in the task definition, the default privileges of task principal account without the SeImpersonatePrivilege will be used for task process.</span></span> <span data-ttu-id="9ca93-124">如果 **ProcessTokenSidType** 不存在於工作定義中，則會使用「不受限制」作為預設值。</span><span class="sxs-lookup"><span data-stu-id="9ca93-124">If **ProcessTokenSidType** is not present in the task definition, "unrestricted" is used as the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ca93-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ca93-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ca93-126">工作註冊資訊</span><span class="sxs-lookup"><span data-stu-id="9ca93-126">Task Registration Information</span></span>](task-registration-information.md)
</dt> <dt>

[<span data-ttu-id="9ca93-127">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="9ca93-127">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="9ca93-128">工作的安全性內容</span><span class="sxs-lookup"><span data-stu-id="9ca93-128">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 





---
title: TaskFolder. RegisterTask 方法
description: 在撰寫腳本時，註冊 (會使用 XML 來定義工作，在資料夾中建立) 新工作。
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- RegisterTask 方法工作排程器
- RegisterTask 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，RegisterTask 方法
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934833"
---
# <a name="taskfolderregistertask-method"></a><span data-ttu-id="38397-106">TaskFolder. RegisterTask 方法</span><span class="sxs-lookup"><span data-stu-id="38397-106">TaskFolder.RegisterTask method</span></span>

<span data-ttu-id="38397-107">在撰寫腳本時，註冊 (會使用 XML 來定義工作，在資料夾中建立) 新工作。</span><span class="sxs-lookup"><span data-stu-id="38397-107">For scripting, registers (creates) a new task in the folder using XML to define the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="38397-108">語法</span><span class="sxs-lookup"><span data-stu-id="38397-108">Syntax</span></span>


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a><span data-ttu-id="38397-109">參數</span><span class="sxs-lookup"><span data-stu-id="38397-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38397-110">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38397-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-111">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="38397-111">The name of the task.</span></span> <span data-ttu-id="38397-112">如果此值為 **Nothing**，則會在根工作資料夾中註冊工作，且工作名稱將會是工作排程器服務所建立的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="38397-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="38397-113">工作名稱的開頭或結尾不能是空白字元。</span><span class="sxs-lookup"><span data-stu-id="38397-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="38397-114">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="38397-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="38397-115">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="38397-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="38397-116">*xmlText* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38397-116">*xmlText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-117">工作的 XML 格式描述。</span><span class="sxs-lookup"><span data-stu-id="38397-117">An XML-formatted description of the task.</span></span>

<span data-ttu-id="38397-118">下列主題包含使用 XML 定義的工作。</span><span class="sxs-lookup"><span data-stu-id="38397-118">The following topics contain tasks defined using XML.</span></span>

-   [<span data-ttu-id="38397-119"> (XML) 的時間觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="38397-119">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)
-   <span data-ttu-id="38397-120">[ (XML) 的事件觸發程式範例 ](/previous-versions//aa446889(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38397-120">[Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85))</span></span>
-   [<span data-ttu-id="38397-121"> (XML) 的每日觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="38397-121">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)
-   [<span data-ttu-id="38397-122"> (XML) 的註冊觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="38397-122">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)
-   [<span data-ttu-id="38397-123"> (XML) 的每週觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="38397-123">Weekly Trigger Example (XML)</span></span>](weekly-trigger-example--xml-.md)
-   [<span data-ttu-id="38397-124"> (XML) 的登入觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="38397-124">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)
-   [<span data-ttu-id="38397-125"> (XML) 的開機觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="38397-125">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

</dd> <dt>

<span data-ttu-id="38397-126">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38397-126">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-127">工作 [**\_ 建立**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) 常數。</span><span class="sxs-lookup"><span data-stu-id="38397-127">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="38397-128">值</span><span class="sxs-lookup"><span data-stu-id="38397-128">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="38397-129">意義</span><span class="sxs-lookup"><span data-stu-id="38397-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="38397-130"><dt>**工作 \_\_僅驗證**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="38397-130"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="38397-131">工作排程器會檢查描述工作但未註冊工作的 XML 語法。</span><span class="sxs-lookup"><span data-stu-id="38397-131">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="38397-132">這個常數無法與工作 **\_ 建立**、工作 **\_ 更新** 或工作 **\_ 建立 \_ 或 \_ 更新** 值結合。</span><span class="sxs-lookup"><span data-stu-id="38397-132">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="38397-133"><dt>**工作 \_建立**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="38397-133"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="38397-134">工作排程器會將工作註冊為新工作。</span><span class="sxs-lookup"><span data-stu-id="38397-134">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="38397-135"><dt>**工作 \_UPDATE**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="38397-135"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="38397-136">工作排程器會將工作註冊為現有工作的更新版本。</span><span class="sxs-lookup"><span data-stu-id="38397-136">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="38397-137">更新註冊觸發程式的工作時，工作會在更新發生之後執行。</span><span class="sxs-lookup"><span data-stu-id="38397-137">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="38397-138"><dt>**工作 \_建立 \_ 或 \_ 更新**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="38397-138"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="38397-139">如果工作已存在，工作排程器會將工作註冊為新工作或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="38397-139">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="38397-140">相當於工作 \_ 建立 \| 工作 \_ 更新。</span><span class="sxs-lookup"><span data-stu-id="38397-140">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="38397-141"><dt>**工作 \_停**</dt>用 <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="38397-141"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="38397-142">工作排程器會停用現有的工作。</span><span class="sxs-lookup"><span data-stu-id="38397-142">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="38397-143"><dt>**工作 \_不要 \_ 新增 \_ 主體 \_ ACE**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="38397-143"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="38397-144">工作排程器無法新增內容主體的允許存取控制專案 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="38397-144">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="38397-145">使用這個旗標來呼叫 **TaskFolder. RegisterTask** 函式來更新工作時，工作排程器服務不會為新的內容主體新增 ace，也不會從舊的內容主體移除 ace。</span><span class="sxs-lookup"><span data-stu-id="38397-145">When the **TaskFolder.RegisterTask** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="38397-146"><dt>**工作 \_忽略 \_ 註冊 \_ 觸發**</dt>程式 <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="38397-146"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="38397-147">工作排程器會建立工作，但會忽略工作中的註冊觸發程式。</span><span class="sxs-lookup"><span data-stu-id="38397-147">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="38397-148">藉由略過註冊觸發程式，除非以時間為基礎的觸發程式使其在註冊時執行，否則工作將無法在註冊時執行。</span><span class="sxs-lookup"><span data-stu-id="38397-148">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                               |



 

</dd> <dt>

<span data-ttu-id="38397-149">*userId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38397-149">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-150">用來註冊工作的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="38397-150">The user credentials that are used to register the task.</span></span>

> [!Note]  
> <span data-ttu-id="38397-151">如果工作定義為工作排程器1.0 工作，則請勿在此 userId 參數中使用組名 (，而不是特定的使用者名稱) 。</span><span class="sxs-lookup"><span data-stu-id="38397-151">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="38397-152">當工作的 XML 中工作專案的 version 屬性設定為1.1 時，工作就會定義為工作排程器1.0 工作。</span><span class="sxs-lookup"><span data-stu-id="38397-152">A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</span></span>

 

</dd> <dt>

<span data-ttu-id="38397-153">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38397-153">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-154">用來註冊工作之 userId 的密碼。</span><span class="sxs-lookup"><span data-stu-id="38397-154">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="38397-155">\_使用工作登入 \_ 服務 \_ 帳戶登入類型時，密碼必須是空白的 **變異** 值，例如 **vt \_ Null** 或 **vt \_ 空白**。</span><span class="sxs-lookup"><span data-stu-id="38397-155">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="38397-156">*logonType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38397-156">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-157">定義用來執行已註冊工作的登入技巧。</span><span class="sxs-lookup"><span data-stu-id="38397-157">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="38397-158">值</span><span class="sxs-lookup"><span data-stu-id="38397-158">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="38397-159">意義</span><span class="sxs-lookup"><span data-stu-id="38397-159">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="38397-160"><dt>**工作 \_登入 \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="38397-160"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="38397-161">未指定登入方法。</span><span class="sxs-lookup"><span data-stu-id="38397-161">The logon method is not specified.</span></span> <span data-ttu-id="38397-162">用於非 NT 認證。</span><span class="sxs-lookup"><span data-stu-id="38397-162">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="38397-163"><dt>**工作 \_登入 \_ 密碼**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="38397-163"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="38397-164">使用密碼來登入使用者。</span><span class="sxs-lookup"><span data-stu-id="38397-164">Use a password for logging on the user.</span></span> <span data-ttu-id="38397-165">註冊時必須提供密碼。</span><span class="sxs-lookup"><span data-stu-id="38397-165">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="38397-166"><dt>**工作 \_登入 \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="38397-166"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="38397-167">使用現有的互動式權杖來執行工作。</span><span class="sxs-lookup"><span data-stu-id="38397-167">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="38397-168">使用者必須使用服務登入使用者 (S4U) 登入。</span><span class="sxs-lookup"><span data-stu-id="38397-168">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="38397-169">使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密的檔案。</span><span class="sxs-lookup"><span data-stu-id="38397-169">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="38397-170"><dt>**工作 \_登入 \_ 互動式 \_ 權杖**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="38397-170"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="38397-171">使用者必須已經登入。</span><span class="sxs-lookup"><span data-stu-id="38397-171">User must already be logged on.</span></span> <span data-ttu-id="38397-172">此工作只會在現有的互動式會話中執行。</span><span class="sxs-lookup"><span data-stu-id="38397-172">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="38397-173"><dt>**工作 \_登入 \_ 群組**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="38397-173"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="38397-174">群組啟用。</span><span class="sxs-lookup"><span data-stu-id="38397-174">Group activation.</span></span> <span data-ttu-id="38397-175">**GroupId** 欄位會指定群組。</span><span class="sxs-lookup"><span data-stu-id="38397-175">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="38397-176"><dt>**工作 \_登入 \_ 服務 \_ 帳戶**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="38397-176"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="38397-177">表示使用本機系統、本機服務或網路服務帳戶做為執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="38397-177">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="38397-178"><dt>**工作 \_登入 \_ 互動式 \_ 權杖 \_ 或 \_ 密碼**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="38397-178"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="38397-179">首先使用互動式權杖。</span><span class="sxs-lookup"><span data-stu-id="38397-179">First use the interactive token.</span></span> <span data-ttu-id="38397-180">如果使用者未登入 (沒有可使用的互動式權杖) ，則會使用密碼。</span><span class="sxs-lookup"><span data-stu-id="38397-180">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="38397-181">註冊工作時必須指定密碼。</span><span class="sxs-lookup"><span data-stu-id="38397-181">The password must be specified when a task is registered.</span></span> <span data-ttu-id="38397-182">因為新的工作比工作登入密碼更可靠，所以不建議使用此旗標 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="38397-182">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="38397-183">*sddl* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="38397-183">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-184">與已註冊工作相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="38397-184">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="38397-185">您可以在工作的安全描述項中指定 (ACL) 的存取控制清單，以允許或拒絕特定使用者和群組對工作的存取。</span><span class="sxs-lookup"><span data-stu-id="38397-185">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="38397-186">如果本機系統帳戶拒絕存取某項工作，工作排程器服務可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="38397-186">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="38397-187">*pTask* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="38397-187">*pTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38397-188">代表新工作的 [**RegisteredTask**](registeredtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="38397-188">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38397-189">傳回值</span><span class="sxs-lookup"><span data-stu-id="38397-189">Return value</span></span>

<span data-ttu-id="38397-190">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="38397-190">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38397-191">備註</span><span class="sxs-lookup"><span data-stu-id="38397-191">Remarks</span></span>

<span data-ttu-id="38397-192">對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="38397-192">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="38397-193">若要將工作登入類型設定為 interactive，請在工作主體的 [**LogonType**](principal-logontype.md)屬性中，或在 **TaskFolder. RegisterTask** 或 [**TaskFolder**](taskfolder-registertaskdefinition.md)的 *LogonType* 參數中指定 3 (工作登入 **\_ \_ 互動式 \_ 權杖**) 或 4 (工作 **登入 \_ \_ 群組**) 。</span><span class="sxs-lookup"><span data-stu-id="38397-193">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="38397-194">只有 Administrators 群組的成員可以建立具有開機觸發程式的工作。</span><span class="sxs-lookup"><span data-stu-id="38397-194">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="38397-195">您可以使用 *userId* 參數中所指定的群組來成功註冊工作，並在 **TaskFolder. RegisterTask** 或 [**TaskFolder**](taskfolder-registertaskdefinition.md)的 *logonType* 參數中指定 3 (工作登入 **互動式) \_ \_ \_ 權杖**，但不會執行該工作。</span><span class="sxs-lookup"><span data-stu-id="38397-195">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="38397-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="38397-196">Requirements</span></span>



| <span data-ttu-id="38397-197">需求</span><span class="sxs-lookup"><span data-stu-id="38397-197">Requirement</span></span> | <span data-ttu-id="38397-198">值</span><span class="sxs-lookup"><span data-stu-id="38397-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38397-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38397-199">Minimum supported client</span></span><br/> | <span data-ttu-id="38397-200">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38397-200">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="38397-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38397-201">Minimum supported server</span></span><br/> | <span data-ttu-id="38397-202">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38397-202">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38397-203">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="38397-203">Type library</span></span><br/>             | <dl> <span data-ttu-id="38397-204"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="38397-204"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="38397-205">DLL</span><span class="sxs-lookup"><span data-stu-id="38397-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38397-206"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38397-206"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38397-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38397-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38397-208">工作排程器</span><span class="sxs-lookup"><span data-stu-id="38397-208">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="38397-209">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="38397-209">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="38397-210">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="38397-210">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 


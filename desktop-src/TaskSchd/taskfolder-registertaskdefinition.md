---
title: TaskFolder. RegisterTaskDefinition 方法
description: 針對腳本，暫存器 (會使用 TaskDefinition 物件來定義工作，以在指定的位置建立) 工作。
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- RegisterTaskDefinition 方法工作排程器
- RegisterTaskDefinition 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，RegisterTaskDefinition 方法
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384917"
---
# <a name="taskfolderregistertaskdefinition-method"></a><span data-ttu-id="9be01-106">TaskFolder. RegisterTaskDefinition 方法</span><span class="sxs-lookup"><span data-stu-id="9be01-106">TaskFolder.RegisterTaskDefinition method</span></span>

<span data-ttu-id="9be01-107">針對腳本，暫存器 (會使用 [**TaskDefinition**](taskdefinition.md) 物件來定義工作，以在指定的位置建立) 工作。</span><span class="sxs-lookup"><span data-stu-id="9be01-107">For scripting, registers (creates) a task in a specified location using the [**TaskDefinition**](taskdefinition.md) object to define a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be01-108">語法</span><span class="sxs-lookup"><span data-stu-id="9be01-108">Syntax</span></span>


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a><span data-ttu-id="9be01-109">參數</span><span class="sxs-lookup"><span data-stu-id="9be01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be01-110">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9be01-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-111">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="9be01-111">The name of the task.</span></span> <span data-ttu-id="9be01-112">如果此值為 **Nothing**，則會在根工作資料夾中註冊工作，且工作名稱將會是工作排程器服務所建立的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="9be01-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="9be01-113">工作名稱的開頭或結尾不能是空白字元。</span><span class="sxs-lookup"><span data-stu-id="9be01-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="9be01-114">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="9be01-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="9be01-115">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="9be01-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="9be01-116">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9be01-116">*definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-117">已註冊之工作的定義。</span><span class="sxs-lookup"><span data-stu-id="9be01-117">The definition of the task that is registered.</span></span>

</dd> <dt>

<span data-ttu-id="9be01-118">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9be01-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-119">工作 [**\_ 建立**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) 常數。</span><span class="sxs-lookup"><span data-stu-id="9be01-119">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="9be01-120">值</span><span class="sxs-lookup"><span data-stu-id="9be01-120">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="9be01-121">意義</span><span class="sxs-lookup"><span data-stu-id="9be01-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="9be01-122"><dt>**工作 \_\_僅驗證**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-122"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="9be01-123">工作排程器會檢查描述工作但未註冊工作的 XML 語法。</span><span class="sxs-lookup"><span data-stu-id="9be01-123">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="9be01-124">這個常數無法與工作 **\_ 建立**、工作 **\_ 更新** 或工作 **\_ 建立 \_ 或 \_ 更新** 值結合。</span><span class="sxs-lookup"><span data-stu-id="9be01-124">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="9be01-125"><dt>**工作 \_建立**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-125"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="9be01-126">工作排程器會將工作註冊為新工作。</span><span class="sxs-lookup"><span data-stu-id="9be01-126">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="9be01-127"><dt>**工作 \_UPDATE**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-127"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="9be01-128">工作排程器會將工作註冊為現有工作的更新版本。</span><span class="sxs-lookup"><span data-stu-id="9be01-128">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="9be01-129">更新註冊觸發程式的工作時，工作會在更新發生之後執行。</span><span class="sxs-lookup"><span data-stu-id="9be01-129">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="9be01-130"><dt>**工作 \_建立 \_ 或 \_ 更新**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-130"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="9be01-131">如果工作已存在，工作排程器會將工作註冊為新工作或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="9be01-131">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="9be01-132">相當於工作 \_ 建立 \| 工作 \_ 更新。</span><span class="sxs-lookup"><span data-stu-id="9be01-132">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="9be01-133"><dt>**工作 \_停**</dt>用 <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-133"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="9be01-134">工作排程器會停用現有的工作。</span><span class="sxs-lookup"><span data-stu-id="9be01-134">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="9be01-135"><dt>**工作 \_不要 \_ 新增 \_ 主體 \_ ACE**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-135"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="9be01-136">工作排程器無法新增內容主體的允許存取控制專案 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="9be01-136">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="9be01-137">使用這個旗標來呼叫 **TaskFolder. RegisterTaskDefinition** 函式來更新工作時，工作排程器服務不會為新的內容主體新增 ace，也不會從舊的內容主體移除 ace。</span><span class="sxs-lookup"><span data-stu-id="9be01-137">When the **TaskFolder.RegisterTaskDefinition** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="9be01-138"><dt>**工作 \_忽略 \_ 註冊 \_ 觸發**</dt>程式 <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-138"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="9be01-139">工作排程器會建立工作，但會忽略工作中的註冊觸發程式。</span><span class="sxs-lookup"><span data-stu-id="9be01-139">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="9be01-140">藉由略過註冊觸發程式，除非以時間為基礎的觸發程式使其在註冊時執行，否則工作將無法在註冊時執行。</span><span class="sxs-lookup"><span data-stu-id="9be01-140">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="9be01-141">*userId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9be01-141">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-142">用來註冊工作的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="9be01-142">The user credentials that are used to register the task.</span></span> <span data-ttu-id="9be01-143">如果存在，這些認證會優先于 *定義* 參數所指向的工作定義物件中所指定的認證。</span><span class="sxs-lookup"><span data-stu-id="9be01-143">If present, these credentials take priority over the credentials specified in the task definition object pointed to by the *definition* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="9be01-144">如果工作定義為工作排程器1.0 工作，則請勿在此 userId 參數中使用組名 (，而不是特定的使用者名稱) 。</span><span class="sxs-lookup"><span data-stu-id="9be01-144">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="9be01-145">當工作設定中的 [ [**相容性**](tasksettings-compatibility.md) ] 屬性設定為 [1] 時，工作就會定義為工作排程器1.0 工作。</span><span class="sxs-lookup"><span data-stu-id="9be01-145">A task is defined as a Task Scheduler 1.0 task when the [**Compatibility**](tasksettings-compatibility.md) property is set to 1 in the task's settings.</span></span>

 

</dd> <dt>

<span data-ttu-id="9be01-146">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9be01-146">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-147">用來註冊工作之 userId 的密碼。</span><span class="sxs-lookup"><span data-stu-id="9be01-147">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="9be01-148">\_使用工作登入 \_ 服務 \_ 帳戶登入類型時，密碼必須是空白的 **變異** 值，例如 **vt \_ Null** 或 **vt \_ 空白**。</span><span class="sxs-lookup"><span data-stu-id="9be01-148">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="9be01-149">*logonType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9be01-149">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-150">定義用來執行已註冊工作的登入技巧。</span><span class="sxs-lookup"><span data-stu-id="9be01-150">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="9be01-151">值</span><span class="sxs-lookup"><span data-stu-id="9be01-151">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="9be01-152">意義</span><span class="sxs-lookup"><span data-stu-id="9be01-152">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="9be01-153"><dt>**工作 \_登入 \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-153"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="9be01-154">未指定登入方法。</span><span class="sxs-lookup"><span data-stu-id="9be01-154">The logon method is not specified.</span></span> <span data-ttu-id="9be01-155">用於非 NT 認證。</span><span class="sxs-lookup"><span data-stu-id="9be01-155">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="9be01-156"><dt>**工作 \_登入 \_ 密碼**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-156"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="9be01-157">使用密碼來登入使用者。</span><span class="sxs-lookup"><span data-stu-id="9be01-157">Use a password for logging on the user.</span></span> <span data-ttu-id="9be01-158">註冊時必須提供密碼。</span><span class="sxs-lookup"><span data-stu-id="9be01-158">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="9be01-159"><dt>**工作 \_登入 \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-159"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="9be01-160">使用現有的互動式權杖來執行工作。</span><span class="sxs-lookup"><span data-stu-id="9be01-160">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="9be01-161">使用者必須使用服務登入使用者 (S4U) 登入。</span><span class="sxs-lookup"><span data-stu-id="9be01-161">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="9be01-162">使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密的檔案。</span><span class="sxs-lookup"><span data-stu-id="9be01-162">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="9be01-163"><dt>**工作 \_登入 \_ 互動式 \_ 權杖**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-163"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="9be01-164">使用者必須已經登入。</span><span class="sxs-lookup"><span data-stu-id="9be01-164">User must already be logged on.</span></span> <span data-ttu-id="9be01-165">此工作只會在現有的互動式會話中執行。</span><span class="sxs-lookup"><span data-stu-id="9be01-165">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="9be01-166"><dt>**工作 \_登入 \_ 群組**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-166"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="9be01-167">群組啟用。</span><span class="sxs-lookup"><span data-stu-id="9be01-167">Group activation.</span></span> <span data-ttu-id="9be01-168">**GroupId** 欄位會指定群組。</span><span class="sxs-lookup"><span data-stu-id="9be01-168">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="9be01-169"><dt>**工作 \_登入 \_ 服務 \_ 帳戶**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-169"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="9be01-170">表示使用本機系統、本機服務或網路服務帳戶做為執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9be01-170">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="9be01-171"><dt>**工作 \_登入 \_ 互動式 \_ 權杖 \_ 或 \_ 密碼**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-171"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="9be01-172">首先使用互動式權杖。</span><span class="sxs-lookup"><span data-stu-id="9be01-172">First use the interactive token.</span></span> <span data-ttu-id="9be01-173">如果使用者未登入 (沒有可使用的互動式權杖) ，則會使用密碼。</span><span class="sxs-lookup"><span data-stu-id="9be01-173">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="9be01-174">註冊工作時必須指定密碼。</span><span class="sxs-lookup"><span data-stu-id="9be01-174">The password must be specified when a task is registered.</span></span> <span data-ttu-id="9be01-175">因為新的工作比工作登入密碼更可靠，所以不建議使用此旗標 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="9be01-175">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9be01-176">*sddl* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9be01-176">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-177">與已註冊工作相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="9be01-177">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="9be01-178">您可以在工作的安全描述項中指定 (ACL) 的存取控制清單，以允許或拒絕特定使用者和群組對工作的存取。</span><span class="sxs-lookup"><span data-stu-id="9be01-178">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="9be01-179">如果本機系統帳戶拒絕存取某項工作，工作排程器服務可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="9be01-179">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="9be01-180">工作 \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9be01-180">*task* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9be01-181">代表新工作的 [**RegisteredTask**](registeredtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9be01-181">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be01-182">傳回值</span><span class="sxs-lookup"><span data-stu-id="9be01-182">Return value</span></span>

<span data-ttu-id="9be01-183">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9be01-183">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9be01-184">備註</span><span class="sxs-lookup"><span data-stu-id="9be01-184">Remarks</span></span>

<span data-ttu-id="9be01-185">對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="9be01-185">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="9be01-186">若要將工作登入類型設定為 interactive，請在工作主體的 [**LogonType**](principal-logontype.md)屬性中，或在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 **TaskFolder** 的 *LogonType* 參數中指定 3 (工作登入 **\_ \_ 互動式 \_ 權杖**) 或 4 (工作 **登入 \_ \_ 群組**) 。</span><span class="sxs-lookup"><span data-stu-id="9be01-186">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**.</span></span>

<span data-ttu-id="9be01-187">只有 Administrators 群組的成員可以建立具有開機觸發程式的工作。</span><span class="sxs-lookup"><span data-stu-id="9be01-187">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="9be01-188">您可以使用 *userId* 參數中所指定的群組來成功註冊工作，並在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 **TaskFolder** 的 *logonType* 參數中指定 3 (工作登入 **互動式) \_ \_ \_ 權杖**，但不會執行該工作。</span><span class="sxs-lookup"><span data-stu-id="9be01-188">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**, but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="9be01-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="9be01-189">Requirements</span></span>



| <span data-ttu-id="9be01-190">需求</span><span class="sxs-lookup"><span data-stu-id="9be01-190">Requirement</span></span> | <span data-ttu-id="9be01-191">值</span><span class="sxs-lookup"><span data-stu-id="9be01-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be01-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9be01-192">Minimum supported client</span></span><br/> | <span data-ttu-id="9be01-193">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be01-193">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9be01-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9be01-194">Minimum supported server</span></span><br/> | <span data-ttu-id="9be01-195">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be01-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9be01-196">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9be01-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="9be01-197"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-197"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9be01-198">DLL</span><span class="sxs-lookup"><span data-stu-id="9be01-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9be01-199"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9be01-199"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be01-200">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9be01-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be01-201">工作排程器</span><span class="sxs-lookup"><span data-stu-id="9be01-201">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="9be01-202">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="9be01-202">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="9be01-203">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="9be01-203">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

 






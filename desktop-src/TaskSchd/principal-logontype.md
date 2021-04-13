---
title: Principal. LogonType 屬性
description: 針對腳本，取得或設定執行與主體相關聯之工作所需的安全性登入方法。
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- LogonType 屬性工作排程器
- LogonType 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，LogonType 屬性
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465629"
---
# <a name="principallogontype-property"></a><span data-ttu-id="e3f92-106">Principal. LogonType 屬性</span><span class="sxs-lookup"><span data-stu-id="e3f92-106">Principal.LogonType property</span></span>

<span data-ttu-id="e3f92-107">針對腳本，取得或設定執行與主體相關聯之工作所需的安全性登入方法。</span><span class="sxs-lookup"><span data-stu-id="e3f92-107">For scripting, gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f92-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3f92-108">Syntax</span></span>


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a><span data-ttu-id="e3f92-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e3f92-109">Property value</span></span>

<span data-ttu-id="e3f92-110">設定為下列其中一個工作 [**\_ 登入類型**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) 列舉常數。</span><span class="sxs-lookup"><span data-stu-id="e3f92-110">Set to one of the following [**TASK\_LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) enumeration constants.</span></span>



| <span data-ttu-id="e3f92-111">值</span><span class="sxs-lookup"><span data-stu-id="e3f92-111">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="e3f92-112">意義</span><span class="sxs-lookup"><span data-stu-id="e3f92-112">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="e3f92-113"><dt>**工作 \_登入 \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-113"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="e3f92-114">未指定登入方法。</span><span class="sxs-lookup"><span data-stu-id="e3f92-114">The logon method is not specified.</span></span> <span data-ttu-id="e3f92-115">用於非 NT 認證。</span><span class="sxs-lookup"><span data-stu-id="e3f92-115">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="e3f92-116"><dt>**工作 \_登入 \_ 密碼**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-116"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="e3f92-117">使用密碼來登入使用者。</span><span class="sxs-lookup"><span data-stu-id="e3f92-117">Use a password for logging on the user.</span></span> <span data-ttu-id="e3f92-118">註冊時必須提供密碼。</span><span class="sxs-lookup"><span data-stu-id="e3f92-118">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="e3f92-119"><dt>**工作 \_登入 \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-119"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="e3f92-120">使用現有的互動式權杖來執行工作。</span><span class="sxs-lookup"><span data-stu-id="e3f92-120">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="e3f92-121">使用者必須使用服務登入使用者 (S4U) 登入。</span><span class="sxs-lookup"><span data-stu-id="e3f92-121">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="e3f92-122">使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密的檔案。</span><span class="sxs-lookup"><span data-stu-id="e3f92-122">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="e3f92-123"><dt>**工作 \_登入 \_ 互動式 \_ 權杖**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-123"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="e3f92-124">使用者必須已經登入。</span><span class="sxs-lookup"><span data-stu-id="e3f92-124">User must already be logged on.</span></span> <span data-ttu-id="e3f92-125">此工作只會在現有的互動式會話中執行。</span><span class="sxs-lookup"><span data-stu-id="e3f92-125">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="e3f92-126"><dt>**工作 \_登入 \_ 群組**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-126"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="e3f92-127">群組啟用。</span><span class="sxs-lookup"><span data-stu-id="e3f92-127">Group activation.</span></span> <span data-ttu-id="e3f92-128">UserId 欄位會指定群組。</span><span class="sxs-lookup"><span data-stu-id="e3f92-128">The userId field specifies the group.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="e3f92-129"><dt>**工作 \_登入 \_ 服務 \_ 帳戶**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-129"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="e3f92-130">表示使用本機系統、本機服務或網路服務帳戶做為執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="e3f92-130">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="e3f92-131"><dt>**工作 \_登入 \_ 互動式 \_ 權杖 \_ 或 \_ 密碼**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-131"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e3f92-132">首先使用互動式權杖。</span><span class="sxs-lookup"><span data-stu-id="e3f92-132">First use the interactive token.</span></span> <span data-ttu-id="e3f92-133">如果使用者未登入 (沒有可使用的互動式權杖) ，則會使用密碼。</span><span class="sxs-lookup"><span data-stu-id="e3f92-133">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="e3f92-134">註冊工作時必須指定密碼。</span><span class="sxs-lookup"><span data-stu-id="e3f92-134">The password must be specified when a task is registered.</span></span> <span data-ttu-id="e3f92-135">因為新的工作比工作登入密碼更可靠，所以不建議使用此旗標 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="e3f92-135">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3f92-136">備註</span><span class="sxs-lookup"><span data-stu-id="e3f92-136">Remarks</span></span>

<span data-ttu-id="e3f92-137">只有當使用者識別碼是由 [**UserId**](principal-userid.md) 屬性指定時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="e3f92-137">This property is valid only when a user identifier is specified by the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="e3f92-138">讀取或寫入工作的 XML 時，登入類型會在 [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) 工作排程器架構的元素中指定。</span><span class="sxs-lookup"><span data-stu-id="e3f92-138">When reading or writing XML for a task, the logon type is specified in the [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="e3f92-139">對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="e3f92-139">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="e3f92-140">若要將工作登入類型設定為 interactive，請在工作主體的 **LogonType** 屬性中，或在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 [**TaskFolder**](taskfolder-registertaskdefinition.md)的 *LogonType* 參數中指定 3 (工作登入 **\_ \_ 互動式 \_ 權杖**) 或 4 (工作 **登入 \_ \_ 群組**) 。</span><span class="sxs-lookup"><span data-stu-id="e3f92-140">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the **LogonType** property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f92-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3f92-141">Requirements</span></span>



| <span data-ttu-id="e3f92-142">需求</span><span class="sxs-lookup"><span data-stu-id="e3f92-142">Requirement</span></span> | <span data-ttu-id="e3f92-143">值</span><span class="sxs-lookup"><span data-stu-id="e3f92-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f92-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3f92-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f92-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3f92-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e3f92-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3f92-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f92-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3f92-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3f92-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e3f92-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3f92-149"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e3f92-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e3f92-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3f92-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3f92-151"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f92-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3f92-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f92-153">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e3f92-153">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e3f92-154">**主要**</span><span class="sxs-lookup"><span data-stu-id="e3f92-154">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 






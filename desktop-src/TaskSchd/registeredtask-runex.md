---
title: RegisteredTask. RunEx 方法
description: 針對腳本，會使用指定的旗標和會話識別碼立即執行已註冊的工作。
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- RunEx 方法工作排程器
- RunEx 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，RunEx 方法
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104663"
---
# <a name="registeredtaskrunex-method"></a><span data-ttu-id="26b56-106">RegisteredTask. RunEx 方法</span><span class="sxs-lookup"><span data-stu-id="26b56-106">RegisteredTask.RunEx method</span></span>

<span data-ttu-id="26b56-107">針對腳本，會使用指定的旗標和會話識別碼立即執行已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="26b56-107">For scripting, runs the registered task immediately using specified flags and a session identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b56-108">語法</span><span class="sxs-lookup"><span data-stu-id="26b56-108">Syntax</span></span>


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="26b56-109">參數</span><span class="sxs-lookup"><span data-stu-id="26b56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b56-110">*params* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26b56-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b56-111">用來當做工作動作中之值的參數。</span><span class="sxs-lookup"><span data-stu-id="26b56-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="26b56-112">若不指定工作動作的任何參數值，請將此參數設定為 **Nothing**。</span><span class="sxs-lookup"><span data-stu-id="26b56-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="26b56-113">否則，可以指定單一字串值或字串值的陣列。</span><span class="sxs-lookup"><span data-stu-id="26b56-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="26b56-114">您指定的字串值會與名稱配對，並以名稱/值組的形式儲存。</span><span class="sxs-lookup"><span data-stu-id="26b56-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="26b56-115">如果您指定單一字串值，則 Arg0 將會是指派給值的名稱。</span><span class="sxs-lookup"><span data-stu-id="26b56-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="26b56-116">此值可以在工作動作中使用，其中 $ (Arg0) 變數會在動作屬性中使用。</span><span class="sxs-lookup"><span data-stu-id="26b56-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="26b56-117">如果您傳入值（例如 "0"、"100" 和 "250"）做為字串值的陣列，則 "0" 將取代 $ (Arg0) 變數，"100" 將取代 $ (Arg1) 變數，而 "250" 將取代動作屬性中使用的 $ (Arg2) 變數。</span><span class="sxs-lookup"><span data-stu-id="26b56-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="26b56-118">最多可以指定32個字串值。</span><span class="sxs-lookup"><span data-stu-id="26b56-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="26b56-119">如需詳細資訊和可使用 $ (Arg0) ，$ (Arg1) ，...，$ (Arg32) 變數值的動作屬性清單，請參閱工作 [動作](task-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="26b56-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="26b56-120">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26b56-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b56-121">工作 [ \_ 執行 \_ 旗標](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) 常數，定義工作的執行方式。</span><span class="sxs-lookup"><span data-stu-id="26b56-121">A [TASK\_RUN\_FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) constant that defines how the task is run.</span></span>

</dd> <dt>

<span data-ttu-id="26b56-122">*sessionID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26b56-122">*sessionID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b56-123">您要在其中啟動工作的終端機伺服器會話。</span><span class="sxs-lookup"><span data-stu-id="26b56-123">The terminal server session in which you want to launch the task.</span></span>

<span data-ttu-id="26b56-124">如果工作 \_ 執行 \_ 使用 \_ 會話 \_ 識別碼常數 (0x4) 不會傳遞至 *flags* 參數，則會忽略此參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="26b56-124">If the TASK\_RUN\_USE\_SESSION\_ID constant (0x4) is not passed into the *flags* parameter, then the value specified in this parameter is ignored.</span></span> <span data-ttu-id="26b56-125">如果工作回合 \_ \_ 使用 \_ 會話 \_ 識別碼常數傳遞至 *flags* 參數，且 sessionID 值小於或等於0，則會傳回不正確引數錯誤。</span><span class="sxs-lookup"><span data-stu-id="26b56-125">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.</span></span>

<span data-ttu-id="26b56-126">如果工作回合 \_ \_ 使用 \_ 會話 \_ 識別碼常數傳遞至 *旗標* 參數，且 sessionID 值是大於0的有效會話識別碼，且如果沒有為 *使用者* 參數指定任何值，則工作排程器服務會嘗試以互動方式啟動工作，就像登入指定會話的使用者一樣。</span><span class="sxs-lookup"><span data-stu-id="26b56-126">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is logged on to the specified session.</span></span>

<span data-ttu-id="26b56-127">如果工作回合 \_ \_ 使用 \_ 會話 \_ 識別碼常數傳遞至 *旗標* 參數，且 sessionID 值是大於0的有效會話識別碼，且使用者參數中指定了使用者，則工作排程器服務會嘗試以互動方式啟動工作，就像使用者參數中指定的使用者一樣。 </span><span class="sxs-lookup"><span data-stu-id="26b56-127">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="26b56-128">*runningTask* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="26b56-128">*runningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26b56-129">定義工作新實例的 [**RunningTask**](runningtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="26b56-129">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b56-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="26b56-130">Return value</span></span>

<span data-ttu-id="26b56-131">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="26b56-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b56-132">備註</span><span class="sxs-lookup"><span data-stu-id="26b56-132">Remarks</span></span>

<span data-ttu-id="26b56-133">這個方法會傳回而不會發生錯誤，但是如果已註冊工作的 [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) 屬性設定為 false，則不會執行此工作。</span><span class="sxs-lookup"><span data-stu-id="26b56-133">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b56-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="26b56-134">Requirements</span></span>



| <span data-ttu-id="26b56-135">需求</span><span class="sxs-lookup"><span data-stu-id="26b56-135">Requirement</span></span> | <span data-ttu-id="26b56-136">值</span><span class="sxs-lookup"><span data-stu-id="26b56-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26b56-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26b56-137">Minimum supported client</span></span><br/> | <span data-ttu-id="26b56-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26b56-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="26b56-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26b56-139">Minimum supported server</span></span><br/> | <span data-ttu-id="26b56-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26b56-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26b56-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="26b56-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="26b56-142"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26b56-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26b56-143">DLL</span><span class="sxs-lookup"><span data-stu-id="26b56-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26b56-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26b56-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b56-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26b56-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b56-146">工作排程器</span><span class="sxs-lookup"><span data-stu-id="26b56-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="26b56-147">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="26b56-147">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 






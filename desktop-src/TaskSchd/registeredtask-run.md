---
title: RegisteredTask 方法
description: 針對腳本，會立即執行已註冊的工作。
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Run 方法工作排程器
- Run 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，Run 方法
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966137"
---
# <a name="registeredtaskrun-method"></a><span data-ttu-id="8465e-106">RegisteredTask 方法</span><span class="sxs-lookup"><span data-stu-id="8465e-106">RegisteredTask.Run method</span></span>

<span data-ttu-id="8465e-107">針對腳本，會立即執行已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="8465e-107">For scripting, runs the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="8465e-108">語法</span><span class="sxs-lookup"><span data-stu-id="8465e-108">Syntax</span></span>


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="8465e-109">參數</span><span class="sxs-lookup"><span data-stu-id="8465e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8465e-110">*params* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8465e-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8465e-111">用來當做工作動作中之值的參數。</span><span class="sxs-lookup"><span data-stu-id="8465e-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="8465e-112">若不指定工作動作的任何參數值，請將此參數設定為 **Nothing**。</span><span class="sxs-lookup"><span data-stu-id="8465e-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="8465e-113">否則，可以指定單一字串值或字串值的陣列。</span><span class="sxs-lookup"><span data-stu-id="8465e-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="8465e-114">您指定的字串值會與名稱配對，並以名稱/值組的形式儲存。</span><span class="sxs-lookup"><span data-stu-id="8465e-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="8465e-115">如果您指定單一字串值，則 Arg0 將會是指派給值的名稱。</span><span class="sxs-lookup"><span data-stu-id="8465e-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="8465e-116">此值可以在工作動作中使用，其中 $ (Arg0) 變數會在動作屬性中使用。</span><span class="sxs-lookup"><span data-stu-id="8465e-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="8465e-117">如果您傳入值（例如 "0"、"100" 和 "250"）做為字串值的陣列，則 "0" 將取代 $ (Arg0) 變數，"100" 將取代 $ (Arg1) 變數，而 "250" 將取代動作屬性中使用的 $ (Arg2) 變數。</span><span class="sxs-lookup"><span data-stu-id="8465e-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="8465e-118">最多可以指定32個字串值。</span><span class="sxs-lookup"><span data-stu-id="8465e-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="8465e-119">如需詳細資訊和可使用 $ (Arg0) ，$ (Arg1) ，...，$ (Arg32) 變數值的動作屬性清單，請參閱工作 [動作](task-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="8465e-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="8465e-120">*ppRunningTask* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8465e-120">*ppRunningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8465e-121">定義工作新實例的 [**RunningTask**](runningtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8465e-121">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8465e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="8465e-122">Return value</span></span>

<span data-ttu-id="8465e-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8465e-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8465e-124">備註</span><span class="sxs-lookup"><span data-stu-id="8465e-124">Remarks</span></span>

<span data-ttu-id="8465e-125">**RegisteredTask** 函式相當於 [**RegisteredTask. RunEx**](registeredtask-runex.md)函式，其 flags 參數等於0，而且沒有針對使用者參數指定任何專案。</span><span class="sxs-lookup"><span data-stu-id="8465e-125">The **RegisteredTask.Run** function is equivalent to the [**RegisteredTask.RunEx**](registeredtask-runex.md) function with the flags parameter equal to 0 and nothing specified for the user parameter.</span></span>

<span data-ttu-id="8465e-126">這個方法會傳回而不會發生錯誤，但是如果已註冊工作的 [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) 屬性設定為 false，則不會執行此工作。</span><span class="sxs-lookup"><span data-stu-id="8465e-126">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="8465e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8465e-127">Requirements</span></span>



| <span data-ttu-id="8465e-128">需求</span><span class="sxs-lookup"><span data-stu-id="8465e-128">Requirement</span></span> | <span data-ttu-id="8465e-129">值</span><span class="sxs-lookup"><span data-stu-id="8465e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8465e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8465e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8465e-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8465e-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8465e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8465e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8465e-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8465e-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8465e-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8465e-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="8465e-135"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8465e-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8465e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8465e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8465e-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8465e-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8465e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8465e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8465e-139">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8465e-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8465e-140">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="8465e-140">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 






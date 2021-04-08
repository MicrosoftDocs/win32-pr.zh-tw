---
title: TaskSettings. AllowHardTerminate 屬性
description: 針對腳本，取得或設定布林值，這個值表示工作可能會由使用 TerminateProcess 的工作排程器服務終止。
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- AllowHardTerminate 屬性工作排程器
- AllowHardTerminate 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、AllowHardTerminate 屬性
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686136"
---
# <a name="tasksettingsallowhardterminate-property"></a><span data-ttu-id="36d1f-106">TaskSettings. AllowHardTerminate 屬性</span><span class="sxs-lookup"><span data-stu-id="36d1f-106">TaskSettings.AllowHardTerminate property</span></span>

<span data-ttu-id="36d1f-107">針對腳本，取得或設定布林值，這個值表示工作可能會由使用 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)的工作排程器服務終止。</span><span class="sxs-lookup"><span data-stu-id="36d1f-107">For scripting, gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="36d1f-108">服務會藉由傳送 [**WM \_ 關閉**](../winmsg/wm-close.md) 通知來嘗試關閉執行中的工作，如果工作沒有回應，則只有在這個屬性設定為 true 時，才會終止工作。</span><span class="sxs-lookup"><span data-stu-id="36d1f-108">The service will try to close the running task by sending the [**WM\_CLOSE**](../winmsg/wm-close.md) notification, and if the task does not respond, the task will be terminated only if this property is set to true.</span></span>

<span data-ttu-id="36d1f-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="36d1f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d1f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="36d1f-110">Syntax</span></span>


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="36d1f-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="36d1f-111">Property value</span></span>

<span data-ttu-id="36d1f-112">若為 True，則可使用 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)來終止工作。</span><span class="sxs-lookup"><span data-stu-id="36d1f-112">If True, the task can be terminated by using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="36d1f-113">如果為 False，則無法使用 **TerminateProcess** 來終止工作。</span><span class="sxs-lookup"><span data-stu-id="36d1f-113">If False, the task cannot be terminated by using **TerminateProcess**.</span></span>

## <a name="remarks"></a><span data-ttu-id="36d1f-114">備註</span><span class="sxs-lookup"><span data-stu-id="36d1f-114">Remarks</span></span>

<span data-ttu-id="36d1f-115">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="36d1f-115">When reading or writing XML for a task, this setting is specified in the [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d1f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="36d1f-116">Requirements</span></span>



| <span data-ttu-id="36d1f-117">需求</span><span class="sxs-lookup"><span data-stu-id="36d1f-117">Requirement</span></span> | <span data-ttu-id="36d1f-118">值</span><span class="sxs-lookup"><span data-stu-id="36d1f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36d1f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36d1f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36d1f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36d1f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="36d1f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36d1f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36d1f-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36d1f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36d1f-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="36d1f-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="36d1f-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="36d1f-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="36d1f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="36d1f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d1f-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d1f-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36d1f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36d1f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d1f-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="36d1f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 


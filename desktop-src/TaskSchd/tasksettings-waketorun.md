---
title: TaskSettings. WakeToRun 屬性
description: 針對腳本，取得或設定布林值，指出工作排程器會在執行工作時喚醒電腦。
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- WakeToRun 屬性工作排程器
- WakeToRun 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、WakeToRun 屬性
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685733"
---
# <a name="tasksettingswaketorun-property"></a><span data-ttu-id="31ca0-106">TaskSettings. WakeToRun 屬性</span><span class="sxs-lookup"><span data-stu-id="31ca0-106">TaskSettings.WakeToRun property</span></span>

<span data-ttu-id="31ca0-107">針對腳本，取得或設定布林值，指出工作排程器會在執行工作時喚醒電腦。</span><span class="sxs-lookup"><span data-stu-id="31ca0-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

<span data-ttu-id="31ca0-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="31ca0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ca0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="31ca0-109">Syntax</span></span>


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a><span data-ttu-id="31ca0-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="31ca0-110">Property value</span></span>

<span data-ttu-id="31ca0-111">若為 True，則屬性會指出工作排程器會在執行工作時喚醒電腦。</span><span class="sxs-lookup"><span data-stu-id="31ca0-111">If True, the property indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ca0-112">備註</span><span class="sxs-lookup"><span data-stu-id="31ca0-112">Remarks</span></span>

<span data-ttu-id="31ca0-113">當工作排程器服務喚醒電腦以執行工作時，即使電腦不再處於睡眠或睡眠模式，畫面仍會保持關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="31ca0-113">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="31ca0-114">當 Windows Vista 偵測到使用者已回到使用電腦時，畫面會開啟。</span><span class="sxs-lookup"><span data-stu-id="31ca0-114">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="31ca0-115">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="31ca0-115">When reading or writing XML for a task, this setting is specified in the [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ca0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="31ca0-116">Requirements</span></span>



| <span data-ttu-id="31ca0-117">需求</span><span class="sxs-lookup"><span data-stu-id="31ca0-117">Requirement</span></span> | <span data-ttu-id="31ca0-118">值</span><span class="sxs-lookup"><span data-stu-id="31ca0-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31ca0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31ca0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31ca0-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31ca0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="31ca0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31ca0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31ca0-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31ca0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31ca0-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="31ca0-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="31ca0-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="31ca0-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="31ca0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="31ca0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31ca0-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31ca0-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31ca0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31ca0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ca0-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="31ca0-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






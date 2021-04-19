---
title: WakeToRun (settingsType) 元素
description: 指定工作排程器會在執行工作時喚醒電腦。
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- WakeToRun 元素工作排程器
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991780"
---
# <a name="waketorun-settingstype-element"></a><span data-ttu-id="e226d-104">WakeToRun (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="e226d-104">WakeToRun (settingsType) Element</span></span>

<span data-ttu-id="e226d-105">指定工作排程器會在執行工作時喚醒電腦。</span><span class="sxs-lookup"><span data-stu-id="e226d-105">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span>

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

<span data-ttu-id="e226d-106">**WakeToRun** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="e226d-106">The **WakeToRun** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e226d-107">父元素</span><span class="sxs-lookup"><span data-stu-id="e226d-107">Parent element</span></span>



| <span data-ttu-id="e226d-108">元素</span><span class="sxs-lookup"><span data-stu-id="e226d-108">Element</span></span>                                                           | <span data-ttu-id="e226d-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="e226d-109">Derived from</span></span>                                                         | <span data-ttu-id="e226d-110">Description</span><span class="sxs-lookup"><span data-stu-id="e226d-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e226d-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="e226d-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e226d-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="e226d-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e226d-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="e226d-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e226d-114">備註</span><span class="sxs-lookup"><span data-stu-id="e226d-114">Remarks</span></span>

<span data-ttu-id="e226d-115">當工作排程器服務喚醒電腦以執行工作時，即使電腦不再處於睡眠或睡眠模式，畫面仍會保持關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="e226d-115">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="e226d-116">當 Windows Vista 偵測到使用者已回到使用電腦時，畫面會開啟。</span><span class="sxs-lookup"><span data-stu-id="e226d-116">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="e226d-117">針對 c + + 開發，請參閱 [**ITaskSettings 的 WakeToRun 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun)。</span><span class="sxs-lookup"><span data-stu-id="e226d-117">For C++ development, see [**WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span></span>

<span data-ttu-id="e226d-118">如需腳本開發，請參閱 [**TaskSettings. WakeToRun**](tasksettings-waketorun.md)。</span><span class="sxs-lookup"><span data-stu-id="e226d-118">For script development, see [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e226d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e226d-119">Requirements</span></span>



| <span data-ttu-id="e226d-120">需求</span><span class="sxs-lookup"><span data-stu-id="e226d-120">Requirement</span></span> | <span data-ttu-id="e226d-121">值</span><span class="sxs-lookup"><span data-stu-id="e226d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e226d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e226d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e226d-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e226d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e226d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e226d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e226d-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e226d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e226d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e226d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e226d-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="e226d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e226d-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e226d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






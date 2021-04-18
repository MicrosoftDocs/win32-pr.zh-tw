---
title: DeleteExpiredTaskAfter (settingsType) 元素
description: 指定在工作到期之後，工作排程器將等待的時間量。
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- DeleteExpiredTaskAfter 元素工作排程器
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965289"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a><span data-ttu-id="e16e0-104">DeleteExpiredTaskAfter (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="e16e0-104">DeleteExpiredTaskAfter (settingsType) Element</span></span>

<span data-ttu-id="e16e0-105">指定在工作到期之後，工作排程器將等待的時間量。</span><span class="sxs-lookup"><span data-stu-id="e16e0-105">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="e16e0-106">如果未指定這個專案的值，工作排程器服務將不會刪除該工作。</span><span class="sxs-lookup"><span data-stu-id="e16e0-106">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span> <span data-ttu-id="e16e0-107">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="e16e0-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e16e0-108">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="e16e0-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

<span data-ttu-id="e16e0-109">**DeleteExpiredTaskAfter** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="e16e0-109">The **DeleteExpiredTaskAfter** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e16e0-110">父元素</span><span class="sxs-lookup"><span data-stu-id="e16e0-110">Parent element</span></span>



| <span data-ttu-id="e16e0-111">元素</span><span class="sxs-lookup"><span data-stu-id="e16e0-111">Element</span></span>                                                           | <span data-ttu-id="e16e0-112">衍生自</span><span class="sxs-lookup"><span data-stu-id="e16e0-112">Derived from</span></span>                                                         | <span data-ttu-id="e16e0-113">Description</span><span class="sxs-lookup"><span data-stu-id="e16e0-113">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e16e0-114">**設定**</span><span class="sxs-lookup"><span data-stu-id="e16e0-114">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e16e0-115">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="e16e0-115">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e16e0-116">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="e16e0-116">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e16e0-117">備註</span><span class="sxs-lookup"><span data-stu-id="e16e0-117">Remarks</span></span>

<span data-ttu-id="e16e0-118">針對 c + + 開發，請參閱 [**ITaskSettings 的 DeleteExpiredTaskAfter 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter)。</span><span class="sxs-lookup"><span data-stu-id="e16e0-118">For C++ development, see [**DeleteExpiredTaskAfter Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span></span>

<span data-ttu-id="e16e0-119">如需腳本開發，請參閱 [**TaskSettings. DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)。</span><span class="sxs-lookup"><span data-stu-id="e16e0-119">For script development, see [**TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e16e0-120">範例</span><span class="sxs-lookup"><span data-stu-id="e16e0-120">Examples</span></span>

<span data-ttu-id="e16e0-121">下列 XML 定義的設定專案會在一周後刪除已過期的工作。</span><span class="sxs-lookup"><span data-stu-id="e16e0-121">The following XML defines a settings element that deletes an expired task after one week.</span></span>


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e16e0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e16e0-122">Requirements</span></span>



| <span data-ttu-id="e16e0-123">需求</span><span class="sxs-lookup"><span data-stu-id="e16e0-123">Requirement</span></span> | <span data-ttu-id="e16e0-124">值</span><span class="sxs-lookup"><span data-stu-id="e16e0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e16e0-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e16e0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e16e0-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e16e0-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e16e0-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e16e0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e16e0-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e16e0-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e16e0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e16e0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e16e0-130">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="e16e0-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






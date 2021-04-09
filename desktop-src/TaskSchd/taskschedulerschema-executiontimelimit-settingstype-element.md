---
title: ExecutionTimeLimit (settingsType) 元素
description: 允許完成工作的時間量。
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- ExecutionTimeLimit 元素工作排程器
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843228"
---
# <a name="executiontimelimit-settingstype-element"></a><span data-ttu-id="cd23a-104">ExecutionTimeLimit (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="cd23a-104">ExecutionTimeLimit (settingsType) Element</span></span>

<span data-ttu-id="cd23a-105">允許完成工作的時間量。此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="cd23a-105">Amount of time allowed to complete the task.The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="cd23a-106">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="cd23a-106">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="cd23a-107">PT0S 的值會讓工作無限期地執行。</span><span class="sxs-lookup"><span data-stu-id="cd23a-107">A value of PT0S will enable the task to run indefinitely.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

<span data-ttu-id="cd23a-108">**ExecutionTimeLimit** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="cd23a-108">The **ExecutionTimeLimit** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cd23a-109">父元素</span><span class="sxs-lookup"><span data-stu-id="cd23a-109">Parent element</span></span>



| <span data-ttu-id="cd23a-110">元素</span><span class="sxs-lookup"><span data-stu-id="cd23a-110">Element</span></span>                                                           | <span data-ttu-id="cd23a-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="cd23a-111">Derived from</span></span>                                                         | <span data-ttu-id="cd23a-112">Description</span><span class="sxs-lookup"><span data-stu-id="cd23a-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd23a-113">**設定**</span><span class="sxs-lookup"><span data-stu-id="cd23a-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="cd23a-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="cd23a-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="cd23a-115">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="cd23a-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cd23a-116">備註</span><span class="sxs-lookup"><span data-stu-id="cd23a-116">Remarks</span></span>

<span data-ttu-id="cd23a-117">針對 c + + 開發，請參閱 [**ITaskSettings 的 ExecutionTimeLimit 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit)。</span><span class="sxs-lookup"><span data-stu-id="cd23a-117">For C++ development, see [**ExecutionTimeLimit Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span></span>

<span data-ttu-id="cd23a-118">如需腳本開發，請參閱 [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md)。</span><span class="sxs-lookup"><span data-stu-id="cd23a-118">For script development, see [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd23a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd23a-119">Requirements</span></span>



| <span data-ttu-id="cd23a-120">需求</span><span class="sxs-lookup"><span data-stu-id="cd23a-120">Requirement</span></span> | <span data-ttu-id="cd23a-121">值</span><span class="sxs-lookup"><span data-stu-id="cd23a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd23a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd23a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd23a-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd23a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd23a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd23a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd23a-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd23a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd23a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd23a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd23a-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="cd23a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






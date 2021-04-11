---
title: 延遲 (bootTriggerType) 元素
description: 指定啟動系統與啟動工作之間的時間長度。
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
keywords:
- Delay 元素工作排程器
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935113"
---
# <a name="delay-boottriggertype-element"></a><span data-ttu-id="3ae7b-104">延遲 (bootTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="3ae7b-104">Delay (bootTriggerType) Element</span></span>

<span data-ttu-id="3ae7b-105">指定啟動系統與啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="3ae7b-105">Specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="3ae7b-106">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="3ae7b-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="3ae7b-107">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="3ae7b-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="3ae7b-108">**Delay** 元素是由 [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="3ae7b-108">The **Delay** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3ae7b-109">父元素</span><span class="sxs-lookup"><span data-stu-id="3ae7b-109">Parent element</span></span>



| <span data-ttu-id="3ae7b-110">元素</span><span class="sxs-lookup"><span data-stu-id="3ae7b-110">Element</span></span>                                                                     | <span data-ttu-id="3ae7b-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="3ae7b-111">Derived from</span></span>                                                               | <span data-ttu-id="3ae7b-112">Description</span><span class="sxs-lookup"><span data-stu-id="3ae7b-112">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="3ae7b-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="3ae7b-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md) | [<span data-ttu-id="3ae7b-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3ae7b-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md) | <span data-ttu-id="3ae7b-115">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3ae7b-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3ae7b-116">備註</span><span class="sxs-lookup"><span data-stu-id="3ae7b-116">Remarks</span></span>

<span data-ttu-id="3ae7b-117">針對腳本開發，事件觸發程式延遲是由 [**BootTrigger**](boottrigger-delay.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="3ae7b-117">For script development, the event trigger delay is specified by the [**BootTrigger.Delay**](boottrigger-delay.md) property.</span></span>

<span data-ttu-id="3ae7b-118">針對 c + + 開發，事件觸發程式延遲是由 [**IBootTrigger：:D elay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="3ae7b-118">For C++ development, the event trigger delay is specified by the [**IBootTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae7b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ae7b-119">Requirements</span></span>



| <span data-ttu-id="3ae7b-120">需求</span><span class="sxs-lookup"><span data-stu-id="3ae7b-120">Requirement</span></span> | <span data-ttu-id="3ae7b-121">值</span><span class="sxs-lookup"><span data-stu-id="3ae7b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ae7b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ae7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae7b-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ae7b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ae7b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ae7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae7b-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ae7b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ae7b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ae7b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae7b-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="3ae7b-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3ae7b-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="3ae7b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






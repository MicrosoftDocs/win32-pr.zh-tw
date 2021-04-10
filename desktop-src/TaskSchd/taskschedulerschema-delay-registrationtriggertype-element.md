---
title: 延遲 (registrationTriggerType) 元素
description: 指定在註冊工作與啟動工作之間的時間長度。
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686567"
---
# <a name="delay-registrationtriggertype-element"></a><span data-ttu-id="9ed67-104">延遲 (registrationTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="9ed67-104">Delay (registrationTriggerType) Element</span></span>

<span data-ttu-id="9ed67-105">指定在註冊工作與啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9ed67-105">Specifies the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="9ed67-106">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="9ed67-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="9ed67-107">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="9ed67-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="9ed67-108">**Delay** 元素是由 [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="9ed67-108">The **Delay** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9ed67-109">父元素</span><span class="sxs-lookup"><span data-stu-id="9ed67-109">Parent element</span></span>



| <span data-ttu-id="9ed67-110">元素</span><span class="sxs-lookup"><span data-stu-id="9ed67-110">Element</span></span>                                                                                     | <span data-ttu-id="9ed67-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="9ed67-111">Derived from</span></span>                                                                               | <span data-ttu-id="9ed67-112">Description</span><span class="sxs-lookup"><span data-stu-id="9ed67-112">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="9ed67-113">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="9ed67-113">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="9ed67-114">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9ed67-114">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="9ed67-115">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="9ed67-115">Specifies a trigger that starts a task when the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9ed67-116">備註</span><span class="sxs-lookup"><span data-stu-id="9ed67-116">Remarks</span></span>

<span data-ttu-id="9ed67-117">針對開發腳本，會使用 [**RegistrationTrigger 的 delay**](registrationtrigger-delay.md) 屬性指定註冊觸發程式延遲。</span><span class="sxs-lookup"><span data-stu-id="9ed67-117">For scripting development, the registration trigger delay is specified using the [**RegistrationTrigger.Delay**](registrationtrigger-delay.md) property.</span></span>

<span data-ttu-id="9ed67-118">針對 c + + 開發，會使用 [**IRegistrationTrigger：:D elay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) 屬性指定註冊觸發程式延遲。</span><span class="sxs-lookup"><span data-stu-id="9ed67-118">For C++ development, the registration trigger delay is specified using the [**IRegistrationTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9ed67-119">範例</span><span class="sxs-lookup"><span data-stu-id="9ed67-119">Examples</span></span>

<span data-ttu-id="9ed67-120">下列 XML 定義的註冊觸發程式延遲，可在工作註冊的時間與工作啟動的時間之間有5分鐘的延遲。</span><span class="sxs-lookup"><span data-stu-id="9ed67-120">The following XML defines a registration trigger delay that allows a 5 minute delay between when the task is registered and when the task is started.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="9ed67-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ed67-121">Requirements</span></span>



| <span data-ttu-id="9ed67-122">需求</span><span class="sxs-lookup"><span data-stu-id="9ed67-122">Requirement</span></span> | <span data-ttu-id="9ed67-123">值</span><span class="sxs-lookup"><span data-stu-id="9ed67-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9ed67-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ed67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed67-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ed67-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9ed67-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ed67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed67-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ed67-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ed67-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ed67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed67-129">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="9ed67-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9ed67-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="9ed67-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






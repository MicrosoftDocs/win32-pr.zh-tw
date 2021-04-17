---
title: 延遲 (logonTriggerType) 元素
description: 使用者登入和工作啟動時間之間的時間量。
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
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
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466765"
---
# <a name="delay-logontriggertype-element"></a><span data-ttu-id="37ebe-104">延遲 (logonTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="37ebe-104">Delay (logonTriggerType) Element</span></span>

<span data-ttu-id="37ebe-105">使用者登入和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="37ebe-105">Amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="37ebe-106">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="37ebe-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="37ebe-107">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="37ebe-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="37ebe-108">**Delay** 元素是由 [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="37ebe-108">The **Delay** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="37ebe-109">父元素</span><span class="sxs-lookup"><span data-stu-id="37ebe-109">Parent element</span></span>



| <span data-ttu-id="37ebe-110">元素</span><span class="sxs-lookup"><span data-stu-id="37ebe-110">Element</span></span>                                                                       | <span data-ttu-id="37ebe-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="37ebe-111">Derived from</span></span>                                                                 | <span data-ttu-id="37ebe-112">Description</span><span class="sxs-lookup"><span data-stu-id="37ebe-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="37ebe-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ebe-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="37ebe-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="37ebe-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="37ebe-115">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="37ebe-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="37ebe-116">備註</span><span class="sxs-lookup"><span data-stu-id="37ebe-116">Remarks</span></span>

<span data-ttu-id="37ebe-117">針對腳本開發，登入觸發程式延遲是使用 [**LogonTrigger**](logontrigger-delay.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="37ebe-117">For scripting development, the logon trigger delay is specified using the [**LogonTrigger.Delay**](logontrigger-delay.md) property.</span></span>

<span data-ttu-id="37ebe-118">針對 c + + 開發，登入觸發程式的使用者識別碼會使用 [**ILogonTrigger：:D elay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="37ebe-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ebe-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="37ebe-119">Requirements</span></span>



| <span data-ttu-id="37ebe-120">需求</span><span class="sxs-lookup"><span data-stu-id="37ebe-120">Requirement</span></span> | <span data-ttu-id="37ebe-121">值</span><span class="sxs-lookup"><span data-stu-id="37ebe-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37ebe-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37ebe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="37ebe-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37ebe-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37ebe-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37ebe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="37ebe-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37ebe-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37ebe-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37ebe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ebe-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="37ebe-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="37ebe-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="37ebe-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






---
title: ValueQueries (eventTriggerType) 元素
description: 包含一系列的元素，其中每個專案都包含名稱和 XPath 查詢值。
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- ValueQueries 元素工作排程器
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934068"
---
# <a name="valuequeries-eventtriggertype-element"></a><span data-ttu-id="7501e-104">ValueQueries (eventTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="7501e-104">ValueQueries (eventTriggerType) Element</span></span>

<span data-ttu-id="7501e-105">包含一系列的元素，其中每個專案都包含名稱和 XPath 查詢值。</span><span class="sxs-lookup"><span data-stu-id="7501e-105">Contains a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="7501e-106">查詢會套用至從 [**訂**](taskschedulerschema-subscription-eventtriggertype-element.md) 用帳戶元素中指定之事件訂閱傳回的事件。</span><span class="sxs-lookup"><span data-stu-id="7501e-106">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="7501e-107">XPath 查詢值的名稱可用來做為工作的 [動作] 區段中的變數。</span><span class="sxs-lookup"><span data-stu-id="7501e-107">The name for the XPath query value can be used as a variable in the action section of a task.</span></span>

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

<span data-ttu-id="7501e-108">**ValueQueries** 元素是由 [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="7501e-108">The **ValueQueries** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7501e-109">父元素</span><span class="sxs-lookup"><span data-stu-id="7501e-109">Parent element</span></span>



| <span data-ttu-id="7501e-110">元素</span><span class="sxs-lookup"><span data-stu-id="7501e-110">Element</span></span>                                                                                      | <span data-ttu-id="7501e-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="7501e-111">Derived from</span></span>                                                                 | <span data-ttu-id="7501e-112">Description</span><span class="sxs-lookup"><span data-stu-id="7501e-112">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="7501e-113">**EventTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="7501e-113">**EventTrigger (triggerGroup)**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="7501e-114">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="7501e-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="7501e-115">指定在發生系統事件時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7501e-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7501e-116">備註</span><span class="sxs-lookup"><span data-stu-id="7501e-116">Remarks</span></span>

<span data-ttu-id="7501e-117">針對 c + + 開發，請參閱 [**IEventTrigger 的 ValueQueries 屬性**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries)。</span><span class="sxs-lookup"><span data-stu-id="7501e-117">For C++ development, see [**ValueQueries Property of IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span></span>

<span data-ttu-id="7501e-118">如需腳本開發，請參閱 [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md)。</span><span class="sxs-lookup"><span data-stu-id="7501e-118">For script development, see [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7501e-119">範例</span><span class="sxs-lookup"><span data-stu-id="7501e-119">Examples</span></span>

<span data-ttu-id="7501e-120">如需使用此專案指定事件觸發程式之工作的完整 XML 範例，請參閱 [事件觸發程式範例 (XML) ](/previous-versions//aa446889(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7501e-120">For a complete example of the XML for a task that specifies a an event trigger using this element, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="7501e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7501e-121">Requirements</span></span>



| <span data-ttu-id="7501e-122">需求</span><span class="sxs-lookup"><span data-stu-id="7501e-122">Requirement</span></span> | <span data-ttu-id="7501e-123">值</span><span class="sxs-lookup"><span data-stu-id="7501e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7501e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7501e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7501e-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7501e-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7501e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7501e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7501e-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7501e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 


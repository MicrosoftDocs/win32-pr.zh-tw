---
title: 值 (namedValues) 元素
description: 包含與名稱/值配對中的名稱相關聯的值。
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- 值元素工作排程器
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686362"
---
# <a name="value-namedvalues-element"></a><span data-ttu-id="d2af5-104">值 (namedValues) 元素</span><span class="sxs-lookup"><span data-stu-id="d2af5-104">Value (namedValues) Element</span></span>

<span data-ttu-id="d2af5-105">包含與名稱/值配對中的名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="d2af5-105">Contains the value that is associated with a name in a name-value pair.</span></span>

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

<span data-ttu-id="d2af5-106">**Value** 元素是由 [**namedValues**](taskschedulerschema-namedvalues-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="d2af5-106">The **Value** element is defined by the [**namedValues**](taskschedulerschema-namedvalues-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d2af5-107">父元素</span><span class="sxs-lookup"><span data-stu-id="d2af5-107">Parent element</span></span>



| <span data-ttu-id="d2af5-108">元素</span><span class="sxs-lookup"><span data-stu-id="d2af5-108">Element</span></span>                                                                                              | <span data-ttu-id="d2af5-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="d2af5-109">Derived from</span></span>                                                       | <span data-ttu-id="d2af5-110">Description</span><span class="sxs-lookup"><span data-stu-id="d2af5-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2af5-111">**ValueQueries (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="d2af5-111">**ValueQueries (eventTriggerType)**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="d2af5-112">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="d2af5-112">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md) | <span data-ttu-id="d2af5-113">指定命名的 XPath 查詢集合。</span><span class="sxs-lookup"><span data-stu-id="d2af5-113">Specifies a collection of named XPath queries.</span></span> <span data-ttu-id="d2af5-114">集合中的每個查詢都會套用至從 [**訂**](taskschedulerschema-subscription-eventtriggertype-element.md) 用帳戶元素中指定之訂閱查詢傳回的最後一個相符事件 XML。</span><span class="sxs-lookup"><span data-stu-id="d2af5-114">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="d2af5-115">查詢的名稱可以當做 ShowMessage 動作訊息中的變數使用。</span><span class="sxs-lookup"><span data-stu-id="d2af5-115">The name of the query can be used as a variable in the message of a ShowMessage action.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d2af5-116">備註</span><span class="sxs-lookup"><span data-stu-id="d2af5-116">Remarks</span></span>

<span data-ttu-id="d2af5-117">針對 c + + 開發，請參閱 [**ITaskNamedValuePair 的 Value 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value)。</span><span class="sxs-lookup"><span data-stu-id="d2af5-117">For C++ development, see [**Value Property of ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span></span>

<span data-ttu-id="d2af5-118">如需腳本開發，請參閱 [**TaskNamedValuePair。**](tasknamedvaluepair-value.md)</span><span class="sxs-lookup"><span data-stu-id="d2af5-118">For script development, see [**TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2af5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2af5-119">Requirements</span></span>



| <span data-ttu-id="d2af5-120">需求</span><span class="sxs-lookup"><span data-stu-id="d2af5-120">Requirement</span></span> | <span data-ttu-id="d2af5-121">值</span><span class="sxs-lookup"><span data-stu-id="d2af5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d2af5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2af5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2af5-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2af5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d2af5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2af5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2af5-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2af5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






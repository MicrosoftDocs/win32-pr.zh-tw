---
title: UserId (logonTriggerType) 元素
description: 使用者的識別碼。 此工作會在此使用者登入電腦時啟動。
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- UserId 元素工作排程器
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509439"
---
# <a name="userid-logontriggertype-element"></a><span data-ttu-id="60c19-105">UserId (logonTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="60c19-105">UserId (logonTriggerType) Element</span></span>

<span data-ttu-id="60c19-106">使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="60c19-106">Identifier of the user.</span></span> <span data-ttu-id="60c19-107">此工作會在此使用者登入電腦時啟動。</span><span class="sxs-lookup"><span data-stu-id="60c19-107">The task is started when this user logs on to the computer.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="60c19-108">**UserId** 元素是由 [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="60c19-108">The **UserId** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="60c19-109">父元素</span><span class="sxs-lookup"><span data-stu-id="60c19-109">Parent element</span></span>



| <span data-ttu-id="60c19-110">元素</span><span class="sxs-lookup"><span data-stu-id="60c19-110">Element</span></span>                                                                       | <span data-ttu-id="60c19-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="60c19-111">Derived from</span></span>                                                                 | <span data-ttu-id="60c19-112">Description</span><span class="sxs-lookup"><span data-stu-id="60c19-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="60c19-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="60c19-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="60c19-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60c19-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="60c19-115">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="60c19-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="60c19-116">備註</span><span class="sxs-lookup"><span data-stu-id="60c19-116">Remarks</span></span>

<span data-ttu-id="60c19-117">針對腳本開發，登入觸發程式的使用者識別碼是使用 [**LogonTrigger**](logontrigger-userid.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="60c19-117">For scripting development, the user identifier for the logon trigger is specified using the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span>

<span data-ttu-id="60c19-118">針對 c + + 開發，使用 [**ILogonTrigger：： UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) 屬性指定登入觸發程式的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="60c19-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="60c19-119">範例</span><span class="sxs-lookup"><span data-stu-id="60c19-119">Examples</span></span>

<span data-ttu-id="60c19-120">如需指定登入觸發程式之工作的完整 XML 範例，請參閱 [登入觸發程式範例 (xml) ](logon-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="60c19-120">For a complete example of the XML for a task that specifies a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60c19-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="60c19-121">Requirements</span></span>



| <span data-ttu-id="60c19-122">需求</span><span class="sxs-lookup"><span data-stu-id="60c19-122">Requirement</span></span> | <span data-ttu-id="60c19-123">值</span><span class="sxs-lookup"><span data-stu-id="60c19-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60c19-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60c19-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60c19-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60c19-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60c19-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60c19-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60c19-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60c19-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60c19-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60c19-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c19-129">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="60c19-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="60c19-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="60c19-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






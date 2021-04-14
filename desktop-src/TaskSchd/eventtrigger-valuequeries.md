---
title: EventTrigger. ValueQueries 屬性
description: 針對腳本，取得或設定命名 XPath 查詢的集合。 集合中的每個查詢都會套用至訂閱屬性中指定之訂閱查詢所傳回的最後一個相符事件 XML。
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- ValueQueries 屬性工作排程器
- ValueQueries 屬性工作排程器，EventTrigger 物件
- EventTrigger 物件工作排程器、ValueQueries 屬性
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509063"
---
# <a name="eventtriggervaluequeries-property"></a><span data-ttu-id="95d3e-107">EventTrigger. ValueQueries 屬性</span><span class="sxs-lookup"><span data-stu-id="95d3e-107">EventTrigger.ValueQueries property</span></span>

<span data-ttu-id="95d3e-108">針對腳本，取得或設定命名 XPath 查詢的集合。</span><span class="sxs-lookup"><span data-stu-id="95d3e-108">For scripting, gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="95d3e-109">集合中的每個查詢都會套用至 [**訂閱**](eventtrigger-subscription.md) 屬性中指定之訂閱查詢所傳回的最後一個相符事件 XML。</span><span class="sxs-lookup"><span data-stu-id="95d3e-109">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d3e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="95d3e-110">Syntax</span></span>


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a><span data-ttu-id="95d3e-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="95d3e-111">Property value</span></span>

<span data-ttu-id="95d3e-112">成對名稱/值的集合。</span><span class="sxs-lookup"><span data-stu-id="95d3e-112">A collection of of name-value pairs.</span></span> <span data-ttu-id="95d3e-113">集合中的每個名稱/值組都會針對觸發事件觸發程式的事件，定義其屬性值的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="95d3e-113">Each name-value pair in the collection defines a unique name for a property value of the event that triggers the event trigger.</span></span> <span data-ttu-id="95d3e-114">事件的屬性值會定義為 XPath 事件查詢。</span><span class="sxs-lookup"><span data-stu-id="95d3e-114">The property value of the event is defined as an XPath event query.</span></span> <span data-ttu-id="95d3e-115">如需有關 XPath 事件查詢的詳細資訊，請參閱 [事件選取](/previous-versions//aa385231(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="95d3e-115">For more information about XPath event queries, see [Event Selection](/previous-versions//aa385231(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="95d3e-116">備註</span><span class="sxs-lookup"><span data-stu-id="95d3e-116">Remarks</span></span>

<span data-ttu-id="95d3e-117">查詢的名稱可以當做下列動作屬性中的變數使用：</span><span class="sxs-lookup"><span data-stu-id="95d3e-117">The name of the query can be used as a variable in the following action properties:</span></span>

-   [<span data-ttu-id="95d3e-118">**ShowMessageAction. MessageBody**</span><span class="sxs-lookup"><span data-stu-id="95d3e-118">**ShowMessageAction.MessageBody**</span></span>](showmessageaction-messagebody.md)
-   [<span data-ttu-id="95d3e-119">**ShowMessageAction 標題**</span><span class="sxs-lookup"><span data-stu-id="95d3e-119">**ShowMessageAction.Title**</span></span>](showmessageaction-title.md)
-   [<span data-ttu-id="95d3e-120">**ExecAction. 引數**</span><span class="sxs-lookup"><span data-stu-id="95d3e-120">**ExecAction.Arguments**</span></span>](execaction-arguments.md)
-   [<span data-ttu-id="95d3e-121">**ExecAction. WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="95d3e-121">**ExecAction.WorkingDirectory**</span></span>](execaction-workingdirectory.md)
-   [<span data-ttu-id="95d3e-122">**EmailAction 伺服器**</span><span class="sxs-lookup"><span data-stu-id="95d3e-122">**EmailAction.Server**</span></span>](emailaction-server.md)
-   [<span data-ttu-id="95d3e-123">**EmailAction 主題**</span><span class="sxs-lookup"><span data-stu-id="95d3e-123">**EmailAction.Subject**</span></span>](emailaction-subject.md)
-   [<span data-ttu-id="95d3e-124">**EmailAction.To**</span><span class="sxs-lookup"><span data-stu-id="95d3e-124">**EmailAction.To**</span></span>](emailaction-to.md)
-   [<span data-ttu-id="95d3e-125">**EmailAction.Cc**</span><span class="sxs-lookup"><span data-stu-id="95d3e-125">**EmailAction.Cc**</span></span>](emailaction-cc.md)
-   [<span data-ttu-id="95d3e-126">**EmailAction 密件副本**</span><span class="sxs-lookup"><span data-stu-id="95d3e-126">**EmailAction.Bcc**</span></span>](emailaction-bcc.md)
-   [<span data-ttu-id="95d3e-127">**EmailAction ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="95d3e-127">**EmailAction.ReplyTo**</span></span>](emailaction-replyto.md)
-   [<span data-ttu-id="95d3e-128">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="95d3e-128">**EmailAction.From**</span></span>](emailaction-from.md)
-   [<span data-ttu-id="95d3e-129">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="95d3e-129">**EmailAction.Body**</span></span>](emailaction-body.md)
-   [<span data-ttu-id="95d3e-130">**ComHandlerAction 資料**</span><span class="sxs-lookup"><span data-stu-id="95d3e-130">**ComHandlerAction.Data**</span></span>](comhandleraction-data.md)

<span data-ttu-id="95d3e-131">下列程式碼範例字串顯示可用於名稱/值集合中的兩個名稱值組。</span><span class="sxs-lookup"><span data-stu-id="95d3e-131">The following code example strings show two name value pairs that can be used in a name-value collection.</span></span> <span data-ttu-id="95d3e-132">XPath 查詢所傳回的值可以取代動作屬性中的變數。</span><span class="sxs-lookup"><span data-stu-id="95d3e-132">The values returned by the XPath queries can replace variables in an action's property.</span></span> <span data-ttu-id="95d3e-133">在 `$(user)` [動作] 屬性中，以 and 的名稱參考這些值 `$(machine)` 。</span><span class="sxs-lookup"><span data-stu-id="95d3e-133">The values are referenced by name, with `$(user)` and `$(machine)`, in the action property.</span></span> <span data-ttu-id="95d3e-134">例如，如果在 `$(user)` `$(machine)` [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) 字串中使用和變數，則 XPath 查詢的值會取代字串中的變數。</span><span class="sxs-lookup"><span data-stu-id="95d3e-134">For example, if the `$(user)` and `$(machine)` variables are used in the [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) string, then the value of the XPath queries will replace the variables in the string.</span></span>

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

<span data-ttu-id="95d3e-135">如需針對特定事件撰寫查詢字串的詳細資訊，請參閱 [事件選取](/previous-versions//aa385231(v=vs.85)) 和 [訂閱事件](../wes/subscribing-to-events.md)。</span><span class="sxs-lookup"><span data-stu-id="95d3e-135">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95d3e-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="95d3e-136">Requirements</span></span>



| <span data-ttu-id="95d3e-137">需求</span><span class="sxs-lookup"><span data-stu-id="95d3e-137">Requirement</span></span> | <span data-ttu-id="95d3e-138">值</span><span class="sxs-lookup"><span data-stu-id="95d3e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95d3e-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95d3e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="95d3e-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95d3e-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="95d3e-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95d3e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="95d3e-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95d3e-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95d3e-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="95d3e-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="95d3e-144"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="95d3e-144"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="95d3e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="95d3e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d3e-146"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d3e-146"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d3e-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95d3e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d3e-148">工作排程器</span><span class="sxs-lookup"><span data-stu-id="95d3e-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="95d3e-149">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="95d3e-149">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 


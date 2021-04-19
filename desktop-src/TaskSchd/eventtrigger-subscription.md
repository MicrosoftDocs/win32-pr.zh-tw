---
title: EventTrigger. 訂用帳戶屬性
description: 針對腳本，取得或設定查詢字串，以識別引發觸發程式的事件。
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- 訂用帳戶屬性工作排程器
- 訂用帳戶屬性工作排程器，EventTrigger 物件
- EventTrigger 物件工作排程器，訂用帳戶屬性
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968192"
---
# <a name="eventtriggersubscription-property"></a><span data-ttu-id="caa39-106">EventTrigger. 訂用帳戶屬性</span><span class="sxs-lookup"><span data-stu-id="caa39-106">EventTrigger.Subscription property</span></span>

<span data-ttu-id="caa39-107">針對腳本，取得或設定查詢字串，以識別引發觸發程式的事件。</span><span class="sxs-lookup"><span data-stu-id="caa39-107">For scripting, gets or sets a query string that identifies the event that fires the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="caa39-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="caa39-108">Syntax</span></span>


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a><span data-ttu-id="caa39-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="caa39-109">Property value</span></span>

<span data-ttu-id="caa39-110">識別引發觸發程式之事件的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="caa39-110">A query string that identifies the event that fires the trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa39-111">備註</span><span class="sxs-lookup"><span data-stu-id="caa39-111">Remarks</span></span>

<span data-ttu-id="caa39-112">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**訂閱**](taskschedulerschema-subscription-eventtriggertype-element.md) 元素來指定事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="caa39-112">When reading or writing your own XML for a task, the event subscription is specified using the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="caa39-113">如需針對特定事件撰寫查詢字串的詳細資訊，請參閱 [事件選取](/previous-versions//aa385231(v=vs.85)) 和 [訂閱事件](../wes/subscribing-to-events.md)。</span><span class="sxs-lookup"><span data-stu-id="caa39-113">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="examples"></a><span data-ttu-id="caa39-114">範例</span><span class="sxs-lookup"><span data-stu-id="caa39-114">Examples</span></span>

<span data-ttu-id="caa39-115">下列查詢字串會定義系統通道中所有層級2事件的訂用帳戶：</span><span class="sxs-lookup"><span data-stu-id="caa39-115">The following query string defines a subscription to all level 2 events in the System channel:</span></span>


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a><span data-ttu-id="caa39-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="caa39-116">Requirements</span></span>



| <span data-ttu-id="caa39-117">需求</span><span class="sxs-lookup"><span data-stu-id="caa39-117">Requirement</span></span> | <span data-ttu-id="caa39-118">值</span><span class="sxs-lookup"><span data-stu-id="caa39-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="caa39-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caa39-119">Minimum supported client</span></span><br/> | <span data-ttu-id="caa39-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caa39-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="caa39-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caa39-121">Minimum supported server</span></span><br/> | <span data-ttu-id="caa39-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caa39-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="caa39-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="caa39-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="caa39-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="caa39-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="caa39-125">DLL</span><span class="sxs-lookup"><span data-stu-id="caa39-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caa39-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caa39-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caa39-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caa39-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa39-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="caa39-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="caa39-129">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="caa39-129">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 


---
title: actionGroup 群組
description: 定義工作可執行檔動作群組。
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- actionGroup 群組工作排程器
- actionGroup 工作排程器
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685741"
---
# <a name="actiongroup-group"></a><span data-ttu-id="8f6ad-105">actionGroup 群組</span><span class="sxs-lookup"><span data-stu-id="8f6ad-105">actionGroup Group</span></span>

<span data-ttu-id="8f6ad-106">定義工作可執行檔動作群組。</span><span class="sxs-lookup"><span data-stu-id="8f6ad-106">Defines the group of actions that a task can perform.</span></span>

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="8f6ad-107">子元素</span><span class="sxs-lookup"><span data-stu-id="8f6ad-107">Child elements</span></span>



| <span data-ttu-id="8f6ad-108">元素</span><span class="sxs-lookup"><span data-stu-id="8f6ad-108">Element</span></span>                                                                    | <span data-ttu-id="8f6ad-109">類型</span><span class="sxs-lookup"><span data-stu-id="8f6ad-109">Type</span></span>                                                                       | <span data-ttu-id="8f6ad-110">Description</span><span class="sxs-lookup"><span data-stu-id="8f6ad-110">Description</span></span>                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="8f6ad-111">**ComHandler**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="8f6ad-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="8f6ad-113">表示引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="8f6ad-113">Represents an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="8f6ad-114">**Exec**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-114">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="8f6ad-115">**execType**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-115">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="8f6ad-116">表示執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="8f6ad-116">Represents an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="8f6ad-117">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-117">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="8f6ad-118">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-118">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="8f6ad-119">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="8f6ad-119">Represents an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="8f6ad-120">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-120">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="8f6ad-121">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="8f6ad-121">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="8f6ad-122">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="8f6ad-122">Represents an action that shows a message box.</span></span><br/>               |



## <a name="remarks"></a><span data-ttu-id="8f6ad-123">備註</span><span class="sxs-lookup"><span data-stu-id="8f6ad-123">Remarks</span></span>

<span data-ttu-id="8f6ad-124">讀取或寫入 XML 時，此群組所定義的元素是 [**Actions**](taskschedulerschema-actions-tasktype-element.md) 元素的子項目。</span><span class="sxs-lookup"><span data-stu-id="8f6ad-124">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6ad-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f6ad-125">Requirements</span></span>



| <span data-ttu-id="8f6ad-126">需求</span><span class="sxs-lookup"><span data-stu-id="8f6ad-126">Requirement</span></span> | <span data-ttu-id="8f6ad-127">值</span><span class="sxs-lookup"><span data-stu-id="8f6ad-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f6ad-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f6ad-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8f6ad-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f6ad-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f6ad-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f6ad-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8f6ad-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f6ad-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f6ad-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f6ad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6ad-133">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8f6ad-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






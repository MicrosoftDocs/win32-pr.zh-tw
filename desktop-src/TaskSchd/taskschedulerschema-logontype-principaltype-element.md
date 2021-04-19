---
title: LogonType (principalType) 元素
description: 指定執行與主體相關聯之工作所需的安全性登入方法。
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- LogonType 元素工作排程器
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969761"
---
# <a name="logontype-principaltype-element"></a><span data-ttu-id="ea494-104">LogonType (principalType) 元素</span><span class="sxs-lookup"><span data-stu-id="ea494-104">LogonType (principalType) Element</span></span>

<span data-ttu-id="ea494-105">指定執行與主體相關聯之工作所需的安全性登入方法。</span><span class="sxs-lookup"><span data-stu-id="ea494-105">Specifies the security logon method required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

<span data-ttu-id="ea494-106">**LogonType** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="ea494-106">The **LogonType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ea494-107">父元素</span><span class="sxs-lookup"><span data-stu-id="ea494-107">Parent element</span></span>



| <span data-ttu-id="ea494-108">元素</span><span class="sxs-lookup"><span data-stu-id="ea494-108">Element</span></span>                                                                  | <span data-ttu-id="ea494-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="ea494-109">Derived from</span></span>                                                           | <span data-ttu-id="ea494-110">Description</span><span class="sxs-lookup"><span data-stu-id="ea494-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ea494-111">**主要**</span><span class="sxs-lookup"><span data-stu-id="ea494-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="ea494-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="ea494-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="ea494-113">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="ea494-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ea494-114">備註</span><span class="sxs-lookup"><span data-stu-id="ea494-114">Remarks</span></span>

<span data-ttu-id="ea494-115">**LogonType** 元素和 [**UserId**](taskschedulerschema-userid-principaltype-element.md)元素會一起使用，以定義執行使用此主體之工作所需的使用者。</span><span class="sxs-lookup"><span data-stu-id="ea494-115">The **LogonType** element and the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="ea494-116">針對腳本開發，主體的登入類型是由 [**LogonType**](principal-logontype.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="ea494-116">For scripting development, the logon type for the principal is specified by the [**Principal.LogonType**](principal-logontype.md) property.</span></span>

<span data-ttu-id="ea494-117">針對 c + + 開發，主體的登入類型是由 [**IPrincipal：： LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="ea494-117">For C++ development, the logon type for the principal is specified by the [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) property.</span></span>

<span data-ttu-id="ea494-118">此元素 (由 [**logonType**](taskschedulerschema-logontype-simpletype.md) 簡單類型定義) 必須具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ea494-118">This element (defined by the [**logonType**](taskschedulerschema-logontype-simpletype.md) simple type) must have one of the following values.</span></span>

-   <span data-ttu-id="ea494-119">S4U：使用者必須使用服務登入使用者 (S4U) 登入。</span><span class="sxs-lookup"><span data-stu-id="ea494-119">S4U: User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="ea494-120">使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密檔案。</span><span class="sxs-lookup"><span data-stu-id="ea494-120">When an S4U logon is used, no password is stored by the system and there is no access to the network or encrypted files.</span></span>
-   <span data-ttu-id="ea494-121">密碼：使用者必須使用密碼登入。</span><span class="sxs-lookup"><span data-stu-id="ea494-121">Password: User must log on using a password.</span></span>
-   <span data-ttu-id="ea494-122">InteractiveToken：使用者必須已經登入。</span><span class="sxs-lookup"><span data-stu-id="ea494-122">InteractiveToken: User must already be logged on.</span></span> <span data-ttu-id="ea494-123">此工作只會在現有的互動式會話中執行。</span><span class="sxs-lookup"><span data-stu-id="ea494-123">The task will be run only in an existing interactive session.</span></span>

<span data-ttu-id="ea494-124">對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="ea494-124">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="ea494-125">若要將工作登入類型設定為互動式，請在工作主體的元素中指定 **InteractiveToken** **<LogonType>** 。</span><span class="sxs-lookup"><span data-stu-id="ea494-125">To set the task logon type to be interactive, specify **InteractiveToken** in the **<LogonType>** element of the task principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea494-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea494-126">Requirements</span></span>



| <span data-ttu-id="ea494-127">需求</span><span class="sxs-lookup"><span data-stu-id="ea494-127">Requirement</span></span> | <span data-ttu-id="ea494-128">值</span><span class="sxs-lookup"><span data-stu-id="ea494-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ea494-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea494-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ea494-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea494-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ea494-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea494-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ea494-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea494-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea494-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea494-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea494-134">工作排程器</span><span class="sxs-lookup"><span data-stu-id="ea494-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






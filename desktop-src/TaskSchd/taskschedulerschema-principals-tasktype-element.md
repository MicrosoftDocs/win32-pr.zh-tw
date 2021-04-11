---
title: 主體 (taskType) 元素
description: 指定可以用來執行工作的安全性內容。
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- 主體元素工作排程器
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934014"
---
# <a name="principals-tasktype-element"></a><span data-ttu-id="10022-104">主體 (taskType) 元素</span><span class="sxs-lookup"><span data-stu-id="10022-104">Principals (taskType) Element</span></span>

<span data-ttu-id="10022-105">指定可以用來執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="10022-105">Specifies the security contexts that can be used to run the task.</span></span>

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

<span data-ttu-id="10022-106">**主體** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="10022-106">The **Principals** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="10022-107">父元素</span><span class="sxs-lookup"><span data-stu-id="10022-107">Parent element</span></span>



| <span data-ttu-id="10022-108">元素</span><span class="sxs-lookup"><span data-stu-id="10022-108">Element</span></span>                                          | <span data-ttu-id="10022-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="10022-109">Derived from</span></span>                                                 | <span data-ttu-id="10022-110">Description</span><span class="sxs-lookup"><span data-stu-id="10022-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="10022-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="10022-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="10022-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="10022-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="10022-113">定義工作排程器服務所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="10022-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="10022-114">子元素</span><span class="sxs-lookup"><span data-stu-id="10022-114">Child elements</span></span>



| <span data-ttu-id="10022-115">元素</span><span class="sxs-lookup"><span data-stu-id="10022-115">Element</span></span>                                                                  | <span data-ttu-id="10022-116">類型</span><span class="sxs-lookup"><span data-stu-id="10022-116">Type</span></span>                                                                   | <span data-ttu-id="10022-117">Description</span><span class="sxs-lookup"><span data-stu-id="10022-117">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="10022-118">**主要**</span><span class="sxs-lookup"><span data-stu-id="10022-118">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="10022-119">**principalType**</span><span class="sxs-lookup"><span data-stu-id="10022-119">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="10022-120">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="10022-120">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="10022-121">備註</span><span class="sxs-lookup"><span data-stu-id="10022-121">Remarks</span></span>

<span data-ttu-id="10022-122">您最多可以為工作指定32主體。</span><span class="sxs-lookup"><span data-stu-id="10022-122">You can specify up to 32 principals for a task.</span></span>

<span data-ttu-id="10022-123">針對開發腳本，工作的主體是使用 [**TaskDefinition**](taskdefinition-principal.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="10022-123">For scripting development, the principals of a task are specified using the [**TaskDefinition.Principal**](taskdefinition-principal.md) property.</span></span>

<span data-ttu-id="10022-124">針對 c + + 開發，工作的主體是使用 ITaskDefinition 的 [**Principal 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)來指定。</span><span class="sxs-lookup"><span data-stu-id="10022-124">For C++ development, the principals of a task are specified using the [**Principal property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span></span>

## <a name="examples"></a><span data-ttu-id="10022-125">範例</span><span class="sxs-lookup"><span data-stu-id="10022-125">Examples</span></span>

<span data-ttu-id="10022-126">下列 XML 會定義兩個主體：工作的使用者識別碼和群組識別碼主體。</span><span class="sxs-lookup"><span data-stu-id="10022-126">The following XML defines two principals: a user identifier and group identifier principal for the task.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="10022-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="10022-127">Requirements</span></span>



| <span data-ttu-id="10022-128">需求</span><span class="sxs-lookup"><span data-stu-id="10022-128">Requirement</span></span> | <span data-ttu-id="10022-129">值</span><span class="sxs-lookup"><span data-stu-id="10022-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="10022-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10022-130">Minimum supported client</span></span><br/> | <span data-ttu-id="10022-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10022-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10022-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10022-132">Minimum supported server</span></span><br/> | <span data-ttu-id="10022-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10022-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10022-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10022-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10022-135">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="10022-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="10022-136">工作排程器</span><span class="sxs-lookup"><span data-stu-id="10022-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






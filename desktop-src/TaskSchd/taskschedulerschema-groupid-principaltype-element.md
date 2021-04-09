---
title: GroupId (principalType) 元素
description: 指定執行與主體相關聯之工作所需之使用者群組的識別碼。
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- GroupId 元素工作排程器
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025359"
---
# <a name="groupid-principaltype-element"></a><span data-ttu-id="982c1-104">GroupId (principalType) 元素</span><span class="sxs-lookup"><span data-stu-id="982c1-104">GroupId (principalType) Element</span></span>

<span data-ttu-id="982c1-105">指定執行與主體相關聯之工作所需之使用者群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="982c1-105">Specifies the identifier of the user group required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="982c1-106">**GroupId** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="982c1-106">The **GroupId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="982c1-107">父元素</span><span class="sxs-lookup"><span data-stu-id="982c1-107">Parent element</span></span>



| <span data-ttu-id="982c1-108">元素</span><span class="sxs-lookup"><span data-stu-id="982c1-108">Element</span></span>                                                                  | <span data-ttu-id="982c1-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="982c1-109">Derived from</span></span>                                                           | <span data-ttu-id="982c1-110">Description</span><span class="sxs-lookup"><span data-stu-id="982c1-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="982c1-111">**主要**</span><span class="sxs-lookup"><span data-stu-id="982c1-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="982c1-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="982c1-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="982c1-113">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="982c1-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="982c1-114">備註</span><span class="sxs-lookup"><span data-stu-id="982c1-114">Remarks</span></span>

<span data-ttu-id="982c1-115">您無法同時指定群組識別碼和使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="982c1-115">You cannot specify a group identifier and a user identifier at the same time.</span></span> <span data-ttu-id="982c1-116">請指定 [**UserId**](taskschedulerschema-userid-principaltype-element.md) 或 **GroupId** 元素，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="982c1-116">Specify either the [**UserId**](taskschedulerschema-userid-principaltype-element.md) or **GroupId** elements, but not both.</span></span>

<span data-ttu-id="982c1-117">針對腳本開發，主體的群組識別碼是使用 [**principal. GroupId**](principal-groupid.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="982c1-117">For script development, the group identifier of the principal is specified using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="982c1-118">針對 c + + 開發，會使用 [**IPrincipal：： GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) 屬性指定主體的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="982c1-118">For C++ development, the group identifier of the principal is specified using the [**IPrincipal::GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="982c1-119">範例</span><span class="sxs-lookup"><span data-stu-id="982c1-119">Examples</span></span>

<span data-ttu-id="982c1-120">如需使用此專案之工作的 XML 完整範例，請參閱登入 [觸發程式範例 (xml) ](logon-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="982c1-120">For a complete example of the XML for a task that uses this element, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="982c1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="982c1-121">Requirements</span></span>



| <span data-ttu-id="982c1-122">需求</span><span class="sxs-lookup"><span data-stu-id="982c1-122">Requirement</span></span> | <span data-ttu-id="982c1-123">值</span><span class="sxs-lookup"><span data-stu-id="982c1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="982c1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="982c1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="982c1-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="982c1-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="982c1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="982c1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="982c1-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="982c1-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="982c1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="982c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="982c1-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="982c1-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






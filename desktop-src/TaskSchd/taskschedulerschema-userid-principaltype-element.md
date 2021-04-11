---
title: UserId (principalType) 元素
description: 指定執行與主體相關聯之工作所需的使用者識別碼。
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
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
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385274"
---
# <a name="userid-principaltype-element"></a><span data-ttu-id="207af-104">UserId (principalType) 元素</span><span class="sxs-lookup"><span data-stu-id="207af-104">UserId (principalType) Element</span></span>

<span data-ttu-id="207af-105">指定執行與主體相關聯之工作所需的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="207af-105">Specifies the user identifier required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="207af-106">**UserId** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="207af-106">The **UserId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="207af-107">父元素</span><span class="sxs-lookup"><span data-stu-id="207af-107">Parent element</span></span>



| <span data-ttu-id="207af-108">元素</span><span class="sxs-lookup"><span data-stu-id="207af-108">Element</span></span>                                                                  | <span data-ttu-id="207af-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="207af-109">Derived from</span></span>                                                           | <span data-ttu-id="207af-110">Description</span><span class="sxs-lookup"><span data-stu-id="207af-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="207af-111">**主要**</span><span class="sxs-lookup"><span data-stu-id="207af-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="207af-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="207af-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="207af-113">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="207af-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="207af-114">備註</span><span class="sxs-lookup"><span data-stu-id="207af-114">Remarks</span></span>

<span data-ttu-id="207af-115">**UserId** 元素和 [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)專案會一起使用，以定義執行使用此主體之工作所需的使用者。</span><span class="sxs-lookup"><span data-stu-id="207af-115">The **UserId** element and the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="207af-116">您無法同時指定使用者識別碼和群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="207af-116">You cannot specify a user identifier and a group identifier at the same time.</span></span> <span data-ttu-id="207af-117">請指定 **UserId** 或 [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) 元素，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="207af-117">Specify either the **UserId** or the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element, but not both.</span></span>

<span data-ttu-id="207af-118">針對腳本開發，使用者識別碼會使用 [**Principal. UserId**](principal-userid.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="207af-118">For scripting development, the user identifier is specified using the [**Principal.UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="207af-119">針對 c + + 開發，會使用 [**IPrincipal：： UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) 屬性指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="207af-119">For C++ development, the user identifier is specified using the [**IPrincipal::UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="207af-120">範例</span><span class="sxs-lookup"><span data-stu-id="207af-120">Examples</span></span>

<span data-ttu-id="207af-121">下列 XML 會使用使用者識別碼定義原則。</span><span class="sxs-lookup"><span data-stu-id="207af-121">The following XML defines a principle using a user identifier.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="207af-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="207af-122">Requirements</span></span>



| <span data-ttu-id="207af-123">需求</span><span class="sxs-lookup"><span data-stu-id="207af-123">Requirement</span></span> | <span data-ttu-id="207af-124">值</span><span class="sxs-lookup"><span data-stu-id="207af-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="207af-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="207af-125">Minimum supported client</span></span><br/> | <span data-ttu-id="207af-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="207af-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="207af-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="207af-127">Minimum supported server</span></span><br/> | <span data-ttu-id="207af-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="207af-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="207af-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="207af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207af-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="207af-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






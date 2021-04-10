---
title: RequiredPrivileges (requiredPrivilegesType) 元素
description: 指定工作所需的許可權。
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- RequiredPrivileges 元素工作排程器
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106355"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a><span data-ttu-id="95822-104">RequiredPrivileges (requiredPrivilegesType) 元素</span><span class="sxs-lookup"><span data-stu-id="95822-104">RequiredPrivileges (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="95822-105">指定工作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="95822-105">Specifies the privileges that are required by the task.</span></span>

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

<span data-ttu-id="95822-106">**RequiredPrivileges** 元素是由 [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="95822-106">The **RequiredPrivileges** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="95822-107">父元素</span><span class="sxs-lookup"><span data-stu-id="95822-107">Parent element</span></span>



| <span data-ttu-id="95822-108">元素</span><span class="sxs-lookup"><span data-stu-id="95822-108">Element</span></span>                                                                                  | <span data-ttu-id="95822-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="95822-109">Derived from</span></span>                                                           | <span data-ttu-id="95822-110">Description</span><span class="sxs-lookup"><span data-stu-id="95822-110">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="95822-111">**Principal (principalType)**</span><span class="sxs-lookup"><span data-stu-id="95822-111">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="95822-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="95822-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="95822-113">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="95822-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="95822-114">備註</span><span class="sxs-lookup"><span data-stu-id="95822-114">Remarks</span></span>

<span data-ttu-id="95822-115">針對 c + + 開發，這項資訊是透過 [**IPrincipal2：： RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="95822-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="95822-116">範例</span><span class="sxs-lookup"><span data-stu-id="95822-116">Examples</span></span>

<span data-ttu-id="95822-117">下列 XML 定義使用群組識別碼和必要的許可權。</span><span class="sxs-lookup"><span data-stu-id="95822-117">The following XML defines using a group identifier and the required privileges.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="95822-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="95822-118">Requirements</span></span>



| <span data-ttu-id="95822-119">需求</span><span class="sxs-lookup"><span data-stu-id="95822-119">Requirement</span></span> | <span data-ttu-id="95822-120">值</span><span class="sxs-lookup"><span data-stu-id="95822-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="95822-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95822-121">Minimum supported client</span></span><br/> | <span data-ttu-id="95822-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95822-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="95822-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95822-123">Minimum supported server</span></span><br/> | <span data-ttu-id="95822-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95822-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95822-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95822-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95822-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="95822-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






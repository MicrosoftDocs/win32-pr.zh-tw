---
title: 許可權 (requiredPrivilegesType) 元素
description: 指定工作的許可權，以執行各種系統相關作業，例如關閉系統、載入設備磁碟機，或變更系統時間。
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- 許可權元素工作排程器
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466421"
---
# <a name="privilege-requiredprivilegestype-element"></a><span data-ttu-id="c5d22-104">許可權 (requiredPrivilegesType) 元素</span><span class="sxs-lookup"><span data-stu-id="c5d22-104">Privilege (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="c5d22-105">指定工作的許可權，以執行各種系統相關作業，例如關閉系統、載入設備磁碟機，或變更系統時間。</span><span class="sxs-lookup"><span data-stu-id="c5d22-105">Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

<span data-ttu-id="c5d22-106">**許可權** 元素是由 [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c5d22-106">The **Privilege** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c5d22-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c5d22-107">Parent element</span></span>



| <span data-ttu-id="c5d22-108">元素</span><span class="sxs-lookup"><span data-stu-id="c5d22-108">Element</span></span>                                                                                             | <span data-ttu-id="c5d22-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c5d22-109">Derived from</span></span>                                                                             | <span data-ttu-id="c5d22-110">Description</span><span class="sxs-lookup"><span data-stu-id="c5d22-110">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5d22-111">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="c5d22-111">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="c5d22-112">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="c5d22-112">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="c5d22-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="c5d22-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c5d22-114">備註</span><span class="sxs-lookup"><span data-stu-id="c5d22-114">Remarks</span></span>

<span data-ttu-id="c5d22-115">針對 c + + 開發，這項資訊是透過 [**IPrincipal2：： RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="c5d22-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c5d22-116">範例</span><span class="sxs-lookup"><span data-stu-id="c5d22-116">Examples</span></span>

<span data-ttu-id="c5d22-117">下列 XML 會定義設定專案，指定工作執行各種系統相關作業的許可權，例如關閉系統、載入設備磁碟機，或變更系統時間。</span><span class="sxs-lookup"><span data-stu-id="c5d22-117">The following XML defines a settings element that specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
        
```



## <a name="requirements"></a><span data-ttu-id="c5d22-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5d22-118">Requirements</span></span>



| <span data-ttu-id="c5d22-119">需求</span><span class="sxs-lookup"><span data-stu-id="c5d22-119">Requirement</span></span> | <span data-ttu-id="c5d22-120">值</span><span class="sxs-lookup"><span data-stu-id="c5d22-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c5d22-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5d22-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d22-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5d22-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c5d22-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5d22-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d22-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5d22-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5d22-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5d22-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d22-126">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c5d22-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






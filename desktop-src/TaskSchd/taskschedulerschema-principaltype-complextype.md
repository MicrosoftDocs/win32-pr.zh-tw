---
title: principalType 複雜類型
description: 定義主體專案的屬性、子項目和排序資訊。
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- principalType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466276"
---
# <a name="principaltype-complex-type"></a><span data-ttu-id="f8af5-104">principalType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="f8af5-104">principalType Complex Type</span></span>

<span data-ttu-id="f8af5-105">定義 [**主體**](taskschedulerschema-principal-principaltype-element.md) 專案的屬性、子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="f8af5-105">Defines the attribute, child elements, and sequencing information for the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f8af5-106">子元素</span><span class="sxs-lookup"><span data-stu-id="f8af5-106">Child elements</span></span>



| <span data-ttu-id="f8af5-107">元素</span><span class="sxs-lookup"><span data-stu-id="f8af5-107">Element</span></span>                                                                                             | <span data-ttu-id="f8af5-108">類型</span><span class="sxs-lookup"><span data-stu-id="f8af5-108">Type</span></span>                                                                                     | <span data-ttu-id="f8af5-109">Description</span><span class="sxs-lookup"><span data-stu-id="f8af5-109">Description</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8af5-110">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="f8af5-110">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md)                        | <span data-ttu-id="f8af5-111">字串</span><span class="sxs-lookup"><span data-stu-id="f8af5-111">string</span></span>                                                                                   | <span data-ttu-id="f8af5-112">指定工作排程器使用者介面中顯示的主體名稱 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="f8af5-112">Specifies the name of the principal that is displayed in the Task Scheduler user interface (UI).</span></span><br/>                 |
| [<span data-ttu-id="f8af5-113">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="f8af5-113">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)                                | [<span data-ttu-id="f8af5-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="f8af5-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="f8af5-115">指定執行與主體相關聯之工作所需之使用者群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8af5-115">Specifies the identifier of the user group that is required to run tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="f8af5-116">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="f8af5-116">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)                            | [<span data-ttu-id="f8af5-117">**logonType**</span><span class="sxs-lookup"><span data-stu-id="f8af5-117">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md)                            | <span data-ttu-id="f8af5-118">指定執行與主體相關聯之工作所需的安全性登入方法。</span><span class="sxs-lookup"><span data-stu-id="f8af5-118">Specifies the security logon method that is required to run tasks that are associated with the principal.</span></span><br/>        |
| [<span data-ttu-id="f8af5-119">**ProcessTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="f8af5-119">**ProcessTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [<span data-ttu-id="f8af5-120">**processTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="f8af5-120">**processTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-simpletype.md)        | <span data-ttu-id="f8af5-121">指定工作可使用 (SID) 的進程安全識別碼類型。</span><span class="sxs-lookup"><span data-stu-id="f8af5-121">Specifies the types of process security identifier (SID) that can be used by tasks.</span></span><br/>                              |
| [<span data-ttu-id="f8af5-122">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="f8af5-122">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="f8af5-123">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="f8af5-123">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="f8af5-124">指定執行工作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="f8af5-124">Specifies the required privileges to run the task.</span></span><br/>                                                               |
| [<span data-ttu-id="f8af5-125">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="f8af5-125">**RunLevel**</span></span>](taskschedulerschema-runlevel-principaltype-element.md)                              | [<span data-ttu-id="f8af5-126">**runLevelType**</span><span class="sxs-lookup"><span data-stu-id="f8af5-126">**runLevelType**</span></span>](taskschedulerschema-runleveltype-simpletype.md)                      | <span data-ttu-id="f8af5-127">指定將在其上執行工作的許可權層級。</span><span class="sxs-lookup"><span data-stu-id="f8af5-127">Specifies the permission level that the task will be run at.</span></span><br/>                                                     |
| [<span data-ttu-id="f8af5-128">**UserId**</span><span class="sxs-lookup"><span data-stu-id="f8af5-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)                                  | [<span data-ttu-id="f8af5-129">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="f8af5-129">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="f8af5-130">指定執行與主體相關聯之工作所需的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8af5-130">Specifies the user identifier that is required to run tasks that are associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="f8af5-131">屬性</span><span class="sxs-lookup"><span data-stu-id="f8af5-131">Attributes</span></span>



| <span data-ttu-id="f8af5-132">名稱</span><span class="sxs-lookup"><span data-stu-id="f8af5-132">Name</span></span> | <span data-ttu-id="f8af5-133">類型</span><span class="sxs-lookup"><span data-stu-id="f8af5-133">Type</span></span> | <span data-ttu-id="f8af5-134">描述</span><span class="sxs-lookup"><span data-stu-id="f8af5-134">Description</span></span>                                           |
|------|------|-------------------------------------------------------|
| <span data-ttu-id="f8af5-135">id</span><span class="sxs-lookup"><span data-stu-id="f8af5-135">id</span></span>   | <span data-ttu-id="f8af5-136">識別碼</span><span class="sxs-lookup"><span data-stu-id="f8af5-136">ID</span></span>   | <span data-ttu-id="f8af5-137">指定主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8af5-137">Specifies the identifier of the principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f8af5-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8af5-138">Requirements</span></span>



| <span data-ttu-id="f8af5-139">需求</span><span class="sxs-lookup"><span data-stu-id="f8af5-139">Requirement</span></span> | <span data-ttu-id="f8af5-140">值</span><span class="sxs-lookup"><span data-stu-id="f8af5-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f8af5-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8af5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f8af5-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8af5-142">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f8af5-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8af5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f8af5-144">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8af5-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8af5-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8af5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8af5-146">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="f8af5-146">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f8af5-147">工作排程器</span><span class="sxs-lookup"><span data-stu-id="f8af5-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






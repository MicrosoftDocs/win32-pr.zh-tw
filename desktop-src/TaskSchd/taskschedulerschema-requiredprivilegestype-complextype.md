---
title: requiredPrivilegesType 複雜類型
description: 定義 RequiredPrivileges (requiredPrivilegesType) 元素的子項目和排序資訊。
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- requiredPrivilegesType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466981"
---
# <a name="requiredprivilegestype-complex-type"></a><span data-ttu-id="c07d5-104">requiredPrivilegesType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="c07d5-104">requiredPrivilegesType Complex Type</span></span>

<span data-ttu-id="c07d5-105">定義 [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="c07d5-105">Defines the child elements and sequencing information for the [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) element.</span></span>

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c07d5-106">子元素</span><span class="sxs-lookup"><span data-stu-id="c07d5-106">Child elements</span></span>



| <span data-ttu-id="c07d5-107">元素</span><span class="sxs-lookup"><span data-stu-id="c07d5-107">Element</span></span>                                                                           | <span data-ttu-id="c07d5-108">類型</span><span class="sxs-lookup"><span data-stu-id="c07d5-108">Type</span></span>                                                                  | <span data-ttu-id="c07d5-109">Description</span><span class="sxs-lookup"><span data-stu-id="c07d5-109">Description</span></span>                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="c07d5-110">**特權**</span><span class="sxs-lookup"><span data-stu-id="c07d5-110">**Privilege**</span></span>](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [<span data-ttu-id="c07d5-111">**privilegeType**</span><span class="sxs-lookup"><span data-stu-id="c07d5-111">**privilegeType**</span></span>](taskschedulerschema-privilegetype-simpletype.md) | <span data-ttu-id="c07d5-112">指定工作的必要許可權。</span><span class="sxs-lookup"><span data-stu-id="c07d5-112">Specifies the required privileges of the task.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="c07d5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c07d5-113">Requirements</span></span>



| <span data-ttu-id="c07d5-114">需求</span><span class="sxs-lookup"><span data-stu-id="c07d5-114">Requirement</span></span> | <span data-ttu-id="c07d5-115">值</span><span class="sxs-lookup"><span data-stu-id="c07d5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c07d5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c07d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c07d5-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c07d5-117">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c07d5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c07d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c07d5-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c07d5-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c07d5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c07d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07d5-121">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="c07d5-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c07d5-122">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c07d5-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






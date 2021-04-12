---
title: SecurityDescriptor (registrationInfoType) 元素
description: 指定工作的安全描述項。
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- SecurityDescriptor 元素工作排程器
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024768"
---
# <a name="securitydescriptor-registrationinfotype-element"></a><span data-ttu-id="9a1e9-104">SecurityDescriptor (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="9a1e9-104">SecurityDescriptor (registrationInfoType) Element</span></span>

<span data-ttu-id="9a1e9-105">指定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="9a1e9-105">Specifies the security descriptor of the task.</span></span>

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

<span data-ttu-id="9a1e9-106">**SecurityDescriptor** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="9a1e9-106">The **SecurityDescriptor** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9a1e9-107">父元素</span><span class="sxs-lookup"><span data-stu-id="9a1e9-107">Parent element</span></span>



| <span data-ttu-id="9a1e9-108">元素</span><span class="sxs-lookup"><span data-stu-id="9a1e9-108">Element</span></span>                                                                           | <span data-ttu-id="9a1e9-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="9a1e9-109">Derived from</span></span>                                                                         | <span data-ttu-id="9a1e9-110">Description</span><span class="sxs-lookup"><span data-stu-id="9a1e9-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a1e9-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="9a1e9-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="9a1e9-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="9a1e9-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="9a1e9-113">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="9a1e9-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9a1e9-114">備註</span><span class="sxs-lookup"><span data-stu-id="9a1e9-114">Remarks</span></span>

<span data-ttu-id="9a1e9-115">針對開發腳本，會使用 [**RegistrationInfo SecurityDescriptor**](registrationinfo-securitydescriptor.md) 屬性來指定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="9a1e9-115">For scripting development, the security descriptor of a task is specified using the [**RegistrationInfo.SecurityDescriptor**](registrationinfo-securitydescriptor.md) property.</span></span>

<span data-ttu-id="9a1e9-116">若是 c + + 開發，則會使用 [**IRegistrationInfo：： SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) 屬性來指定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="9a1e9-116">For C++ development, the security descriptor of a task is specified using the [**IRegistrationInfo::SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a1e9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a1e9-117">Requirements</span></span>



| <span data-ttu-id="9a1e9-118">需求</span><span class="sxs-lookup"><span data-stu-id="9a1e9-118">Requirement</span></span> | <span data-ttu-id="9a1e9-119">值</span><span class="sxs-lookup"><span data-stu-id="9a1e9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a1e9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a1e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9a1e9-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a1e9-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a1e9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a1e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9a1e9-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a1e9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a1e9-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a1e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1e9-125">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="9a1e9-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9a1e9-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="9a1e9-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






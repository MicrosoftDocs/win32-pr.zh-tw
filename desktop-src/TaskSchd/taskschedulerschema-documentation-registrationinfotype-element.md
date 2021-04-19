---
title: 檔 (registrationInfoType) 元素
description: 指定工作的任何其他檔。
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- 檔元素工作排程器
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979695"
---
# <a name="documentation-registrationinfotype-element"></a><span data-ttu-id="4af5f-104">檔 (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="4af5f-104">Documentation (registrationInfoType) Element</span></span>

<span data-ttu-id="4af5f-105">指定工作的任何其他檔。</span><span class="sxs-lookup"><span data-stu-id="4af5f-105">Specifies any additional documentation for the task.</span></span>

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="4af5f-106">**檔** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="4af5f-106">The **Documentation** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4af5f-107">父元素</span><span class="sxs-lookup"><span data-stu-id="4af5f-107">Parent element</span></span>



| <span data-ttu-id="4af5f-108">元素</span><span class="sxs-lookup"><span data-stu-id="4af5f-108">Element</span></span>                                                                           | <span data-ttu-id="4af5f-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="4af5f-109">Derived from</span></span>                                                                         | <span data-ttu-id="4af5f-110">Description</span><span class="sxs-lookup"><span data-stu-id="4af5f-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4af5f-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="4af5f-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="4af5f-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="4af5f-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="4af5f-113">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="4af5f-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4af5f-114">備註</span><span class="sxs-lookup"><span data-stu-id="4af5f-114">Remarks</span></span>

<span data-ttu-id="4af5f-115">若為腳本應用程式，則會使用 [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) 屬性來指定額外的工作檔。</span><span class="sxs-lookup"><span data-stu-id="4af5f-115">For scripting applications, additional task documentation is specified using the using the [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) property.</span></span>

<span data-ttu-id="4af5f-116">若是 c + + 應用程式，則使用 [**IRegistrationInfo：:D 檔**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) 屬性來指定其他工作檔。</span><span class="sxs-lookup"><span data-stu-id="4af5f-116">For C++ applications, additional task documentation is specified using the using the [**IRegistrationInfo::Documentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4af5f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4af5f-117">Requirements</span></span>



| <span data-ttu-id="4af5f-118">需求</span><span class="sxs-lookup"><span data-stu-id="4af5f-118">Requirement</span></span> | <span data-ttu-id="4af5f-119">值</span><span class="sxs-lookup"><span data-stu-id="4af5f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4af5f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4af5f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4af5f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4af5f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4af5f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4af5f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4af5f-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4af5f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4af5f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4af5f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af5f-125">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="4af5f-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






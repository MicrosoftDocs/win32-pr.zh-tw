---
title: 日期 (registrationInfoType) 元素
description: 指定註冊工作的日期和時間。
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- 日期元素工作排程器
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104634"
---
# <a name="date-registrationinfotype-element"></a><span data-ttu-id="c6062-104">日期 (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="c6062-104">Date (registrationInfoType) Element</span></span>

<span data-ttu-id="c6062-105">指定註冊工作的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c6062-105">Specifies the date and time when the task is registered.</span></span>

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

<span data-ttu-id="c6062-106">**Date** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c6062-106">The **Date** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c6062-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c6062-107">Parent element</span></span>



| <span data-ttu-id="c6062-108">元素</span><span class="sxs-lookup"><span data-stu-id="c6062-108">Element</span></span>                                                                           | <span data-ttu-id="c6062-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c6062-109">Derived from</span></span>                                                                         | <span data-ttu-id="c6062-110">Description</span><span class="sxs-lookup"><span data-stu-id="c6062-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6062-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="c6062-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="c6062-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="c6062-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="c6062-113">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="c6062-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c6062-114">備註</span><span class="sxs-lookup"><span data-stu-id="c6062-114">Remarks</span></span>

<span data-ttu-id="c6062-115">針對開發腳本，會使用 [ [**RegistrationInfo**](registrationinfo-date.md) ] 屬性來指定工作的註冊日期。</span><span class="sxs-lookup"><span data-stu-id="c6062-115">For scripting development, the registration date of a task is specified using the [**RegistrationInfo.Date**](registrationinfo-date.md) property.</span></span>

<span data-ttu-id="c6062-116">針對 c + + 開發，會使用 [**IRegistrationInfo：:D ate**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) 屬性來指定工作的註冊日期。</span><span class="sxs-lookup"><span data-stu-id="c6062-116">For C++ development, the registration date of a task is specified using the [**IRegistrationInfo::Date**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6062-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6062-117">Requirements</span></span>



| <span data-ttu-id="c6062-118">需求</span><span class="sxs-lookup"><span data-stu-id="c6062-118">Requirement</span></span> | <span data-ttu-id="c6062-119">值</span><span class="sxs-lookup"><span data-stu-id="c6062-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6062-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6062-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c6062-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6062-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6062-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6062-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c6062-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6062-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6062-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6062-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6062-125">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c6062-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c6062-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c6062-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






---
title: 來源 (registrationInfoType) 元素
description: 指定工作源自的位置。 例如，從元件、服務、應用程式或使用者。
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- 來源元素工作排程器
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384094"
---
# <a name="source-registrationinfotype-element"></a><span data-ttu-id="727d6-105">來源 (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="727d6-105">Source (registrationInfoType) Element</span></span>

<span data-ttu-id="727d6-106">指定工作源自的位置。</span><span class="sxs-lookup"><span data-stu-id="727d6-106">Specifies where the task originated from.</span></span> <span data-ttu-id="727d6-107">例如，從元件、服務、應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="727d6-107">For example, from a component, a service, an application, or a user.</span></span>

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="727d6-108">**Source** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="727d6-108">The **Source** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="727d6-109">父元素</span><span class="sxs-lookup"><span data-stu-id="727d6-109">Parent element</span></span>



| <span data-ttu-id="727d6-110">元素</span><span class="sxs-lookup"><span data-stu-id="727d6-110">Element</span></span>                                                                           | <span data-ttu-id="727d6-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="727d6-111">Derived from</span></span>                                                                         | <span data-ttu-id="727d6-112">Description</span><span class="sxs-lookup"><span data-stu-id="727d6-112">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="727d6-113">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="727d6-113">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="727d6-114">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="727d6-114">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="727d6-115">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="727d6-115">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="727d6-116">備註</span><span class="sxs-lookup"><span data-stu-id="727d6-116">Remarks</span></span>

<span data-ttu-id="727d6-117">針對開發腳本，會使用 [**RegistrationInfo 的 source**](registrationinfo-source.md) 屬性來指定工作的來源。</span><span class="sxs-lookup"><span data-stu-id="727d6-117">For scripting development, the source of a task is specified using the [**RegistrationInfo.Source**](registrationinfo-source.md) property.</span></span>

<span data-ttu-id="727d6-118">若是 c + + 開發，則會使用 [**IRegistrationInfo：： source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) 屬性來指定工作的來源。</span><span class="sxs-lookup"><span data-stu-id="727d6-118">For C++ development, the source of a task is specified using the [**IRegistrationInfo::Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="727d6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="727d6-119">Requirements</span></span>



| <span data-ttu-id="727d6-120">需求</span><span class="sxs-lookup"><span data-stu-id="727d6-120">Requirement</span></span> | <span data-ttu-id="727d6-121">值</span><span class="sxs-lookup"><span data-stu-id="727d6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="727d6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="727d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="727d6-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="727d6-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="727d6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="727d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="727d6-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="727d6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="727d6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="727d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727d6-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="727d6-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="727d6-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="727d6-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






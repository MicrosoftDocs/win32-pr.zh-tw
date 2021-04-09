---
title: 描述 (registrationInfoType) 元素
description: 指定工作的描述。
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Description 元素工作排程器
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685738"
---
# <a name="description-registrationinfotype-element"></a><span data-ttu-id="b73fe-104">描述 (registrationInfoType) 元素</span><span class="sxs-lookup"><span data-stu-id="b73fe-104">Description (registrationInfoType) Element</span></span>

<span data-ttu-id="b73fe-105">指定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="b73fe-105">Specifies the description of the task.</span></span>

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="b73fe-106">**Description** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="b73fe-106">The **Description** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b73fe-107">父元素</span><span class="sxs-lookup"><span data-stu-id="b73fe-107">Parent element</span></span>



| <span data-ttu-id="b73fe-108">元素</span><span class="sxs-lookup"><span data-stu-id="b73fe-108">Element</span></span>                                                                           | <span data-ttu-id="b73fe-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="b73fe-109">Derived from</span></span>                                                                         | <span data-ttu-id="b73fe-110">Description</span><span class="sxs-lookup"><span data-stu-id="b73fe-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b73fe-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b73fe-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="b73fe-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="b73fe-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="b73fe-113">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="b73fe-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b73fe-114">備註</span><span class="sxs-lookup"><span data-stu-id="b73fe-114">Remarks</span></span>

<span data-ttu-id="b73fe-115">針對開發腳本，會使用 [**RegistrationInfo 的 description**](registrationinfo-description.md) 屬性指定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="b73fe-115">For scripting development, the description of a task is specified using the [**RegistrationInfo.Description**](registrationinfo-description.md) property.</span></span>

<span data-ttu-id="b73fe-116">針對 c + + 開發，會使用 [**IRegistrationInfo：:D 描述 e)**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) 屬性來指定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="b73fe-116">For C++ development, the description of a task is specified using the [**IRegistrationInfo::Description**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b73fe-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b73fe-117">Requirements</span></span>



| <span data-ttu-id="b73fe-118">需求</span><span class="sxs-lookup"><span data-stu-id="b73fe-118">Requirement</span></span> | <span data-ttu-id="b73fe-119">值</span><span class="sxs-lookup"><span data-stu-id="b73fe-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b73fe-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b73fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b73fe-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b73fe-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b73fe-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b73fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b73fe-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b73fe-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b73fe-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b73fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73fe-125">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="b73fe-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b73fe-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b73fe-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






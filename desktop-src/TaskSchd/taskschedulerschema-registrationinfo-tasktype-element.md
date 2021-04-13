---
title: RegistrationInfo (taskType) 元素
description: 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- 註冊資訊工作排程器、XML 元素
- RegistrationInfo 元素工作排程器
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466020"
---
# <a name="registrationinfo-tasktype-element"></a><span data-ttu-id="fb8ad-105">RegistrationInfo (taskType) 元素</span><span class="sxs-lookup"><span data-stu-id="fb8ad-105">RegistrationInfo (taskType) Element</span></span>

<span data-ttu-id="fb8ad-106">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-106">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

<span data-ttu-id="fb8ad-107">**RegistrationInfo** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-107">The **RegistrationInfo** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fb8ad-108">父元素</span><span class="sxs-lookup"><span data-stu-id="fb8ad-108">Parent element</span></span>



| <span data-ttu-id="fb8ad-109">元素</span><span class="sxs-lookup"><span data-stu-id="fb8ad-109">Element</span></span>                                          | <span data-ttu-id="fb8ad-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="fb8ad-110">Derived from</span></span>                                                 | <span data-ttu-id="fb8ad-111">Description</span><span class="sxs-lookup"><span data-stu-id="fb8ad-111">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="fb8ad-112">**Task**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-112">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="fb8ad-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="fb8ad-114">定義工作排程器服務所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-114">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="fb8ad-115">子元素</span><span class="sxs-lookup"><span data-stu-id="fb8ad-115">Child elements</span></span>



| <span data-ttu-id="fb8ad-116">元素</span><span class="sxs-lookup"><span data-stu-id="fb8ad-116">Element</span></span>                                                                                                                  | <span data-ttu-id="fb8ad-117">類型</span><span class="sxs-lookup"><span data-stu-id="fb8ad-117">Type</span></span>     | <span data-ttu-id="fb8ad-118">Description</span><span class="sxs-lookup"><span data-stu-id="fb8ad-118">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb8ad-119">**編寫 (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-119">**Author (registrationInfoType)**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="fb8ad-120">字串</span><span class="sxs-lookup"><span data-stu-id="fb8ad-120">string</span></span>   | <span data-ttu-id="fb8ad-121">指定工作的作者。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-121">Specifies the author of the task.</span></span><br/>                                                                              |
| [<span data-ttu-id="fb8ad-122">**日期 (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-122">**Date (registrationInfoType)**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="fb8ad-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="fb8ad-123">dateTime</span></span> | <span data-ttu-id="fb8ad-124">指定註冊工作的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-124">Specifies the date and time when the task is registered.</span></span><br/>                                                       |
| [<span data-ttu-id="fb8ad-125">**描述 (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-125">**Description (registrationInfoType)**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="fb8ad-126">字串</span><span class="sxs-lookup"><span data-stu-id="fb8ad-126">string</span></span>   | <span data-ttu-id="fb8ad-127">指定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-127">Specifies the description of the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="fb8ad-128">**檔 (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-128">**Documentation (registrationInfoType)**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="fb8ad-129">字串</span><span class="sxs-lookup"><span data-stu-id="fb8ad-129">string</span></span>   | <span data-ttu-id="fb8ad-130">指定工作的任何其他檔。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-130">Specifies any additional documentation for the task.</span></span><br/>                                                           |
| [<span data-ttu-id="fb8ad-131">**SecurityDescriptor (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-131">**SecurityDescriptor (registrationInfoType)**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="fb8ad-132">字串</span><span class="sxs-lookup"><span data-stu-id="fb8ad-132">string</span></span>   | <span data-ttu-id="fb8ad-133">指定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-133">Specifies the security descriptor of the task.</span></span><br/>                                                                 |
| [<span data-ttu-id="fb8ad-134">**來源 (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-134">**Source (registrationInfoType)**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="fb8ad-135">字串</span><span class="sxs-lookup"><span data-stu-id="fb8ad-135">string</span></span>   | <span data-ttu-id="fb8ad-136">指定工作源自的位置。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-136">Specifies where the task originated from.</span></span> <span data-ttu-id="fb8ad-137">例如，從元件、服務、應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-137">For example, from a component, a service, an application, or a user.</span></span><br/> |
| [<span data-ttu-id="fb8ad-138">**URI (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-138">**URI (registrationInfoType)**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="fb8ad-139">anyURI</span><span class="sxs-lookup"><span data-stu-id="fb8ad-139">anyURI</span></span>   | <span data-ttu-id="fb8ad-140">指定工作的 URI。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-140">Specifies the URI of the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="fb8ad-141">**版本 (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="fb8ad-141">**Version (registrationInfoType)**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="fb8ad-142">字串</span><span class="sxs-lookup"><span data-stu-id="fb8ad-142">string</span></span>   | <span data-ttu-id="fb8ad-143">指定工作的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-143">Specifies the version number of the task.</span></span><br/>                                                                      |



## <a name="remarks"></a><span data-ttu-id="fb8ad-144">備註</span><span class="sxs-lookup"><span data-stu-id="fb8ad-144">Remarks</span></span>

<span data-ttu-id="fb8ad-145">針對開發腳本，會使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性指定工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-145">For scripting development, the registration information of a task is specified using the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property.</span></span>

<span data-ttu-id="fb8ad-146">針對 c + + 開發，會使用 [**ITaskDefinition 的 RegistrationInfo 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo)來指定工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="fb8ad-146">For C++ development, the registration information of a task is specified using the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb8ad-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb8ad-147">Requirements</span></span>



| <span data-ttu-id="fb8ad-148">需求</span><span class="sxs-lookup"><span data-stu-id="fb8ad-148">Requirement</span></span> | <span data-ttu-id="fb8ad-149">值</span><span class="sxs-lookup"><span data-stu-id="fb8ad-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb8ad-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb8ad-150">Minimum supported client</span></span><br/> | <span data-ttu-id="fb8ad-151">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb8ad-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb8ad-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb8ad-152">Minimum supported server</span></span><br/> | <span data-ttu-id="fb8ad-153">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb8ad-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb8ad-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb8ad-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb8ad-155">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="fb8ad-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="fb8ad-156">工作排程器</span><span class="sxs-lookup"><span data-stu-id="fb8ad-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






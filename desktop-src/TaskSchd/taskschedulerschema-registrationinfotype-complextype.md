---
title: registrationInfoType 複雜類型
description: 定義 RegistrationInfo 元素的子項目和排序資訊。
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- registrationInfoType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934669"
---
# <a name="registrationinfotype-complex-type"></a><span data-ttu-id="dd79f-104">registrationInfoType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="dd79f-104">registrationInfoType Complex Type</span></span>

<span data-ttu-id="dd79f-105">定義 [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="dd79f-105">Defines the child elements and sequencing information for the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="dd79f-106">子元素</span><span class="sxs-lookup"><span data-stu-id="dd79f-106">Child elements</span></span>



| <span data-ttu-id="dd79f-107">元素</span><span class="sxs-lookup"><span data-stu-id="dd79f-107">Element</span></span>                                                                                           | <span data-ttu-id="dd79f-108">類型</span><span class="sxs-lookup"><span data-stu-id="dd79f-108">Type</span></span>     | <span data-ttu-id="dd79f-109">Description</span><span class="sxs-lookup"><span data-stu-id="dd79f-109">Description</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd79f-110">**作者**</span><span class="sxs-lookup"><span data-stu-id="dd79f-110">**Author**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="dd79f-111">字串</span><span class="sxs-lookup"><span data-stu-id="dd79f-111">string</span></span>   | <span data-ttu-id="dd79f-112">指定工作的作者。</span><span class="sxs-lookup"><span data-stu-id="dd79f-112">Specifies the author of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="dd79f-113">**日期**</span><span class="sxs-lookup"><span data-stu-id="dd79f-113">**Date**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="dd79f-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="dd79f-114">dateTime</span></span> | <span data-ttu-id="dd79f-115">指定註冊工作的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="dd79f-115">Specifies the date and time when the task is registered.</span></span><br/>                                                |
| [<span data-ttu-id="dd79f-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="dd79f-116">**Description**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="dd79f-117">字串</span><span class="sxs-lookup"><span data-stu-id="dd79f-117">string</span></span>   | <span data-ttu-id="dd79f-118">指定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="dd79f-118">Specifies the description of the task.</span></span><br/>                                                                  |
| [<span data-ttu-id="dd79f-119">**文件**</span><span class="sxs-lookup"><span data-stu-id="dd79f-119">**Documentation**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="dd79f-120">字串</span><span class="sxs-lookup"><span data-stu-id="dd79f-120">string</span></span>   | <span data-ttu-id="dd79f-121">指定工作的任何其他檔。</span><span class="sxs-lookup"><span data-stu-id="dd79f-121">Specifies any additional documentation for the task.</span></span><br/>                                                    |
| [<span data-ttu-id="dd79f-122">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="dd79f-122">**SecurityDescriptor**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="dd79f-123">字串</span><span class="sxs-lookup"><span data-stu-id="dd79f-123">string</span></span>   | <span data-ttu-id="dd79f-124">指定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="dd79f-124">Specifies the security descriptor of the task.</span></span><br/>                                                          |
| [<span data-ttu-id="dd79f-125">**源**</span><span class="sxs-lookup"><span data-stu-id="dd79f-125">**Source**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="dd79f-126">字串</span><span class="sxs-lookup"><span data-stu-id="dd79f-126">string</span></span>   | <span data-ttu-id="dd79f-127">指定工作源自的位置。</span><span class="sxs-lookup"><span data-stu-id="dd79f-127">Specifies where the task originated from.</span></span> <span data-ttu-id="dd79f-128">例如，從元件、服務、應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="dd79f-128">For example, from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="dd79f-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="dd79f-129">**URI**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="dd79f-130">anyURI</span><span class="sxs-lookup"><span data-stu-id="dd79f-130">anyURI</span></span>   | <span data-ttu-id="dd79f-131">指定工作的 URI。</span><span class="sxs-lookup"><span data-stu-id="dd79f-131">Specifies the URI of the task.</span></span><br/>                                                                          |
| [<span data-ttu-id="dd79f-132">**版本**</span><span class="sxs-lookup"><span data-stu-id="dd79f-132">**Version**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="dd79f-133">字串</span><span class="sxs-lookup"><span data-stu-id="dd79f-133">string</span></span>   | <span data-ttu-id="dd79f-134">指定工作的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="dd79f-134">Specifies the version number of the task.</span></span><br/>                                                               |



## <a name="requirements"></a><span data-ttu-id="dd79f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd79f-135">Requirements</span></span>



| <span data-ttu-id="dd79f-136">需求</span><span class="sxs-lookup"><span data-stu-id="dd79f-136">Requirement</span></span> | <span data-ttu-id="dd79f-137">值</span><span class="sxs-lookup"><span data-stu-id="dd79f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd79f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd79f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dd79f-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd79f-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd79f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd79f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dd79f-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd79f-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd79f-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd79f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd79f-143">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="dd79f-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="dd79f-144">工作排程器</span><span class="sxs-lookup"><span data-stu-id="dd79f-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






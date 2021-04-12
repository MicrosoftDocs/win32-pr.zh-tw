---
title: registrationTriggerType 複雜類型
description: 定義 RegistrationTrigger 元素的子項目和排序資訊。
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- registrationTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384998"
---
# <a name="registrationtriggertype-complex-type"></a><span data-ttu-id="cdd28-104">registrationTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="cdd28-104">registrationTriggerType Complex Type</span></span>

<span data-ttu-id="cdd28-105">定義 [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="cdd28-105">Defines child elements and sequencing information for the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cdd28-106">子元素</span><span class="sxs-lookup"><span data-stu-id="cdd28-106">Child elements</span></span>



| <span data-ttu-id="cdd28-107">元素</span><span class="sxs-lookup"><span data-stu-id="cdd28-107">Element</span></span>                                                                    | <span data-ttu-id="cdd28-108">類型</span><span class="sxs-lookup"><span data-stu-id="cdd28-108">Type</span></span>     | <span data-ttu-id="cdd28-109">Description</span><span class="sxs-lookup"><span data-stu-id="cdd28-109">Description</span></span>                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdd28-110">**延遲**</span><span class="sxs-lookup"><span data-stu-id="cdd28-110">**Delay**</span></span>](taskschedulerschema-delay-registrationtriggertype-element.md) | <span data-ttu-id="cdd28-111">duration</span><span class="sxs-lookup"><span data-stu-id="cdd28-111">duration</span></span> | <span data-ttu-id="cdd28-112">指定在註冊工作與啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="cdd28-112">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cdd28-113">備註</span><span class="sxs-lookup"><span data-stu-id="cdd28-113">Remarks</span></span>

<span data-ttu-id="cdd28-114">除了這裡定義的子項目之外， [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) 元素也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子專案。</span><span class="sxs-lookup"><span data-stu-id="cdd28-114">In addition to the child elements defined here, the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd28-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdd28-115">Requirements</span></span>



| <span data-ttu-id="cdd28-116">需求</span><span class="sxs-lookup"><span data-stu-id="cdd28-116">Requirement</span></span> | <span data-ttu-id="cdd28-117">值</span><span class="sxs-lookup"><span data-stu-id="cdd28-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cdd28-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdd28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd28-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdd28-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cdd28-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdd28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd28-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdd28-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cdd28-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdd28-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd28-123">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="cdd28-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="cdd28-124">工作排程器</span><span class="sxs-lookup"><span data-stu-id="cdd28-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






---
title: bootTriggerType 複雜類型
description: 定義 BootTrigger 元素的子項目和排序資訊。
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- bootTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466292"
---
# <a name="boottriggertype-complex-type"></a><span data-ttu-id="fb3ce-104">bootTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="fb3ce-104">bootTriggerType Complex Type</span></span>

<span data-ttu-id="fb3ce-105">定義 [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="fb3ce-105">Defines the child element and sequencing information for the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="bootTriggerType">
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

## <a name="child-elements"></a><span data-ttu-id="fb3ce-106">子元素</span><span class="sxs-lookup"><span data-stu-id="fb3ce-106">Child elements</span></span>



| <span data-ttu-id="fb3ce-107">元素</span><span class="sxs-lookup"><span data-stu-id="fb3ce-107">Element</span></span>                                                            | <span data-ttu-id="fb3ce-108">類型</span><span class="sxs-lookup"><span data-stu-id="fb3ce-108">Type</span></span>     | <span data-ttu-id="fb3ce-109">Description</span><span class="sxs-lookup"><span data-stu-id="fb3ce-109">Description</span></span>                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb3ce-110">**延遲**</span><span class="sxs-lookup"><span data-stu-id="fb3ce-110">**Delay**</span></span>](taskschedulerschema-delay-boottriggertype-element.md) | <span data-ttu-id="fb3ce-111">duration</span><span class="sxs-lookup"><span data-stu-id="fb3ce-111">duration</span></span> | <span data-ttu-id="fb3ce-112">系統開機和引發觸發程式之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="fb3ce-112">Amount of time between when the system is booted and when the trigger is fired.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="fb3ce-113">備註</span><span class="sxs-lookup"><span data-stu-id="fb3ce-113">Remarks</span></span>

<span data-ttu-id="fb3ce-114">除了這裡定義的子項目之外， [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) 元素也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子專案。</span><span class="sxs-lookup"><span data-stu-id="fb3ce-114">In addition to the child element defined here, the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3ce-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb3ce-115">Requirements</span></span>



| <span data-ttu-id="fb3ce-116">需求</span><span class="sxs-lookup"><span data-stu-id="fb3ce-116">Requirement</span></span> | <span data-ttu-id="fb3ce-117">值</span><span class="sxs-lookup"><span data-stu-id="fb3ce-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb3ce-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb3ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb3ce-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb3ce-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb3ce-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb3ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb3ce-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb3ce-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb3ce-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb3ce-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3ce-123">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="fb3ce-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="fb3ce-124">工作排程器</span><span class="sxs-lookup"><span data-stu-id="fb3ce-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






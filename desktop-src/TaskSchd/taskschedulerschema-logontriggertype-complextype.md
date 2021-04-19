---
title: logonTriggerType 複雜類型
description: 定義 LogonTrigger 元素的子項目和排序資訊。
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- logonTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001315"
---
# <a name="logontriggertype-complex-type"></a><span data-ttu-id="876e5-104">logonTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="876e5-104">logonTriggerType Complex Type</span></span>

<span data-ttu-id="876e5-105">定義 [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="876e5-105">Defines the child elements and sequencing information for the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
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

## <a name="child-elements"></a><span data-ttu-id="876e5-106">子元素</span><span class="sxs-lookup"><span data-stu-id="876e5-106">Child elements</span></span>



| <span data-ttu-id="876e5-107">元素</span><span class="sxs-lookup"><span data-stu-id="876e5-107">Element</span></span>                                                               | <span data-ttu-id="876e5-108">類型</span><span class="sxs-lookup"><span data-stu-id="876e5-108">Type</span></span>                                                                    | <span data-ttu-id="876e5-109">Description</span><span class="sxs-lookup"><span data-stu-id="876e5-109">Description</span></span>                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="876e5-110">**延遲**</span><span class="sxs-lookup"><span data-stu-id="876e5-110">**Delay**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)   | <span data-ttu-id="876e5-111">duration</span><span class="sxs-lookup"><span data-stu-id="876e5-111">duration</span></span>                                                                | <span data-ttu-id="876e5-112">使用者登入和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="876e5-112">Amount of time between when the user logs on and when the task is started.</span></span><br/>         |
| [<span data-ttu-id="876e5-113">**UserId**</span><span class="sxs-lookup"><span data-stu-id="876e5-113">**UserId**</span></span>](taskschedulerschema-userid-logontriggertype-element.md) | [<span data-ttu-id="876e5-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="876e5-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="876e5-115">使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="876e5-115">Identifier of the user.</span></span> <span data-ttu-id="876e5-116">此工作會在此使用者登入電腦時啟動。</span><span class="sxs-lookup"><span data-stu-id="876e5-116">The task is started when this user logs onto the computer.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="876e5-117">備註</span><span class="sxs-lookup"><span data-stu-id="876e5-117">Remarks</span></span>

<span data-ttu-id="876e5-118">除了這裡定義的子項目之外， [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) 元素也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子專案。</span><span class="sxs-lookup"><span data-stu-id="876e5-118">In addition to the child elements defined here, the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="876e5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="876e5-119">Requirements</span></span>



| <span data-ttu-id="876e5-120">需求</span><span class="sxs-lookup"><span data-stu-id="876e5-120">Requirement</span></span> | <span data-ttu-id="876e5-121">值</span><span class="sxs-lookup"><span data-stu-id="876e5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="876e5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="876e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="876e5-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="876e5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="876e5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="876e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="876e5-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="876e5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="876e5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="876e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876e5-127">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="876e5-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="876e5-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="876e5-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






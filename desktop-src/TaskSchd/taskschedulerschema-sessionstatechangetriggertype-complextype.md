---
title: sessionStateChangeTriggerType 複雜類型
description: 定義用來建立主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知之工作觸發程式的元素。
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- sessionStateChangeTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317496"
---
# <a name="sessionstatechangetriggertype-complex-type"></a><span data-ttu-id="94597-104">sessionStateChangeTriggerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="94597-104">sessionStateChangeTriggerType Complex Type</span></span>

<span data-ttu-id="94597-105">定義用來建立主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知之工作觸發程式的元素。</span><span class="sxs-lookup"><span data-stu-id="94597-105">Defines the elements used to create a task trigger for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
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
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="94597-106">子元素</span><span class="sxs-lookup"><span data-stu-id="94597-106">Child elements</span></span>



| <span data-ttu-id="94597-107">元素</span><span class="sxs-lookup"><span data-stu-id="94597-107">Element</span></span>                                                                                      | <span data-ttu-id="94597-108">類型</span><span class="sxs-lookup"><span data-stu-id="94597-108">Type</span></span>                                                                                    | <span data-ttu-id="94597-109">Description</span><span class="sxs-lookup"><span data-stu-id="94597-109">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94597-110">**延遲**</span><span class="sxs-lookup"><span data-stu-id="94597-110">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="94597-111">duration</span><span class="sxs-lookup"><span data-stu-id="94597-111">duration</span></span>                                                                                | <span data-ttu-id="94597-112">指定值，這個值表示在偵測到終端機伺服器會話狀態變更時，工作開始之前的延遲時間長度。</span><span class="sxs-lookup"><span data-stu-id="94597-112">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="94597-113">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="94597-113">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="94597-114">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="94597-114">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="94597-115">指定會觸發工作啟動的終端機伺服器會話變更類型。</span><span class="sxs-lookup"><span data-stu-id="94597-115">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="94597-116">**UserId**</span><span class="sxs-lookup"><span data-stu-id="94597-116">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="94597-117">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="94597-117">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="94597-118">指定終端機伺服器會話的使用者。</span><span class="sxs-lookup"><span data-stu-id="94597-118">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="94597-119">當偵測到此使用者的會話狀態變更時，就會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="94597-119">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="94597-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="94597-120">Requirements</span></span>



| <span data-ttu-id="94597-121">需求</span><span class="sxs-lookup"><span data-stu-id="94597-121">Requirement</span></span> | <span data-ttu-id="94597-122">值</span><span class="sxs-lookup"><span data-stu-id="94597-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94597-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94597-123">Minimum supported client</span></span><br/> | <span data-ttu-id="94597-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94597-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94597-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94597-125">Minimum supported server</span></span><br/> | <span data-ttu-id="94597-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94597-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






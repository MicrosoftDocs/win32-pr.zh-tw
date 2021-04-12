---
title: Count (restartType) 元素
description: 指定工作排程器將嘗試重新開機工作的次數。
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Count 元素工作排程器
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464809"
---
# <a name="count-restarttype-element"></a><span data-ttu-id="f2608-104">Count (restartType) 元素</span><span class="sxs-lookup"><span data-stu-id="f2608-104">Count (restartType) Element</span></span>

<span data-ttu-id="f2608-105">指定工作排程器將嘗試重新開機工作的次數。</span><span class="sxs-lookup"><span data-stu-id="f2608-105">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span>

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="f2608-106">元素是由 [**restartType**](taskschedulerschema-restarttype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="f2608-106">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f2608-107">父元素</span><span class="sxs-lookup"><span data-stu-id="f2608-107">Parent element</span></span>



| <span data-ttu-id="f2608-108">元素</span><span class="sxs-lookup"><span data-stu-id="f2608-108">Element</span></span>                                                                               | <span data-ttu-id="f2608-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="f2608-109">Derived from</span></span>                                                       | <span data-ttu-id="f2608-110">Description</span><span class="sxs-lookup"><span data-stu-id="f2608-110">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2608-111">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="f2608-111">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="f2608-112">**restartType**</span><span class="sxs-lookup"><span data-stu-id="f2608-112">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="f2608-113">指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="f2608-113">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f2608-114">備註</span><span class="sxs-lookup"><span data-stu-id="f2608-114">Remarks</span></span>

<span data-ttu-id="f2608-115">如果指定這個元素，則也必須指定 [**Interval**](taskschedulerschema-interval-restarttype-element.md) 元素，以告知工作排程器要嘗試重新開機工作的時間長度。</span><span class="sxs-lookup"><span data-stu-id="f2608-115">If this element is specified, the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element must also be specified to tell the Task Scheduler how long to attempt to restart the task.</span></span>

<span data-ttu-id="f2608-116">針對 c + + 開發，請參閱 [**ITaskSettings 的 RestartCount 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount)。</span><span class="sxs-lookup"><span data-stu-id="f2608-116">For C++ development, see [**RestartCount Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span></span>

<span data-ttu-id="f2608-117">如需腳本開發，請參閱 [**TaskSettings. RestartCount**](tasksettings-restartcount.md)。</span><span class="sxs-lookup"><span data-stu-id="f2608-117">For script development, see [**TaskSettings.RestartCount**](tasksettings-restartcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2608-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2608-118">Requirements</span></span>



| <span data-ttu-id="f2608-119">需求</span><span class="sxs-lookup"><span data-stu-id="f2608-119">Requirement</span></span> | <span data-ttu-id="f2608-120">值</span><span class="sxs-lookup"><span data-stu-id="f2608-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f2608-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2608-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2608-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2608-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2608-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2608-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2608-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2608-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2608-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2608-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2608-126">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="f2608-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






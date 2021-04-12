---
title: UseUnifiedSchedulingEngine (settingsType) 元素
description: 指定將使用整合排程引擎來執行這項工作。
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- UseUnifiedSchedulingEngine 元素工作排程器
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024880"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a><span data-ttu-id="08f01-104">UseUnifiedSchedulingEngine (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="08f01-104">UseUnifiedSchedulingEngine (settingsType) Element</span></span>

<span data-ttu-id="08f01-105">指定將使用整合排程引擎來執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="08f01-105">Specifies that the Unified Scheduling Engine will be used to run this task.</span></span>

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="08f01-106">**UseUnifiedSchedulingEngine** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="08f01-106">The **UseUnifiedSchedulingEngine** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="08f01-107">父元素</span><span class="sxs-lookup"><span data-stu-id="08f01-107">Parent element</span></span>



| <span data-ttu-id="08f01-108">元素</span><span class="sxs-lookup"><span data-stu-id="08f01-108">Element</span></span>                                                           | <span data-ttu-id="08f01-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="08f01-109">Derived from</span></span>                                                         | <span data-ttu-id="08f01-110">Description</span><span class="sxs-lookup"><span data-stu-id="08f01-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="08f01-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="08f01-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="08f01-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="08f01-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="08f01-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="08f01-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="08f01-114">備註</span><span class="sxs-lookup"><span data-stu-id="08f01-114">Remarks</span></span>

<span data-ttu-id="08f01-115">此元素的預設設定為 False。</span><span class="sxs-lookup"><span data-stu-id="08f01-115">The default setting for this element is False.</span></span>

<span data-ttu-id="08f01-116">針對 c + + 開發，這項資訊是透過 [**ITaskSettings2：： UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="08f01-116">For C++ development, this information is accessed through the [**ITaskSettings2::UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) property.</span></span>

## <a name="examples"></a><span data-ttu-id="08f01-117">範例</span><span class="sxs-lookup"><span data-stu-id="08f01-117">Examples</span></span>

<span data-ttu-id="08f01-118">下列 XML 會定義設定專案，指定將用來執行這項工作的統一排程引擎。</span><span class="sxs-lookup"><span data-stu-id="08f01-118">The following XML defines a settings element that specifies that the Unified Scheduling Engine will be used to run this task.</span></span>


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="08f01-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="08f01-119">Requirements</span></span>



| <span data-ttu-id="08f01-120">需求</span><span class="sxs-lookup"><span data-stu-id="08f01-120">Requirement</span></span> | <span data-ttu-id="08f01-121">值</span><span class="sxs-lookup"><span data-stu-id="08f01-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="08f01-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08f01-122">Minimum supported client</span></span><br/> | <span data-ttu-id="08f01-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08f01-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="08f01-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08f01-124">Minimum supported server</span></span><br/> | <span data-ttu-id="08f01-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08f01-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08f01-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08f01-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f01-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="08f01-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






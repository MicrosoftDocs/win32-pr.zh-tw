---
title: DisallowStartIfOnBatteries (settingsType) 元素
description: 指定當電腦以電池執行時，工作將不會啟動。
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- DisallowStartIfOnBatteries 元素工作排程器
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686564"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a><span data-ttu-id="c8b46-104">DisallowStartIfOnBatteries (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="c8b46-104">DisallowStartIfOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="c8b46-105">指定當電腦以電池執行時，工作將不會啟動。</span><span class="sxs-lookup"><span data-stu-id="c8b46-105">Specifies that the task will not be started if the computer is running on batteries.</span></span>

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

<span data-ttu-id="c8b46-106">**DisallowStartIfOnBatteries** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c8b46-106">The **DisallowStartIfOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c8b46-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c8b46-107">Parent element</span></span>



| <span data-ttu-id="c8b46-108">元素</span><span class="sxs-lookup"><span data-stu-id="c8b46-108">Element</span></span>                                                           | <span data-ttu-id="c8b46-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c8b46-109">Derived from</span></span>                                                         | <span data-ttu-id="c8b46-110">Description</span><span class="sxs-lookup"><span data-stu-id="c8b46-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8b46-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="c8b46-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c8b46-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c8b46-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c8b46-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="c8b46-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c8b46-114">備註</span><span class="sxs-lookup"><span data-stu-id="c8b46-114">Remarks</span></span>

<span data-ttu-id="c8b46-115">此元素的預設設定為 True。</span><span class="sxs-lookup"><span data-stu-id="c8b46-115">The default setting for this element is True.</span></span>

<span data-ttu-id="c8b46-116">針對腳本開發，這項資訊是透過 [**TaskSettings DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="c8b46-116">For scripting development, this information is accessed through the [**TaskSettings.DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) property.</span></span>

<span data-ttu-id="c8b46-117">針對 c + + 開發，此資訊可透過 [**ITaskSettings：:D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="c8b46-117">For C++ development, this information is accessed through the [**ITaskSettings::DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c8b46-118">範例</span><span class="sxs-lookup"><span data-stu-id="c8b46-118">Examples</span></span>

<span data-ttu-id="c8b46-119">下列 XML 定義的設定元素不允許在電腦以電池執行時執行工作。</span><span class="sxs-lookup"><span data-stu-id="c8b46-119">The following XML defines a settings element that does not allow the task to run if the computer is running on batteries.</span></span>


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="c8b46-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8b46-120">Requirements</span></span>



| <span data-ttu-id="c8b46-121">需求</span><span class="sxs-lookup"><span data-stu-id="c8b46-121">Requirement</span></span> | <span data-ttu-id="c8b46-122">值</span><span class="sxs-lookup"><span data-stu-id="c8b46-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8b46-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8b46-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b46-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8b46-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c8b46-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8b46-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b46-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8b46-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8b46-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8b46-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b46-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c8b46-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






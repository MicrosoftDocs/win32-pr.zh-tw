---
title: StopIfGoingOnBatteries (settingsType) 元素
description: 指定當電腦進入電池時，工作將會停止。
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- StopIfGoingOnBatteries 元素工作排程器
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967961"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a><span data-ttu-id="9e490-104">StopIfGoingOnBatteries (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="9e490-104">StopIfGoingOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="9e490-105">指定當電腦進入電池時，工作將會停止。</span><span class="sxs-lookup"><span data-stu-id="9e490-105">Specifies that the task will be stopped if the computer is going onto batteries.</span></span>

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="9e490-106">**StopIfGoingOnBatteries** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="9e490-106">The **StopIfGoingOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9e490-107">父元素</span><span class="sxs-lookup"><span data-stu-id="9e490-107">Parent element</span></span>



| <span data-ttu-id="9e490-108">元素</span><span class="sxs-lookup"><span data-stu-id="9e490-108">Element</span></span>                                                           | <span data-ttu-id="9e490-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="9e490-109">Derived from</span></span>                                                         | <span data-ttu-id="9e490-110">Description</span><span class="sxs-lookup"><span data-stu-id="9e490-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e490-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="9e490-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="9e490-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="9e490-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="9e490-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="9e490-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9e490-114">備註</span><span class="sxs-lookup"><span data-stu-id="9e490-114">Remarks</span></span>

<span data-ttu-id="9e490-115">此元素的預設設定為 False。</span><span class="sxs-lookup"><span data-stu-id="9e490-115">The default setting for this element is False.</span></span> <span data-ttu-id="9e490-116">請注意，預設值已與舊版工作排程器變更。</span><span class="sxs-lookup"><span data-stu-id="9e490-116">Note that the default value has changed from previous versions of Task Scheduler.</span></span>

<span data-ttu-id="9e490-117">針對腳本開發，此設定會使用 [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="9e490-117">For scripting development, this setting is specified using the [**TaskSettings.StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) property.</span></span>

<span data-ttu-id="9e490-118">針對 c + + 開發，此設定會使用 [**ITaskSettings：： StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="9e490-118">For C++ development, this setting is specified using the [**ITaskSettings::StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9e490-119">範例</span><span class="sxs-lookup"><span data-stu-id="9e490-119">Examples</span></span>

<span data-ttu-id="9e490-120">下列 XML 會定義允許工作的永久終止的設定元素。</span><span class="sxs-lookup"><span data-stu-id="9e490-120">The following XML defines a settings element that allows a hard termination of the task.</span></span>


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="9e490-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e490-121">Requirements</span></span>



| <span data-ttu-id="9e490-122">需求</span><span class="sxs-lookup"><span data-stu-id="9e490-122">Requirement</span></span> | <span data-ttu-id="9e490-123">值</span><span class="sxs-lookup"><span data-stu-id="9e490-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e490-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e490-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e490-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e490-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e490-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e490-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e490-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e490-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e490-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e490-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e490-129">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="9e490-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






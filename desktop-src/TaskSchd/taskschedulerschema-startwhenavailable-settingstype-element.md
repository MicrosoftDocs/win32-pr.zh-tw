---
title: StartWhenAvailable (settingsType) 元素
description: 指定工作排程器可以在經過排程的時間之後隨時啟動工作。
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- StartWhenAvailable 元素工作排程器
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934070"
---
# <a name="startwhenavailable-settingstype-element"></a><span data-ttu-id="c6c81-104">StartWhenAvailable (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="c6c81-104">StartWhenAvailable (settingsType) Element</span></span>

<span data-ttu-id="c6c81-105">指定工作排程器可以在經過排程的時間之後隨時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="c6c81-105">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="c6c81-106">**StartWhenAvailable** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c6c81-106">The **StartWhenAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c6c81-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c6c81-107">Parent element</span></span>



| <span data-ttu-id="c6c81-108">元素</span><span class="sxs-lookup"><span data-stu-id="c6c81-108">Element</span></span>                                                           | <span data-ttu-id="c6c81-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c6c81-109">Derived from</span></span>                                                         | <span data-ttu-id="c6c81-110">Description</span><span class="sxs-lookup"><span data-stu-id="c6c81-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6c81-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="c6c81-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c6c81-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c6c81-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c6c81-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="c6c81-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c6c81-114">備註</span><span class="sxs-lookup"><span data-stu-id="c6c81-114">Remarks</span></span>

<span data-ttu-id="c6c81-115">這個屬性只適用于計時工作。</span><span class="sxs-lookup"><span data-stu-id="c6c81-115">This property applies only to timed tasks.</span></span>

<span data-ttu-id="c6c81-116">針對 c + + 開發，請參閱 [**ITaskSettings 的 StartWhenAvailable 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable)。</span><span class="sxs-lookup"><span data-stu-id="c6c81-116">For C++ development, see [**StartWhenAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span></span>

<span data-ttu-id="c6c81-117">如需腳本開發，請參閱 [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md)。</span><span class="sxs-lookup"><span data-stu-id="c6c81-117">For script development, see [**TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c6c81-118">範例</span><span class="sxs-lookup"><span data-stu-id="c6c81-118">Examples</span></span>

<span data-ttu-id="c6c81-119">下列 XML 會定義 settings 元素，讓工作排程器在工作可用時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="c6c81-119">The following XML defines a settings element that allows the Task Scheduler to start the task when it is available.</span></span>


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="c6c81-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6c81-120">Requirements</span></span>



| <span data-ttu-id="c6c81-121">需求</span><span class="sxs-lookup"><span data-stu-id="c6c81-121">Requirement</span></span> | <span data-ttu-id="c6c81-122">值</span><span class="sxs-lookup"><span data-stu-id="c6c81-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6c81-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6c81-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c81-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c81-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6c81-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6c81-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c81-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c81-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6c81-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6c81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c81-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c6c81-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






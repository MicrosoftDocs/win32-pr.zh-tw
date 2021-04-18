---
title: 已啟用 (settingsType) 元素
description: 指定已啟用工作。 只有當這項設定為 True 時，才能執行此工作。
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Enabled 元素工作排程器
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965524"
---
# <a name="enabled-settingstype-element"></a><span data-ttu-id="c5393-105">已啟用 (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="c5393-105">Enabled (settingsType) Element</span></span>

<span data-ttu-id="c5393-106">指定已啟用工作。</span><span class="sxs-lookup"><span data-stu-id="c5393-106">Specifies that the task is enabled.</span></span> <span data-ttu-id="c5393-107">只有當這項設定為 True 時，才能執行此工作。</span><span class="sxs-lookup"><span data-stu-id="c5393-107">The task can be performed only when this setting is True.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

<span data-ttu-id="c5393-108">**Enabled** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c5393-108">The **Enabled** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c5393-109">父元素</span><span class="sxs-lookup"><span data-stu-id="c5393-109">Parent element</span></span>



| <span data-ttu-id="c5393-110">元素</span><span class="sxs-lookup"><span data-stu-id="c5393-110">Element</span></span>                                                           | <span data-ttu-id="c5393-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="c5393-111">Derived from</span></span>                                                         | <span data-ttu-id="c5393-112">Description</span><span class="sxs-lookup"><span data-stu-id="c5393-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5393-113">**設定**</span><span class="sxs-lookup"><span data-stu-id="c5393-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c5393-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c5393-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c5393-115">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="c5393-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c5393-116">備註</span><span class="sxs-lookup"><span data-stu-id="c5393-116">Remarks</span></span>

<span data-ttu-id="c5393-117">針對 c + + 開發，請參閱 [**ITaskSettings 的 Enabled 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled)。</span><span class="sxs-lookup"><span data-stu-id="c5393-117">For C++ development, see [**Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span></span>

<span data-ttu-id="c5393-118">如需腳本開發，請參閱 [**TaskSettings。**](tasksettings-enabled.md)</span><span class="sxs-lookup"><span data-stu-id="c5393-118">For script development, see [**TaskSettings.Enabled**](tasksettings-enabled.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c5393-119">範例</span><span class="sxs-lookup"><span data-stu-id="c5393-119">Examples</span></span>

<span data-ttu-id="c5393-120">如需已啟用之工作的完整 XML 範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="c5393-120">For a complete example of the XML for a task that is enabled, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5393-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5393-121">Requirements</span></span>



| <span data-ttu-id="c5393-122">需求</span><span class="sxs-lookup"><span data-stu-id="c5393-122">Requirement</span></span> | <span data-ttu-id="c5393-123">值</span><span class="sxs-lookup"><span data-stu-id="c5393-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5393-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5393-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c5393-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5393-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5393-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5393-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c5393-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5393-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






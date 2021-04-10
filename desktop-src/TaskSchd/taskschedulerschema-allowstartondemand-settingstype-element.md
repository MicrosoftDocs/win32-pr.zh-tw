---
title: AllowStartOnDemand (settingsType) 元素
description: 指定可使用 [執行] 命令或內容功能表來啟動工作。
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- AllowStartOnDemand 元素工作排程器
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934073"
---
# <a name="allowstartondemand-settingstype-element"></a><span data-ttu-id="5fed2-104">AllowStartOnDemand (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="5fed2-104">AllowStartOnDemand (settingsType) Element</span></span>

<span data-ttu-id="5fed2-105">指定可使用 [執行] 命令或內容功能表來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="5fed2-105">Specifies that the task can be started using either the Run command or the Context menu.</span></span>

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="5fed2-106">**AllowStartOnDemand** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="5fed2-106">The **AllowStartOnDemand** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5fed2-107">父元素</span><span class="sxs-lookup"><span data-stu-id="5fed2-107">Parent element</span></span>



| <span data-ttu-id="5fed2-108">元素</span><span class="sxs-lookup"><span data-stu-id="5fed2-108">Element</span></span>                                                           | <span data-ttu-id="5fed2-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="5fed2-109">Derived from</span></span>                                                         | <span data-ttu-id="5fed2-110">Description</span><span class="sxs-lookup"><span data-stu-id="5fed2-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fed2-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="5fed2-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="5fed2-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="5fed2-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="5fed2-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="5fed2-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5fed2-114">備註</span><span class="sxs-lookup"><span data-stu-id="5fed2-114">Remarks</span></span>

<span data-ttu-id="5fed2-115">當此專案設定為 True 時，可以在任何觸發程式啟動工作時，獨立啟動工作。</span><span class="sxs-lookup"><span data-stu-id="5fed2-115">When this element is set to True, the task can be started independently of when any triggers start the task.</span></span>

<span data-ttu-id="5fed2-116">針對 c + + 開發，請參閱 [**ITaskSettings 的 AllowDemandStart 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart)。</span><span class="sxs-lookup"><span data-stu-id="5fed2-116">For C++ development, see the [**AllowDemandStart property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span></span>

<span data-ttu-id="5fed2-117">如需腳本開發，請參閱 [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md)。</span><span class="sxs-lookup"><span data-stu-id="5fed2-117">For script development, see [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5fed2-118">範例</span><span class="sxs-lookup"><span data-stu-id="5fed2-118">Examples</span></span>

<span data-ttu-id="5fed2-119">如需允許要求開始之工作的 XML 完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="5fed2-119">For a complete example of the XML for a task that allows demand start, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fed2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fed2-120">Requirements</span></span>



| <span data-ttu-id="5fed2-121">需求</span><span class="sxs-lookup"><span data-stu-id="5fed2-121">Requirement</span></span> | <span data-ttu-id="5fed2-122">值</span><span class="sxs-lookup"><span data-stu-id="5fed2-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5fed2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fed2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5fed2-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fed2-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5fed2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fed2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5fed2-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fed2-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fed2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fed2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fed2-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="5fed2-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






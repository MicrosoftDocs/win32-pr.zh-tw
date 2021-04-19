---
title: AllowHardTerminate (settingsType) 元素
description: 指定可以使用 TerminateProcess 終止工作。
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- AllowHardTerminate (settingsType) 元素工作排程器
- AllowHardTerminate 元素工作排程器
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965071"
---
# <a name="allowhardterminate-settingstype-element"></a><span data-ttu-id="318d0-105">AllowHardTerminate (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="318d0-105">AllowHardTerminate (settingsType) Element</span></span>

<span data-ttu-id="318d0-106">指定可以使用 TerminateProcess 終止工作。</span><span class="sxs-lookup"><span data-stu-id="318d0-106">Specifies that the task may be terminated using TerminateProcess.</span></span>

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="318d0-107">**AllowHardTerminate** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="318d0-107">The **AllowHardTerminate** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="318d0-108">父元素</span><span class="sxs-lookup"><span data-stu-id="318d0-108">Parent element</span></span>



| <span data-ttu-id="318d0-109">元素</span><span class="sxs-lookup"><span data-stu-id="318d0-109">Element</span></span>                                                           | <span data-ttu-id="318d0-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="318d0-110">Derived from</span></span>                                                 | <span data-ttu-id="318d0-111">Description</span><span class="sxs-lookup"><span data-stu-id="318d0-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="318d0-112">**設定**</span><span class="sxs-lookup"><span data-stu-id="318d0-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="318d0-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="318d0-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="318d0-114">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="318d0-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="318d0-115">備註</span><span class="sxs-lookup"><span data-stu-id="318d0-115">Remarks</span></span>

<span data-ttu-id="318d0-116">針對 c + + 開發，請參閱 [**ITaskSettings 的 AllowHardTerminate 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate)。</span><span class="sxs-lookup"><span data-stu-id="318d0-116">For C++ development, see the [**AllowHardTerminate property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span></span>

<span data-ttu-id="318d0-117">如需腳本開發，請參閱 [**TaskSettings. AllowHardTerminate**](tasksettings-allowhardterminate.md)。</span><span class="sxs-lookup"><span data-stu-id="318d0-117">For script development, see [**TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).</span></span>

## <a name="examples"></a><span data-ttu-id="318d0-118">範例</span><span class="sxs-lookup"><span data-stu-id="318d0-118">Examples</span></span>

<span data-ttu-id="318d0-119">如需允許硬終止之工作的 XML 完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="318d0-119">For a complete example of the XML for a task that allows hard termination, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="318d0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="318d0-120">Requirements</span></span>



| <span data-ttu-id="318d0-121">需求</span><span class="sxs-lookup"><span data-stu-id="318d0-121">Requirement</span></span> | <span data-ttu-id="318d0-122">值</span><span class="sxs-lookup"><span data-stu-id="318d0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="318d0-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="318d0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="318d0-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="318d0-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="318d0-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="318d0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="318d0-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="318d0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="318d0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="318d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318d0-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="318d0-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






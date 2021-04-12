---
title: RunOnlyIfIdle (settingsType) 元素
description: 指定只有當電腦處於閒置狀態時，才會執行工作。
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- RunOnlyIfIdle 元素工作排程器
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025357"
---
# <a name="runonlyifidle-settingstype-element"></a><span data-ttu-id="4b601-104">RunOnlyIfIdle (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="4b601-104">RunOnlyIfIdle (settingsType) Element</span></span>

<span data-ttu-id="4b601-105">指定只有當電腦處於閒置狀態時，才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="4b601-105">Specifies that the task is run only when the computer is in an idle state.</span></span>

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

<span data-ttu-id="4b601-106">**RunOnlyIfIdle** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="4b601-106">The **RunOnlyIfIdle** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4b601-107">父元素</span><span class="sxs-lookup"><span data-stu-id="4b601-107">Parent element</span></span>



| <span data-ttu-id="4b601-108">元素</span><span class="sxs-lookup"><span data-stu-id="4b601-108">Element</span></span>                                                           | <span data-ttu-id="4b601-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="4b601-109">Derived from</span></span>                                                         | <span data-ttu-id="4b601-110">Description</span><span class="sxs-lookup"><span data-stu-id="4b601-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b601-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="4b601-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="4b601-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="4b601-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="4b601-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="4b601-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4b601-114">備註</span><span class="sxs-lookup"><span data-stu-id="4b601-114">Remarks</span></span>

<span data-ttu-id="4b601-115">針對 c + + 開發，請參閱 [**ITaskSettings 的 RunOnlyIfIdle 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle)。</span><span class="sxs-lookup"><span data-stu-id="4b601-115">For C++ development, see [**RunOnlyIfIdle Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span></span>

<span data-ttu-id="4b601-116">如需腳本開發，請參閱 [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md)。</span><span class="sxs-lookup"><span data-stu-id="4b601-116">For script development, see [**TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b601-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b601-117">Requirements</span></span>



| <span data-ttu-id="4b601-118">需求</span><span class="sxs-lookup"><span data-stu-id="4b601-118">Requirement</span></span> | <span data-ttu-id="4b601-119">值</span><span class="sxs-lookup"><span data-stu-id="4b601-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b601-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b601-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b601-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b601-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b601-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b601-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b601-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b601-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b601-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b601-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b601-125">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="4b601-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4b601-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="4b601-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






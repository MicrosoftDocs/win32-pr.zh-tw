---
title: Volatile 元素
description: 指出每次 Windows 啟動時是否自動停用工作。
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Volatile 元素工作排程器
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686361"
---
# <a name="volatile-element"></a><span data-ttu-id="c5b3b-104">Volatile 元素</span><span class="sxs-lookup"><span data-stu-id="c5b3b-104">Volatile Element</span></span>

<span data-ttu-id="c5b3b-105">指出每次 Windows 啟動時是否自動停用工作。</span><span class="sxs-lookup"><span data-stu-id="c5b3b-105">Indicates whether the task is automatically disabled every time Windows starts.</span></span>

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

<span data-ttu-id="c5b3b-106">**Volatile** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c5b3b-106">The **Volatile** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c5b3b-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c5b3b-107">Parent element</span></span>



| <span data-ttu-id="c5b3b-108">元素</span><span class="sxs-lookup"><span data-stu-id="c5b3b-108">Element</span></span>                                                           | <span data-ttu-id="c5b3b-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c5b3b-109">Derived from</span></span> | <span data-ttu-id="c5b3b-110">Description</span><span class="sxs-lookup"><span data-stu-id="c5b3b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5b3b-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="c5b3b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) |              | <span data-ttu-id="c5b3b-112">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="c5b3b-112">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c5b3b-113">備註</span><span class="sxs-lookup"><span data-stu-id="c5b3b-113">Remarks</span></span>

<span data-ttu-id="c5b3b-114">若是 c + + 程式設計，則會使用 [**ITaskSettings3：： Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) 屬性來指定此閒置設定。</span><span class="sxs-lookup"><span data-stu-id="c5b3b-114">For C++ programming, this idle setting is specified using the [**ITaskSettings3::Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b3b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5b3b-115">Requirements</span></span>



| <span data-ttu-id="c5b3b-116">需求</span><span class="sxs-lookup"><span data-stu-id="c5b3b-116">Requirement</span></span> | <span data-ttu-id="c5b3b-117">值</span><span class="sxs-lookup"><span data-stu-id="c5b3b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5b3b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5b3b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b3b-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5b3b-119">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="c5b3b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5b3b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b3b-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5b3b-121">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5b3b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5b3b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b3b-123">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c5b3b-123">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c5b3b-124">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c5b3b-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






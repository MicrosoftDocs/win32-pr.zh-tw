---
title: StopOnIdleEnd (idleSettingsType) 元素
description: 指定如果閒置條件在工作完成之前結束，工作排程器將停止工作。
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- StopOnIdleEnd 元素工作排程器
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934977"
---
# <a name="stoponidleend-idlesettingstype-element"></a><span data-ttu-id="057ee-104">StopOnIdleEnd (idleSettingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="057ee-104">StopOnIdleEnd (idleSettingsType) Element</span></span>

<span data-ttu-id="057ee-105">指定如果閒置條件在工作完成之前結束，工作排程器將停止工作。</span><span class="sxs-lookup"><span data-stu-id="057ee-105">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span>

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="057ee-106">**StopOnIdleEnd** 元素是由 [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="057ee-106">The **StopOnIdleEnd** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="057ee-107">父元素</span><span class="sxs-lookup"><span data-stu-id="057ee-107">Parent element</span></span>



| <span data-ttu-id="057ee-108">元素</span><span class="sxs-lookup"><span data-stu-id="057ee-108">Element</span></span>                                                                       | <span data-ttu-id="057ee-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="057ee-109">Derived from</span></span>                                                                 | <span data-ttu-id="057ee-110">Description</span><span class="sxs-lookup"><span data-stu-id="057ee-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="057ee-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="057ee-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="057ee-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="057ee-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="057ee-113">指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="057ee-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="057ee-114">備註</span><span class="sxs-lookup"><span data-stu-id="057ee-114">Remarks</span></span>

<span data-ttu-id="057ee-115">針對 c + + 開發，請參閱 [**IIdleSettings 的 StopOnIdleEnd 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend)。</span><span class="sxs-lookup"><span data-stu-id="057ee-115">For C++ development, see [**StopOnIdleEnd Property of IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span></span>

<span data-ttu-id="057ee-116">如需腳本開發，請參閱 [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md)。</span><span class="sxs-lookup"><span data-stu-id="057ee-116">For script development, see [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).</span></span>

## <a name="examples"></a><span data-ttu-id="057ee-117">範例</span><span class="sxs-lookup"><span data-stu-id="057ee-117">Examples</span></span>

<span data-ttu-id="057ee-118">下列 XML 定義閒置設定，指出當閒置條件結束時，不應執行工作。</span><span class="sxs-lookup"><span data-stu-id="057ee-118">The following XML defines an idle setting that indicates the task should not be performed when the idle condition ends.</span></span>


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="057ee-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="057ee-119">Requirements</span></span>



| <span data-ttu-id="057ee-120">需求</span><span class="sxs-lookup"><span data-stu-id="057ee-120">Requirement</span></span> | <span data-ttu-id="057ee-121">值</span><span class="sxs-lookup"><span data-stu-id="057ee-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="057ee-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="057ee-122">Minimum supported client</span></span><br/> | <span data-ttu-id="057ee-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="057ee-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="057ee-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="057ee-124">Minimum supported server</span></span><br/> | <span data-ttu-id="057ee-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="057ee-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="057ee-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="057ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057ee-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="057ee-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






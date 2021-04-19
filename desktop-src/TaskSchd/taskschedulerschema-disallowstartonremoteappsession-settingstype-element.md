---
title: DisallowStartOnRemoteAppSession (settingsType) 元素
description: 指定當觸發在本機 (鐵路) 會話的遠端應用程式中執行時，工作將不會啟動。
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- DisallowStartOnRemoteAppSession 元素工作排程器
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969573"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a><span data-ttu-id="1eba8-104">DisallowStartOnRemoteAppSession (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="1eba8-104">DisallowStartOnRemoteAppSession (settingsType) Element</span></span>

<span data-ttu-id="1eba8-105">指定當觸發在本機 (鐵路) 會話的遠端應用程式中執行時，工作將不會啟動。</span><span class="sxs-lookup"><span data-stu-id="1eba8-105">Specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span>

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="1eba8-106">**DisallowStartOnRemoteAppSession** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="1eba8-106">The **DisallowStartOnRemoteAppSession** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1eba8-107">父元素</span><span class="sxs-lookup"><span data-stu-id="1eba8-107">Parent element</span></span>



| <span data-ttu-id="1eba8-108">元素</span><span class="sxs-lookup"><span data-stu-id="1eba8-108">Element</span></span>                                                           | <span data-ttu-id="1eba8-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="1eba8-109">Derived from</span></span>                                                         | <span data-ttu-id="1eba8-110">Description</span><span class="sxs-lookup"><span data-stu-id="1eba8-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1eba8-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="1eba8-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1eba8-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="1eba8-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1eba8-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="1eba8-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1eba8-114">備註</span><span class="sxs-lookup"><span data-stu-id="1eba8-114">Remarks</span></span>

<span data-ttu-id="1eba8-115">此元素的預設設定為 False。</span><span class="sxs-lookup"><span data-stu-id="1eba8-115">The default setting for this element is False.</span></span>

<span data-ttu-id="1eba8-116">針對 c + + 開發，此資訊可透過 [**ITaskSettings2：:D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="1eba8-116">For C++ development, this information is accessed through the [**ITaskSettings2::DisallowStartOnRemoteAppSession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1eba8-117">範例</span><span class="sxs-lookup"><span data-stu-id="1eba8-117">Examples</span></span>

<span data-ttu-id="1eba8-118">下列 XML 會定義一個設定專案，如果工作觸發在滑軌會話中執行，則不允許啟動工作。</span><span class="sxs-lookup"><span data-stu-id="1eba8-118">The following XML defines a settings element that does not allow the task to start if the task is triggered to run in a RAIL session.</span></span>


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="1eba8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eba8-119">Requirements</span></span>



| <span data-ttu-id="1eba8-120">需求</span><span class="sxs-lookup"><span data-stu-id="1eba8-120">Requirement</span></span> | <span data-ttu-id="1eba8-121">值</span><span class="sxs-lookup"><span data-stu-id="1eba8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1eba8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1eba8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1eba8-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eba8-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1eba8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1eba8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1eba8-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eba8-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1eba8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1eba8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eba8-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="1eba8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






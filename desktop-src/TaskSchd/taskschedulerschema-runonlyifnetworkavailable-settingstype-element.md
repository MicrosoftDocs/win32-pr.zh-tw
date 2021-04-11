---
title: RunOnlyIfNetworkAvailable (settingsType) 元素
description: 指定只有在有可用的網路時，工作排程器才會執行工作。
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- RunOnlyIfNetworkAvailable 元素工作排程器
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934867"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a><span data-ttu-id="a5347-104">RunOnlyIfNetworkAvailable (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="a5347-104">RunOnlyIfNetworkAvailable (settingsType) Element</span></span>

<span data-ttu-id="a5347-105">指定只有在有可用的網路時，工作排程器才會執行工作。</span><span class="sxs-lookup"><span data-stu-id="a5347-105">Specifies that the Task Scheduler will run the task only when a network is available.</span></span>

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="a5347-106">**RunOnlyIfNetworkAvailable** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="a5347-106">The **RunOnlyIfNetworkAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a5347-107">父元素</span><span class="sxs-lookup"><span data-stu-id="a5347-107">Parent element</span></span>



| <span data-ttu-id="a5347-108">元素</span><span class="sxs-lookup"><span data-stu-id="a5347-108">Element</span></span>                                                           | <span data-ttu-id="a5347-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="a5347-109">Derived from</span></span>                                                         | <span data-ttu-id="a5347-110">Description</span><span class="sxs-lookup"><span data-stu-id="a5347-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5347-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="a5347-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="a5347-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="a5347-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="a5347-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="a5347-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a5347-114">備註</span><span class="sxs-lookup"><span data-stu-id="a5347-114">Remarks</span></span>

<span data-ttu-id="a5347-115">針對 c + + 開發，請參閱 [**ITaskSettings 的 RunOnlyIfNetworkAvailable 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable)。</span><span class="sxs-lookup"><span data-stu-id="a5347-115">For C++ development, see [**RunOnlyIfNetworkAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span></span>

<span data-ttu-id="a5347-116">如需腳本開發，請參閱 [**TaskSettings. RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)。</span><span class="sxs-lookup"><span data-stu-id="a5347-116">For script development, see [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a5347-117">範例</span><span class="sxs-lookup"><span data-stu-id="a5347-117">Examples</span></span>

<span data-ttu-id="a5347-118">下列 XML 定義的設定元素，只有在有可用的網路時，才會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="a5347-118">The following XML defines a settings element that allows the task to start only if a network is available.</span></span>


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="a5347-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5347-119">Requirements</span></span>



| <span data-ttu-id="a5347-120">需求</span><span class="sxs-lookup"><span data-stu-id="a5347-120">Requirement</span></span> | <span data-ttu-id="a5347-121">值</span><span class="sxs-lookup"><span data-stu-id="a5347-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5347-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5347-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a5347-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5347-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5347-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5347-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a5347-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5347-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5347-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5347-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5347-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="a5347-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






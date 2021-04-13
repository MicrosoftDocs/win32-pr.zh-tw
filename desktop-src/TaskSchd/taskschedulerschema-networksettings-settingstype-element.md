---
title: NetworkSettings (settingsType) 元素
description: 包含工作排程器服務用來取得網路設定檔的設定。 當 RunOnlyIfNetworkAvailable 元素設定為 True 時，工作排程器服務會檢查此網路的可用性。
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- NetworkSettings 元素工作排程器
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465805"
---
# <a name="networksettings-settingstype-element"></a><span data-ttu-id="49525-105">NetworkSettings (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="49525-105">NetworkSettings (settingsType) Element</span></span>

<span data-ttu-id="49525-106">包含工作排程器服務用來取得網路設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="49525-106">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="49525-107">當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。</span><span class="sxs-lookup"><span data-stu-id="49525-107">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span>

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="49525-108">**NetworkSettings** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="49525-108">The **NetworkSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="49525-109">父元素</span><span class="sxs-lookup"><span data-stu-id="49525-109">Parent element</span></span>



| <span data-ttu-id="49525-110">元素</span><span class="sxs-lookup"><span data-stu-id="49525-110">Element</span></span>                                                                      | <span data-ttu-id="49525-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="49525-111">Derived from</span></span>                                                         | <span data-ttu-id="49525-112">Description</span><span class="sxs-lookup"><span data-stu-id="49525-112">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="49525-113">**設定 (taskType)**</span><span class="sxs-lookup"><span data-stu-id="49525-113">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="49525-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="49525-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="49525-115">指定工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="49525-115">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="49525-116">備註</span><span class="sxs-lookup"><span data-stu-id="49525-116">Remarks</span></span>

<span data-ttu-id="49525-117">針對 c + + 開發，請參閱 [**ITaskSettings 的 NetworkSettings 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings)。</span><span class="sxs-lookup"><span data-stu-id="49525-117">For C++ development, see [**NetworkSettings Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span></span>

<span data-ttu-id="49525-118">如需腳本開發，請參閱 [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md)。</span><span class="sxs-lookup"><span data-stu-id="49525-118">For script development, see [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49525-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="49525-119">Requirements</span></span>



| <span data-ttu-id="49525-120">需求</span><span class="sxs-lookup"><span data-stu-id="49525-120">Requirement</span></span> | <span data-ttu-id="49525-121">值</span><span class="sxs-lookup"><span data-stu-id="49525-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49525-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49525-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49525-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49525-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49525-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49525-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49525-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49525-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






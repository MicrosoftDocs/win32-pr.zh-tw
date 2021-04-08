---
title: NetworkProfileName (settingsType) 元素
description: 包含網路設定檔的名稱。 當 RunOnlyIfNetworkAvailable 元素設定為 True 時，工作排程器服務會檢查此網路的可用性。 此名稱會用於顯示用途。
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- NetworkProfileName 元素工作排程器
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686072"
---
# <a name="networkprofilename-settingstype-element"></a><span data-ttu-id="3d478-106">NetworkProfileName (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="3d478-106">NetworkProfileName (settingsType) Element</span></span>

<span data-ttu-id="3d478-107">包含網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d478-107">Contains the name of a network profile.</span></span> <span data-ttu-id="3d478-108">當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。</span><span class="sxs-lookup"><span data-stu-id="3d478-108">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="3d478-109">此名稱會用於顯示用途。</span><span class="sxs-lookup"><span data-stu-id="3d478-109">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="3d478-110">**NetworkProfileName** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="3d478-110">The **NetworkProfileName** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3d478-111">父元素</span><span class="sxs-lookup"><span data-stu-id="3d478-111">Parent element</span></span>



| <span data-ttu-id="3d478-112">元素</span><span class="sxs-lookup"><span data-stu-id="3d478-112">Element</span></span>                                                                      | <span data-ttu-id="3d478-113">衍生自</span><span class="sxs-lookup"><span data-stu-id="3d478-113">Derived from</span></span>                                                         | <span data-ttu-id="3d478-114">Description</span><span class="sxs-lookup"><span data-stu-id="3d478-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d478-115">**設定 (taskType)**</span><span class="sxs-lookup"><span data-stu-id="3d478-115">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="3d478-116">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="3d478-116">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="3d478-117">指定工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="3d478-117">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3d478-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d478-118">Requirements</span></span>



| <span data-ttu-id="3d478-119">需求</span><span class="sxs-lookup"><span data-stu-id="3d478-119">Requirement</span></span> | <span data-ttu-id="3d478-120">值</span><span class="sxs-lookup"><span data-stu-id="3d478-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3d478-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d478-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d478-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d478-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3d478-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d478-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d478-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d478-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






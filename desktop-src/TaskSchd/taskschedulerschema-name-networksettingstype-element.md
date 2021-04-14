---
title: NetworkSettingsType) 專案的名稱 (
description: 包含網路設定檔的名稱。 此名稱會用於顯示用途。
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Name 元素工作排程器
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508771"
---
# <a name="name-networksettingstype-element"></a><span data-ttu-id="03342-105">NetworkSettingsType) 專案的名稱 (</span><span class="sxs-lookup"><span data-stu-id="03342-105">Name (networkSettingsType) Element</span></span>

<span data-ttu-id="03342-106">包含網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="03342-106">Contains the name of a network profile.</span></span> <span data-ttu-id="03342-107">此名稱會用於顯示用途。</span><span class="sxs-lookup"><span data-stu-id="03342-107">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

<span data-ttu-id="03342-108">**Name** 元素是由 [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="03342-108">The **Name** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="03342-109">父元素</span><span class="sxs-lookup"><span data-stu-id="03342-109">Parent element</span></span>



| <span data-ttu-id="03342-110">元素</span><span class="sxs-lookup"><span data-stu-id="03342-110">Element</span></span>                                                                                            | <span data-ttu-id="03342-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="03342-111">Derived from</span></span>                                                                       | <span data-ttu-id="03342-112">Description</span><span class="sxs-lookup"><span data-stu-id="03342-112">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03342-113">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="03342-113">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="03342-114">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="03342-114">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="03342-115">包含工作排程器服務用來取得網路設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="03342-115">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="03342-116">當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。</span><span class="sxs-lookup"><span data-stu-id="03342-116">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="03342-117">備註</span><span class="sxs-lookup"><span data-stu-id="03342-117">Remarks</span></span>

<span data-ttu-id="03342-118">針對 c + + 開發，請參閱 [**INetworkSettings 的 Name 屬性**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name)。</span><span class="sxs-lookup"><span data-stu-id="03342-118">For C++ development, see [**Name Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span></span>

<span data-ttu-id="03342-119">如需腳本開發，請參閱 [**NetworkSettings.Name**](networksettings-name.md)。</span><span class="sxs-lookup"><span data-stu-id="03342-119">For script development, see [**NetworkSettings.Name**](networksettings-name.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03342-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="03342-120">Requirements</span></span>



| <span data-ttu-id="03342-121">需求</span><span class="sxs-lookup"><span data-stu-id="03342-121">Requirement</span></span> | <span data-ttu-id="03342-122">值</span><span class="sxs-lookup"><span data-stu-id="03342-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="03342-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03342-123">Minimum supported client</span></span><br/> | <span data-ttu-id="03342-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03342-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="03342-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03342-125">Minimum supported server</span></span><br/> | <span data-ttu-id="03342-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03342-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






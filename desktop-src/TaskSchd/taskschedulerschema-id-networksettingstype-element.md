---
title: Id (networkSettingsType) 元素
description: 包含可識別網路設定檔的 GUID 值。
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Id 元素工作排程器
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106368"
---
# <a name="id-networksettingstype-element"></a><span data-ttu-id="ccd11-104">Id (networkSettingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="ccd11-104">Id (networkSettingsType) Element</span></span>

<span data-ttu-id="ccd11-105">包含可識別網路設定檔的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="ccd11-105">Contains a GUID value that identifies a network profile.</span></span>

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

<span data-ttu-id="ccd11-106">**Id** 元素是由 [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="ccd11-106">The **Id** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ccd11-107">父元素</span><span class="sxs-lookup"><span data-stu-id="ccd11-107">Parent element</span></span>



| <span data-ttu-id="ccd11-108">元素</span><span class="sxs-lookup"><span data-stu-id="ccd11-108">Element</span></span>                                                                                            | <span data-ttu-id="ccd11-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="ccd11-109">Derived from</span></span>                                                                       | <span data-ttu-id="ccd11-110">Description</span><span class="sxs-lookup"><span data-stu-id="ccd11-110">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccd11-111">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="ccd11-111">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="ccd11-112">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="ccd11-112">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="ccd11-113">包含工作排程器服務用來取得網路設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="ccd11-113">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="ccd11-114">當 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素設定為 **True** 時，工作排程器服務會檢查此網路的可用性。</span><span class="sxs-lookup"><span data-stu-id="ccd11-114">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ccd11-115">備註</span><span class="sxs-lookup"><span data-stu-id="ccd11-115">Remarks</span></span>

<span data-ttu-id="ccd11-116">針對 c + + 開發，請參閱 [**INetworkSettings 的 Id 屬性**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id)。</span><span class="sxs-lookup"><span data-stu-id="ccd11-116">For C++ development, see [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span></span>

<span data-ttu-id="ccd11-117">如需腳本開發，請參閱 [**NetworkSettings.Id**](networksettings-id.md)。</span><span class="sxs-lookup"><span data-stu-id="ccd11-117">For script development, see [**NetworkSettings.Id**](networksettings-id.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd11-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccd11-118">Requirements</span></span>



| <span data-ttu-id="ccd11-119">需求</span><span class="sxs-lookup"><span data-stu-id="ccd11-119">Requirement</span></span> | <span data-ttu-id="ccd11-120">值</span><span class="sxs-lookup"><span data-stu-id="ccd11-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ccd11-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccd11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd11-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccd11-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ccd11-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccd11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd11-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccd11-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






---
description: 表示橋接器服務為交換器服務元件的關聯。
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: CIM_SwitchServiceTransparentBridging 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992026"
---
# <a name="cim_switchservicetransparentbridging-class"></a><span data-ttu-id="381fb-103">CIM \_ SwitchServiceTransparentBridging 類別</span><span class="sxs-lookup"><span data-stu-id="381fb-103">CIM\_SwitchServiceTransparentBridging class</span></span>

<span data-ttu-id="381fb-104">表示橋接器服務為交換器服務元件的關聯。</span><span class="sxs-lookup"><span data-stu-id="381fb-104">Represents an association in which a bridge service is a component of a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="381fb-105">語法</span><span class="sxs-lookup"><span data-stu-id="381fb-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="381fb-106">成員</span><span class="sxs-lookup"><span data-stu-id="381fb-106">Members</span></span>

<span data-ttu-id="381fb-107">**CIM \_ SwitchServiceTransparentBridging** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="381fb-107">The **CIM\_SwitchServiceTransparentBridging** class has these types of members:</span></span>

-   [<span data-ttu-id="381fb-108">屬性</span><span class="sxs-lookup"><span data-stu-id="381fb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="381fb-109">屬性</span><span class="sxs-lookup"><span data-stu-id="381fb-109">Properties</span></span>

<span data-ttu-id="381fb-110">**CIM \_ SwitchServiceTransparentBridging** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="381fb-110">The **CIM\_SwitchServiceTransparentBridging** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="381fb-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="381fb-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="381fb-112">資料類型： **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="381fb-112">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="381fb-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="381fb-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="381fb-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="381fb-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="381fb-115">Switch 服務的 [**CIM \_ SwitchService**](cim-switchservice.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="381fb-115">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switch service.</span></span>

</dd> <dt>

<span data-ttu-id="381fb-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="381fb-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="381fb-117">資料類型： **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="381fb-117">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="381fb-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="381fb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="381fb-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="381fb-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="381fb-120">元件橋接服務的 [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="381fb-120">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the component bridging service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="381fb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="381fb-121">Requirements</span></span>



| <span data-ttu-id="381fb-122">需求</span><span class="sxs-lookup"><span data-stu-id="381fb-122">Requirement</span></span> | <span data-ttu-id="381fb-123">值</span><span class="sxs-lookup"><span data-stu-id="381fb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="381fb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="381fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="381fb-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="381fb-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="381fb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="381fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="381fb-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="381fb-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="381fb-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="381fb-128">Namespace</span></span><br/>                | <span data-ttu-id="381fb-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="381fb-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="381fb-130">MOF</span><span class="sxs-lookup"><span data-stu-id="381fb-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="381fb-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="381fb-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="381fb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="381fb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="381fb-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="381fb-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="381fb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="381fb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381fb-135">**CIM \_ ServiceComponent**</span><span class="sxs-lookup"><span data-stu-id="381fb-135">**CIM\_ServiceComponent**</span></span>](cim-servicecomponent.md)
</dt> </dl>

 


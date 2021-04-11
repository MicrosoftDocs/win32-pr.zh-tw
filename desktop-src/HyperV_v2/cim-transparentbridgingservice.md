---
description: 代表 CIM SwitchService 物件的透明橋接層面 \_ 。
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848788"
---
# <a name="cim_transparentbridgingservice-class"></a><span data-ttu-id="58c85-103">CIM \_ TransparentBridgingService 類別</span><span class="sxs-lookup"><span data-stu-id="58c85-103">CIM\_TransparentBridgingService class</span></span>

<span data-ttu-id="58c85-104">代表 [**CIM \_ SwitchService**](cim-switchservice.md) 物件的透明橋接層面。</span><span class="sxs-lookup"><span data-stu-id="58c85-104">Represents the transparent bridging aspect of a [**CIM\_SwitchService**](cim-switchservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c85-105">語法</span><span class="sxs-lookup"><span data-stu-id="58c85-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a><span data-ttu-id="58c85-106">成員</span><span class="sxs-lookup"><span data-stu-id="58c85-106">Members</span></span>

<span data-ttu-id="58c85-107">**CIM \_ TransparentBridgingService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="58c85-107">The **CIM\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="58c85-108">屬性</span><span class="sxs-lookup"><span data-stu-id="58c85-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58c85-109">屬性</span><span class="sxs-lookup"><span data-stu-id="58c85-109">Properties</span></span>

<span data-ttu-id="58c85-110">**CIM \_ TransparentBridgingService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="58c85-110">The **CIM\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58c85-111">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="58c85-111">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58c85-112">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="58c85-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58c85-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58c85-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58c85-114">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIB。IETF \| BRIDGE-dot1dTpAgingTime ") </span><span class="sxs-lookup"><span data-stu-id="58c85-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpAgingTime")</span></span>
</dt> </dl>

<span data-ttu-id="58c85-115">以秒為單位的超時時間（以秒為單位），用來產生動態學習的轉送資訊。</span><span class="sxs-lookup"><span data-stu-id="58c85-115">The timeout period, in seconds, for aging out dynamically learned forwarding information.</span></span> <span data-ttu-id="58c85-116">802.1 D-1990 標準建議預設值300秒。</span><span class="sxs-lookup"><span data-stu-id="58c85-116">The 802.1D-1990 standard recommends a default of 300 seconds.</span></span>

</dd> <dt>

<span data-ttu-id="58c85-117">**裂**</span><span class="sxs-lookup"><span data-stu-id="58c85-117">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58c85-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="58c85-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58c85-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58c85-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58c85-120">篩選具有一個以上篩選資料庫的 VLAN 感知參數所使用的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="58c85-120">Filtering Database Identifier used by VLAN-aware switches that have more than one filtering database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58c85-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="58c85-121">Requirements</span></span>



| <span data-ttu-id="58c85-122">需求</span><span class="sxs-lookup"><span data-stu-id="58c85-122">Requirement</span></span> | <span data-ttu-id="58c85-123">值</span><span class="sxs-lookup"><span data-stu-id="58c85-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c85-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58c85-124">Minimum supported client</span></span><br/> | <span data-ttu-id="58c85-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="58c85-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="58c85-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58c85-126">Minimum supported server</span></span><br/> | <span data-ttu-id="58c85-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58c85-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="58c85-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="58c85-128">Namespace</span></span><br/>                | <span data-ttu-id="58c85-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="58c85-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="58c85-130">MOF</span><span class="sxs-lookup"><span data-stu-id="58c85-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58c85-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="58c85-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58c85-132">DLL</span><span class="sxs-lookup"><span data-stu-id="58c85-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c85-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58c85-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58c85-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58c85-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c85-135">**CIM \_ ForwardingService**</span><span class="sxs-lookup"><span data-stu-id="58c85-135">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 


---
description: 表示路由網域設定資料。
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Msvm_EthernetSwitchPortRoutingDomainSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853155"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a><span data-ttu-id="c4005-103">Msvm \_ EthernetSwitchPortRoutingDomainSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="c4005-103">Msvm\_EthernetSwitchPortRoutingDomainSettingData class</span></span>

<span data-ttu-id="c4005-104">表示路由網域設定資料。</span><span class="sxs-lookup"><span data-stu-id="c4005-104">Represents the routing domain setting data.</span></span>

<span data-ttu-id="c4005-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4005-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4005-106">語法</span><span class="sxs-lookup"><span data-stu-id="c4005-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a><span data-ttu-id="c4005-107">成員</span><span class="sxs-lookup"><span data-stu-id="c4005-107">Members</span></span>

<span data-ttu-id="c4005-108">**Msvm \_ EthernetSwitchPortRoutingDomainSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c4005-108">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c4005-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c4005-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4005-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c4005-110">Properties</span></span>

<span data-ttu-id="c4005-111">**Msvm \_ EthernetSwitchPortRoutingDomainSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c4005-111">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4005-112">**IsolationIdList**</span><span class="sxs-lookup"><span data-stu-id="c4005-112">**IsolationIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4005-113">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="c4005-113">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="c4005-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c4005-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4005-115">限定詞： **WmiDataId** (3) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="c4005-115">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c4005-116">路由網域的 VirtualSubnetId 或 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4005-116">The VirtualSubnetId or VLAN IDs for the routing domains.</span></span>

</dd> <dt>

<span data-ttu-id="c4005-117">**IsolationIdNameList**</span><span class="sxs-lookup"><span data-stu-id="c4005-117">**IsolationIdNameList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4005-118">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c4005-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4005-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c4005-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4005-120">限定詞： **WmiDataId** (4) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="c4005-120">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c4005-121">VirtualSubnetId 或 VLAN 的易記名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="c4005-121">The VirtualSubnetId or VLAN friendly name array.</span></span>

</dd> <dt>

<span data-ttu-id="c4005-122">**RoutingDomainGuid**</span><span class="sxs-lookup"><span data-stu-id="c4005-122">**RoutingDomainGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4005-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4005-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4005-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c4005-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4005-125">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (1) 、 [**版本**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="c4005-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c4005-126">路由網域 GUID。</span><span class="sxs-lookup"><span data-stu-id="c4005-126">The routing domain GUID.</span></span>

</dd> <dt>

<span data-ttu-id="c4005-127">**RoutingDomainName**</span><span class="sxs-lookup"><span data-stu-id="c4005-127">**RoutingDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4005-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4005-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4005-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c4005-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4005-130">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (2) 、 [**版本**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="c4005-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c4005-131">路由網域的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c4005-131">The routing domain friendly name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4005-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4005-132">Requirements</span></span>



| <span data-ttu-id="c4005-133">需求</span><span class="sxs-lookup"><span data-stu-id="c4005-133">Requirement</span></span> | <span data-ttu-id="c4005-134">值</span><span class="sxs-lookup"><span data-stu-id="c4005-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4005-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4005-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c4005-136">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c4005-136">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c4005-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4005-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c4005-138">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c4005-138">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c4005-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="c4005-139">Namespace</span></span><br/>                | <span data-ttu-id="c4005-140">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c4005-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c4005-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c4005-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4005-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c4005-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4005-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c4005-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4005-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4005-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4005-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4005-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4005-146">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="c4005-146">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 


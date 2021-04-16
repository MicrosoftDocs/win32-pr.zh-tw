---
description: 用來建立一個 Msvm EmulatedEthernetPortSettingData 實例之間關聯性的關聯 \_ ，以及一個或多個 Msvm EthernetSwitchFeatureSettingData 實例之間的關聯性 \_ 。
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Msvm_EthernetPortFailoverSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513500"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a><span data-ttu-id="685fc-103">Msvm \_ EthernetPortFailoverSettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="685fc-103">Msvm\_EthernetPortFailoverSettingDataComponent class</span></span>

<span data-ttu-id="685fc-104">用來建立一個 [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) 實例之間關聯性的關聯，以及一個或多個 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)實例之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="685fc-104">An association used to establish relationships between one instance of an [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="685fc-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="685fc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="685fc-106">語法</span><span class="sxs-lookup"><span data-stu-id="685fc-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="685fc-107">成員</span><span class="sxs-lookup"><span data-stu-id="685fc-107">Members</span></span>

<span data-ttu-id="685fc-108">**Msvm \_ EthernetPortFailoverSettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="685fc-108">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="685fc-109">屬性</span><span class="sxs-lookup"><span data-stu-id="685fc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="685fc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="685fc-110">Properties</span></span>

<span data-ttu-id="685fc-111">**Msvm \_ EthernetPortFailoverSettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="685fc-111">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="685fc-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="685fc-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685fc-113">資料類型： **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="685fc-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="685fc-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="685fc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685fc-115">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="685fc-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="685fc-116">代表 Ethernet 埠之 [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) 或 [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="685fc-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="685fc-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="685fc-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685fc-118">資料類型： **[ **Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="685fc-118">Data type: **[**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="685fc-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="685fc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685fc-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="685fc-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="685fc-121">代表來賓網路介面卡設定之 [**Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="685fc-121">A reference to an instance of the [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) class that represents the guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="685fc-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="685fc-122">Requirements</span></span>



| <span data-ttu-id="685fc-123">需求</span><span class="sxs-lookup"><span data-stu-id="685fc-123">Requirement</span></span> | <span data-ttu-id="685fc-124">值</span><span class="sxs-lookup"><span data-stu-id="685fc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685fc-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="685fc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="685fc-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="685fc-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="685fc-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="685fc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="685fc-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="685fc-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="685fc-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="685fc-129">Namespace</span></span><br/>                | <span data-ttu-id="685fc-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="685fc-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="685fc-131">MOF</span><span class="sxs-lookup"><span data-stu-id="685fc-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="685fc-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="685fc-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="685fc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="685fc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="685fc-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="685fc-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


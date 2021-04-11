---
description: '\_ \_ 使用 Msvm GuestNetworkAdapterConfiguration 類別的實例，在 Msvm EmulatedEthernetPortSettingData 或 Msvm SyntheticEthernetPortSettingData 類別的實例之間建立關聯性 \_ 。'
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Msvm_SettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944566"
---
# <a name="msvm_settingdatacomponent-class"></a><span data-ttu-id="82fdc-103">Msvm \_ SettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="82fdc-103">Msvm\_SettingDataComponent class</span></span>

<span data-ttu-id="82fdc-104">使用 [**Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)類別的實例，在 [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md)或 [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md)類別的實例之間建立關聯性。</span><span class="sxs-lookup"><span data-stu-id="82fdc-104">Establish a relationship between an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class with an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span>

<span data-ttu-id="82fdc-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="82fdc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82fdc-106">語法</span><span class="sxs-lookup"><span data-stu-id="82fdc-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="82fdc-107">成員</span><span class="sxs-lookup"><span data-stu-id="82fdc-107">Members</span></span>

<span data-ttu-id="82fdc-108">**Msvm \_ SettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="82fdc-108">The **Msvm\_SettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="82fdc-109">屬性</span><span class="sxs-lookup"><span data-stu-id="82fdc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82fdc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="82fdc-110">Properties</span></span>

<span data-ttu-id="82fdc-111">**Msvm \_ SettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="82fdc-111">The **Msvm\_SettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82fdc-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="82fdc-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82fdc-113">資料類型： **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="82fdc-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="82fdc-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82fdc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82fdc-115">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82fdc-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82fdc-116">代表 Ethernet 埠之 [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) 或 [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="82fdc-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="82fdc-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="82fdc-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82fdc-118">資料類型： **[ **Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span><span class="sxs-lookup"><span data-stu-id="82fdc-118">Data type: **[**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span></span>
</dt> <dt>

<span data-ttu-id="82fdc-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82fdc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82fdc-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="82fdc-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="82fdc-121">代表來賓網路介面卡設定之 [**Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="82fdc-121">A reference to an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class that represents a guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82fdc-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="82fdc-122">Requirements</span></span>



| <span data-ttu-id="82fdc-123">需求</span><span class="sxs-lookup"><span data-stu-id="82fdc-123">Requirement</span></span> | <span data-ttu-id="82fdc-124">值</span><span class="sxs-lookup"><span data-stu-id="82fdc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82fdc-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82fdc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82fdc-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82fdc-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="82fdc-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82fdc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82fdc-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82fdc-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82fdc-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="82fdc-129">Namespace</span></span><br/>                | <span data-ttu-id="82fdc-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="82fdc-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="82fdc-131">MOF</span><span class="sxs-lookup"><span data-stu-id="82fdc-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82fdc-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="82fdc-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82fdc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="82fdc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82fdc-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82fdc-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


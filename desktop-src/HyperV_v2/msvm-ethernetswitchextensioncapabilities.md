---
description: 代表 Ethernet 擴充功能與其功能之間的關聯。
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Msvm_EthernetSwitchExtensionCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695879"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a><span data-ttu-id="294b4-103">Msvm \_ EthernetSwitchExtensionCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="294b4-103">Msvm\_EthernetSwitchExtensionCapabilities class</span></span>

<span data-ttu-id="294b4-104">代表 Ethernet 擴充功能與其功能之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="294b4-104">Represents the association between Ethernet extensions and their capabilities.</span></span>

<span data-ttu-id="294b4-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="294b4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="294b4-106">語法</span><span class="sxs-lookup"><span data-stu-id="294b4-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="294b4-107">成員</span><span class="sxs-lookup"><span data-stu-id="294b4-107">Members</span></span>

<span data-ttu-id="294b4-108">**Msvm \_ EthernetSwitchExtensionCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="294b4-108">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="294b4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="294b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="294b4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="294b4-110">Properties</span></span>

<span data-ttu-id="294b4-111">**Msvm \_ EthernetSwitchExtensionCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="294b4-111">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="294b4-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="294b4-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="294b4-113">資料類型： **[ **Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="294b4-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="294b4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="294b4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="294b4-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「功能」 ) </span><span class="sxs-lookup"><span data-stu-id="294b4-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="294b4-116">[**Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)類別實例的參考，表示與參數相關聯的功能物件。</span><span class="sxs-lookup"><span data-stu-id="294b4-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the capabilities object associated with the switch.</span></span> <span data-ttu-id="294b4-117">這個屬性繼承自 [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="294b4-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="294b4-118">**特性**</span><span class="sxs-lookup"><span data-stu-id="294b4-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="294b4-119">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="294b4-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="294b4-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="294b4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="294b4-121">提供有關功能的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="294b4-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="294b4-122">這個屬性繼承自 [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="294b4-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="294b4-123">值</span><span class="sxs-lookup"><span data-stu-id="294b4-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="294b4-124">意義</span><span class="sxs-lookup"><span data-stu-id="294b4-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="294b4-125"><dt>**預設值**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="294b4-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="294b4-126">相關聯的功能代表 managed 元素的預設功能。</span><span class="sxs-lookup"><span data-stu-id="294b4-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="294b4-127"><dt>**目前**</dt>的 <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="294b4-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="294b4-128">相關聯的功能代表 managed 元素目前的功能。</span><span class="sxs-lookup"><span data-stu-id="294b4-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="294b4-129">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="294b4-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="294b4-130">資料類型： **[ **Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="294b4-130">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="294b4-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="294b4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="294b4-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ManagedElement" ) </span><span class="sxs-lookup"><span data-stu-id="294b4-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="294b4-133">代表已安裝之延伸模組之 [**Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="294b4-133">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents the installed extension.</span></span> <span data-ttu-id="294b4-134">這個屬性繼承自 [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="294b4-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="294b4-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="294b4-135">Requirements</span></span>



| <span data-ttu-id="294b4-136">需求</span><span class="sxs-lookup"><span data-stu-id="294b4-136">Requirement</span></span> | <span data-ttu-id="294b4-137">值</span><span class="sxs-lookup"><span data-stu-id="294b4-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="294b4-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="294b4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="294b4-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="294b4-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="294b4-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="294b4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="294b4-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="294b4-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="294b4-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="294b4-142">Namespace</span></span><br/>                | <span data-ttu-id="294b4-143">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="294b4-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="294b4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="294b4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="294b4-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="294b4-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="294b4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="294b4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="294b4-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="294b4-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


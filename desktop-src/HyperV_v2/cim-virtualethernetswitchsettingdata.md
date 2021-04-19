---
description: 描述虛擬乙太網路交換器的設定資料。
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: CIM_VirtualEthernetSwitchSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974628"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="c0347-103">CIM \_ VirtualEthernetSwitchSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="c0347-103">CIM\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="c0347-104">描述虛擬乙太網路交換器的設定資料。</span><span class="sxs-lookup"><span data-stu-id="c0347-104">Describes settings data for a virtual ethernet switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0347-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0347-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="c0347-106">成員</span><span class="sxs-lookup"><span data-stu-id="c0347-106">Members</span></span>

<span data-ttu-id="c0347-107">**CIM \_ VirtualEthernetSwitchSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c0347-107">The **CIM\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c0347-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c0347-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0347-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c0347-109">Properties</span></span>

<span data-ttu-id="c0347-110">**CIM \_ VirtualEthernetSwitchSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c0347-110">The **CIM\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0347-111">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="c0347-111">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0347-112">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c0347-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0347-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0347-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0347-114">陣列，其中包含目前相關聯的主機資源集區，或與乙太網路交換器相關聯的主機資源集區，以便在乙太網路交換器和虛擬機器之間配置乙太網路連線。</span><span class="sxs-lookup"><span data-stu-id="c0347-114">An array that contains the host resource pools that are currently associated, or to associate with the ethernet switch, in order to allocate ethernet connections between the ethernet switch and a virtual machine.</span></span> <span data-ttu-id="c0347-115">這個屬性的每個非 Null 值都必須符合在 DMTF "DSP0207" 規格中定義的 **WBEM \_ URI \_ UntypedInstancePath** 。</span><span class="sxs-lookup"><span data-stu-id="c0347-115">Each non-Null value of this property must conform to **WBEM\_URI\_UntypedInstancePath** as defined in the DMTF "DSP0207" specification.</span></span>

</dd> <dt>

<span data-ttu-id="c0347-116">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="c0347-116">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0347-117">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0347-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0347-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0347-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0347-119">交換器可針對 MAC 位址學習學習的唯一 MAC 位址數目，如同 IEEE 802.1 標準中所定義。</span><span class="sxs-lookup"><span data-stu-id="c0347-119">The number of unique MAC addresses that the switch can learn for MAC address learning, as defined in the IEEE 802.1 standard.</span></span>

</dd> <dt>

<span data-ttu-id="c0347-120">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="c0347-120">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0347-121">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c0347-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0347-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0347-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0347-123">陣列，其中包含交換器可以存取的 VLAN Id。</span><span class="sxs-lookup"><span data-stu-id="c0347-123">An array that contains the VLAN IDs that the switch can access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0347-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0347-124">Requirements</span></span>



| <span data-ttu-id="c0347-125">需求</span><span class="sxs-lookup"><span data-stu-id="c0347-125">Requirement</span></span> | <span data-ttu-id="c0347-126">值</span><span class="sxs-lookup"><span data-stu-id="c0347-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0347-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0347-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c0347-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c0347-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c0347-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0347-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c0347-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0347-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c0347-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0347-131">Namespace</span></span><br/>                | <span data-ttu-id="c0347-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c0347-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c0347-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c0347-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0347-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c0347-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0347-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c0347-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0347-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0347-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0347-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0347-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0347-138">**CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="c0347-138">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 





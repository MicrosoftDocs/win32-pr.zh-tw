---
description: 用來建立 &\# 0034 的關聯、&0034 的一部分、 \# Msvm EthernetPortAllocationSettingData 的一個實例之間的關聯性 \_ ，以及一個或多個 Msvm \_ EthernetSwitchFeatureSettingData 實例之間的關聯性。
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971828"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a><span data-ttu-id="23b7f-103">Msvm \_ EthernetPortSettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="23b7f-103">Msvm\_EthernetPortSettingDataComponent class</span></span>

<span data-ttu-id="23b7f-104">用來建立一個 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 實例與一個或多個 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)實例之間「部分」關聯性的關聯。</span><span class="sxs-lookup"><span data-stu-id="23b7f-104">An association used to establish "part of" relationships between one instance of an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="23b7f-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="23b7f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b7f-106">語法</span><span class="sxs-lookup"><span data-stu-id="23b7f-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="23b7f-107">成員</span><span class="sxs-lookup"><span data-stu-id="23b7f-107">Members</span></span>

<span data-ttu-id="23b7f-108">**Msvm \_ EthernetPortSettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="23b7f-108">The **Msvm\_EthernetPortSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="23b7f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="23b7f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23b7f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="23b7f-110">Properties</span></span>

<span data-ttu-id="23b7f-111">**Msvm \_ EthernetPortSettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="23b7f-111">The **Msvm\_EthernetPortSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23b7f-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="23b7f-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b7f-113">資料類型： **[ **Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="23b7f-113">Data type: **[**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="23b7f-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="23b7f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23b7f-115">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23b7f-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23b7f-116">代表 Ethernet 埠之 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="23b7f-116">A reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="23b7f-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="23b7f-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b7f-118">資料類型： **[ **Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="23b7f-118">Data type: **[**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="23b7f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="23b7f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23b7f-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="23b7f-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="23b7f-121">[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)類別實例的參考，代表套用至埠的功能設定。</span><span class="sxs-lookup"><span data-stu-id="23b7f-121">A reference to an instance of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the feature settings applied to the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23b7f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="23b7f-122">Requirements</span></span>



| <span data-ttu-id="23b7f-123">需求</span><span class="sxs-lookup"><span data-stu-id="23b7f-123">Requirement</span></span> | <span data-ttu-id="23b7f-124">值</span><span class="sxs-lookup"><span data-stu-id="23b7f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23b7f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23b7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="23b7f-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23b7f-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23b7f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23b7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="23b7f-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23b7f-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23b7f-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="23b7f-129">Namespace</span></span><br/>                | <span data-ttu-id="23b7f-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="23b7f-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23b7f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="23b7f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23b7f-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="23b7f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23b7f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="23b7f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b7f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23b7f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


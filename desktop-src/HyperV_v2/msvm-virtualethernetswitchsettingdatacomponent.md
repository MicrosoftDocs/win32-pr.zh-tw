---
description: 用來建立 &\# 0034 的關聯、&0034 的一部分、 \# 一個 Msvm VirtualEthernetSwitchSettingData 實例之間的關聯性 \_ ，以及一個或多個 Msvm EthernetSwitchFeatureSettingData 實例之間 \_ 的關聯性。
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Msvm_VirtualEthernetSwitchSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192112"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a><span data-ttu-id="399d3-103">Msvm \_ VirtualEthernetSwitchSettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="399d3-103">Msvm\_VirtualEthernetSwitchSettingDataComponent class</span></span>

<span data-ttu-id="399d3-104">用來建立一個 [**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) 實例和一或多個 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)實例之間「部分」關聯性的關聯。</span><span class="sxs-lookup"><span data-stu-id="399d3-104">An association used to establish "part of" relationships between one instance of [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) and one or more instances of [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="399d3-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="399d3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="399d3-106">語法</span><span class="sxs-lookup"><span data-stu-id="399d3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="399d3-107">成員</span><span class="sxs-lookup"><span data-stu-id="399d3-107">Members</span></span>

<span data-ttu-id="399d3-108">**Msvm \_ VirtualEthernetSwitchSettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="399d3-108">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="399d3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="399d3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="399d3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="399d3-110">Properties</span></span>

<span data-ttu-id="399d3-111">**Msvm \_ VirtualEthernetSwitchSettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="399d3-111">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="399d3-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="399d3-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="399d3-113">資料類型： **Msvm \_ VirtualEthernetSwitchSettingData**</span><span class="sxs-lookup"><span data-stu-id="399d3-113">Data type: **Msvm\_VirtualEthernetSwitchSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="399d3-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="399d3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="399d3-115">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="399d3-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="399d3-116">參考代表乙太網路埠之 [**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="399d3-116">Reference to an instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="399d3-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="399d3-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="399d3-118">資料類型： **Msvm \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="399d3-118">Data type: **Msvm\_EthernetSwitchFeatureSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="399d3-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="399d3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="399d3-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="399d3-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="399d3-121">參考 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) 類別的實例，代表套用至參數的設定。</span><span class="sxs-lookup"><span data-stu-id="399d3-121">Reference to an instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that represents the settings applied to the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="399d3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="399d3-122">Requirements</span></span>



| <span data-ttu-id="399d3-123">需求</span><span class="sxs-lookup"><span data-stu-id="399d3-123">Requirement</span></span> | <span data-ttu-id="399d3-124">值</span><span class="sxs-lookup"><span data-stu-id="399d3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399d3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="399d3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="399d3-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="399d3-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="399d3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="399d3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="399d3-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="399d3-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="399d3-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="399d3-129">Namespace</span></span><br/>                | <span data-ttu-id="399d3-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="399d3-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="399d3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="399d3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="399d3-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="399d3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="399d3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="399d3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="399d3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="399d3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: 定義乙太網路交換器和交換器資源之間的關聯。
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Msvm_EthernetSwitchInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945509"
---
# <a name="msvm_ethernetswitchinfo-class"></a><span data-ttu-id="96525-103">Msvm \_ EthernetSwitchInfo 類別</span><span class="sxs-lookup"><span data-stu-id="96525-103">Msvm\_EthernetSwitchInfo class</span></span>

<span data-ttu-id="96525-104">定義乙太網路交換器和交換器資源之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="96525-104">Defines the association between an Ethernet switch and a switch resource.</span></span>

<span data-ttu-id="96525-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="96525-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96525-106">語法</span><span class="sxs-lookup"><span data-stu-id="96525-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="96525-107">成員</span><span class="sxs-lookup"><span data-stu-id="96525-107">Members</span></span>

<span data-ttu-id="96525-108">**Msvm \_ EthernetSwitchInfo** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="96525-108">The **Msvm\_EthernetSwitchInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="96525-109">屬性</span><span class="sxs-lookup"><span data-stu-id="96525-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96525-110">屬性</span><span class="sxs-lookup"><span data-stu-id="96525-110">Properties</span></span>

<span data-ttu-id="96525-111">**Msvm \_ EthernetSwitchInfo** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="96525-111">The **Msvm\_EthernetSwitchInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96525-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="96525-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96525-113">資料類型： **Msvm \_ VirtualEthernetSwitch**</span><span class="sxs-lookup"><span data-stu-id="96525-113">Data type: **Msvm\_VirtualEthernetSwitch**</span></span>
</dt> <dt>

<span data-ttu-id="96525-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96525-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96525-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="96525-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="96525-116">代表裝載系統之 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 類別的參考。</span><span class="sxs-lookup"><span data-stu-id="96525-116">A reference to the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the hosting system.</span></span> <span data-ttu-id="96525-117">此屬性衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="96525-117">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="96525-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="96525-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96525-119">資料類型： **Msvm \_ EthernetSwitchData**</span><span class="sxs-lookup"><span data-stu-id="96525-119">Data type: **Msvm\_EthernetSwitchData**</span></span>
</dt> <dt>

<span data-ttu-id="96525-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96525-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96525-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="96525-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="96525-122">代表切換資源之 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md) 類別的參考。</span><span class="sxs-lookup"><span data-stu-id="96525-122">A reference to the [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md) class that represents the switch resource.</span></span> <span data-ttu-id="96525-123">此屬性衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="96525-123">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96525-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="96525-124">Requirements</span></span>



| <span data-ttu-id="96525-125">需求</span><span class="sxs-lookup"><span data-stu-id="96525-125">Requirement</span></span> | <span data-ttu-id="96525-126">值</span><span class="sxs-lookup"><span data-stu-id="96525-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96525-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96525-127">Minimum supported client</span></span><br/> | <span data-ttu-id="96525-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96525-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="96525-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96525-129">Minimum supported server</span></span><br/> | <span data-ttu-id="96525-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96525-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96525-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="96525-131">Namespace</span></span><br/>                | <span data-ttu-id="96525-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="96525-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="96525-133">MOF</span><span class="sxs-lookup"><span data-stu-id="96525-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96525-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="96525-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96525-135">DLL</span><span class="sxs-lookup"><span data-stu-id="96525-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96525-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96525-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


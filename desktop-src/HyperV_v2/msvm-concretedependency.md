---
description: 定義已安裝之乙太網路交換器擴充功能與乙太網路交換器擴充功能之間的關聯。
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Msvm_ConcreteDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192119"
---
# <a name="msvm_concretedependency-class"></a><span data-ttu-id="709e5-103">Msvm \_ ConcreteDependency 類別</span><span class="sxs-lookup"><span data-stu-id="709e5-103">Msvm\_ConcreteDependency class</span></span>

<span data-ttu-id="709e5-104">定義已安裝之乙太網路交換器擴充功能與乙太網路交換器擴充功能之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="709e5-104">Defines the association between an installed Ethernet switch extension and an Ethernet switch extension.</span></span>

<span data-ttu-id="709e5-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="709e5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="709e5-106">語法</span><span class="sxs-lookup"><span data-stu-id="709e5-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="709e5-107">成員</span><span class="sxs-lookup"><span data-stu-id="709e5-107">Members</span></span>

<span data-ttu-id="709e5-108">**Msvm \_ ConcreteDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="709e5-108">The **Msvm\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="709e5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="709e5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="709e5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="709e5-110">Properties</span></span>

<span data-ttu-id="709e5-111">**Msvm \_ ConcreteDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="709e5-111">The **Msvm\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="709e5-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="709e5-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e5-113">資料類型： **[ **Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="709e5-113">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="709e5-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="709e5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="709e5-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="709e5-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="709e5-116">[**Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)類別實例的參考，代表安裝在系統上的虛擬乙太網路交換器擴充元件。</span><span class="sxs-lookup"><span data-stu-id="709e5-116">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents a virtual Ethernet switch extension component installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="709e5-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="709e5-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e5-118">資料類型： **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="709e5-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="709e5-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="709e5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="709e5-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="709e5-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="709e5-121">[**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)類別之實例的參考，該類別表示系結至特定虛擬乙太網路 **交換器的出現** 位置。</span><span class="sxs-lookup"><span data-stu-id="709e5-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the occurrence of the **Antecedent** bound to a specific virtual Ethernet switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="709e5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="709e5-122">Requirements</span></span>



| <span data-ttu-id="709e5-123">需求</span><span class="sxs-lookup"><span data-stu-id="709e5-123">Requirement</span></span> | <span data-ttu-id="709e5-124">值</span><span class="sxs-lookup"><span data-stu-id="709e5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="709e5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="709e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="709e5-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="709e5-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="709e5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="709e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="709e5-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="709e5-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="709e5-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="709e5-129">Namespace</span></span><br/>                | <span data-ttu-id="709e5-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="709e5-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="709e5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="709e5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="709e5-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="709e5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="709e5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="709e5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="709e5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="709e5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


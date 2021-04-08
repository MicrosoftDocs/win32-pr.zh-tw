---
description: 將虛擬乙太網路交換器與目前系結的延伸模組產生關聯。
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Msvm_HostedEthernetSwitchExtension 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690868"
---
# <a name="msvm_hostedethernetswitchextension-class"></a><span data-ttu-id="780f9-103">Msvm \_ HostedEthernetSwitchExtension 類別</span><span class="sxs-lookup"><span data-stu-id="780f9-103">Msvm\_HostedEthernetSwitchExtension class</span></span>

<span data-ttu-id="780f9-104">將虛擬乙太網路交換器與目前系結的延伸模組產生關聯。</span><span class="sxs-lookup"><span data-stu-id="780f9-104">Associates a virtual Ethernet switch to the extensions currently bound to it.</span></span>

<span data-ttu-id="780f9-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="780f9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="780f9-106">語法</span><span class="sxs-lookup"><span data-stu-id="780f9-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="780f9-107">成員</span><span class="sxs-lookup"><span data-stu-id="780f9-107">Members</span></span>

<span data-ttu-id="780f9-108">**Msvm \_ HostedEthernetSwitchExtension** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="780f9-108">The **Msvm\_HostedEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="780f9-109">屬性</span><span class="sxs-lookup"><span data-stu-id="780f9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="780f9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="780f9-110">Properties</span></span>

<span data-ttu-id="780f9-111">**Msvm \_ HostedEthernetSwitchExtension** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="780f9-111">The **Msvm\_HostedEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="780f9-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="780f9-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="780f9-113">資料類型： **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="780f9-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="780f9-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="780f9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="780f9-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="780f9-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="780f9-116">代表虛擬交換器之 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="780f9-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="780f9-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="780f9-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="780f9-118">資料類型： **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="780f9-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="780f9-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="780f9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="780f9-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="780f9-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="780f9-121">[**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)類別實例的參考，代表系結至虛擬交換器的參數延伸模組實例。</span><span class="sxs-lookup"><span data-stu-id="780f9-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the switch extension instance bound to the virtual switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="780f9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="780f9-122">Requirements</span></span>



| <span data-ttu-id="780f9-123">需求</span><span class="sxs-lookup"><span data-stu-id="780f9-123">Requirement</span></span> | <span data-ttu-id="780f9-124">值</span><span class="sxs-lookup"><span data-stu-id="780f9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="780f9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="780f9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="780f9-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="780f9-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="780f9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="780f9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="780f9-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="780f9-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="780f9-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="780f9-129">Namespace</span></span><br/>                | <span data-ttu-id="780f9-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="780f9-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="780f9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="780f9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="780f9-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="780f9-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="780f9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="780f9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="780f9-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="780f9-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


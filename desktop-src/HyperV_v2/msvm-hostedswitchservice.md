---
description: 連接虛擬交換器服務與透明橋接服務的關聯。
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Msvm_HostedSwitchService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973226"
---
# <a name="msvm_hostedswitchservice-class"></a><span data-ttu-id="6dc41-103">Msvm \_ HostedSwitchService 類別</span><span class="sxs-lookup"><span data-stu-id="6dc41-103">Msvm\_HostedSwitchService class</span></span>

<span data-ttu-id="6dc41-104">連接虛擬交換器服務與透明橋接服務的關聯。</span><span class="sxs-lookup"><span data-stu-id="6dc41-104">An association that connects a virtual switch service to a transparent bridging service.</span></span>

<span data-ttu-id="6dc41-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6dc41-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc41-106">語法</span><span class="sxs-lookup"><span data-stu-id="6dc41-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6dc41-107">成員</span><span class="sxs-lookup"><span data-stu-id="6dc41-107">Members</span></span>

<span data-ttu-id="6dc41-108">**Msvm \_ HostedSwitchService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6dc41-108">The **Msvm\_HostedSwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="6dc41-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6dc41-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6dc41-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6dc41-110">Properties</span></span>

<span data-ttu-id="6dc41-111">**Msvm \_ HostedSwitchService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6dc41-111">The **Msvm\_HostedSwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6dc41-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="6dc41-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dc41-113">資料類型： **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="6dc41-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6dc41-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6dc41-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dc41-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="6dc41-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6dc41-116">代表虛擬交換器之 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="6dc41-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="6dc41-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6dc41-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dc41-118">資料類型： **[ **CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="6dc41-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="6dc41-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6dc41-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dc41-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="6dc41-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6dc41-121">代表橋接服務之 [**Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="6dc41-121">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the bridging service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6dc41-122">備註</span><span class="sxs-lookup"><span data-stu-id="6dc41-122">Remarks</span></span>

<span data-ttu-id="6dc41-123">存取 **Msvm \_ HostedSwitchService** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="6dc41-123">Access to the **Msvm\_HostedSwitchService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6dc41-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="6dc41-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc41-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dc41-125">Requirements</span></span>



| <span data-ttu-id="6dc41-126">需求</span><span class="sxs-lookup"><span data-stu-id="6dc41-126">Requirement</span></span> | <span data-ttu-id="6dc41-127">值</span><span class="sxs-lookup"><span data-stu-id="6dc41-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc41-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dc41-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc41-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dc41-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6dc41-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dc41-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc41-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dc41-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6dc41-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="6dc41-132">Namespace</span></span><br/>                | <span data-ttu-id="6dc41-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6dc41-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6dc41-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6dc41-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dc41-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6dc41-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dc41-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6dc41-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dc41-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6dc41-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6dc41-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dc41-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc41-139">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="6dc41-139">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="6dc41-140">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="6dc41-140">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 


---
description: 將交換器埠連接到動態轉寄專案， (瞭解的 MAC 位址) 。
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Msvm_SwitchPortDynamicForwarding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e6dda46302e9e8c58710bad1f4221e14e2c3f4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983440"
---
# <a name="msvm_switchportdynamicforwarding-class"></a><span data-ttu-id="3b989-103">Msvm \_ SwitchPortDynamicForwarding 類別</span><span class="sxs-lookup"><span data-stu-id="3b989-103">Msvm\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="3b989-104">將交換器埠連接到動態轉寄專案， (瞭解的 MAC 位址) 。</span><span class="sxs-lookup"><span data-stu-id="3b989-104">Connects a switch port to a dynamic forward entry (learned MAC address).</span></span> <span data-ttu-id="3b989-105">在尋找指定埠的所有已學習 MAC 位址時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="3b989-105">This is useful in finding all of the learned MAC addresses for a specified port.</span></span>

<span data-ttu-id="3b989-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b989-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b989-107">語法</span><span class="sxs-lookup"><span data-stu-id="3b989-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3b989-108">成員</span><span class="sxs-lookup"><span data-stu-id="3b989-108">Members</span></span>

<span data-ttu-id="3b989-109">**Msvm \_ SwitchPortDynamicForwarding** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b989-109">The **Msvm\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="3b989-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3b989-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b989-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3b989-111">Properties</span></span>

<span data-ttu-id="3b989-112">**Msvm \_ SwitchPortDynamicForwarding** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b989-112">The **Msvm\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b989-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="3b989-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b989-114">資料類型： **[ **Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span><span class="sxs-lookup"><span data-stu-id="3b989-114">Data type: **[**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3b989-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b989-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b989-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="3b989-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3b989-117">代表切換埠之 [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="3b989-117">A reference to an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="3b989-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="3b989-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b989-119">資料類型： **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="3b989-119">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3b989-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b989-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b989-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="3b989-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3b989-122">[**Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)類別實例的參考，該類別表示轉送資料庫的動態轉送專案。</span><span class="sxs-lookup"><span data-stu-id="3b989-122">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b989-123">備註</span><span class="sxs-lookup"><span data-stu-id="3b989-123">Remarks</span></span>

<span data-ttu-id="3b989-124">存取 **Msvm \_ SwitchPortDynamicForwarding** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="3b989-124">Access to the **Msvm\_SwitchPortDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3b989-125">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="3b989-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3b989-126">範例</span><span class="sxs-lookup"><span data-stu-id="3b989-126">Examples</span></span>

<span data-ttu-id="3b989-127">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="3b989-127">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b989-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b989-128">Requirements</span></span>



| <span data-ttu-id="3b989-129">需求</span><span class="sxs-lookup"><span data-stu-id="3b989-129">Requirement</span></span> | <span data-ttu-id="3b989-130">值</span><span class="sxs-lookup"><span data-stu-id="3b989-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b989-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b989-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3b989-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b989-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3b989-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b989-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3b989-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b989-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b989-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b989-135">Namespace</span></span><br/>                | <span data-ttu-id="3b989-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3b989-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3b989-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3b989-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b989-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3b989-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b989-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3b989-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b989-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b989-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b989-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b989-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b989-142">**CIM \_ SwitchPortDynamicForwarding**</span><span class="sxs-lookup"><span data-stu-id="3b989-142">**CIM\_SwitchPortDynamicForwarding**</span></span>](cim-switchportdynamicforwarding.md)
</dt> <dt>

<span data-ttu-id="3b989-143">[**CIM \_ SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b989-143">[**CIM\_SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span></span>
</dt> </dl>

 


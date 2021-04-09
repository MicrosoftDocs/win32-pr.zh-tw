---
description: 用來將虛擬機器與其 BIOS 產生關聯。
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Msvm_SystemBIOS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112305"
---
# <a name="msvm_systembios-class"></a><span data-ttu-id="72913-103">Msvm \_ SystemBIOS 類別</span><span class="sxs-lookup"><span data-stu-id="72913-103">Msvm\_SystemBIOS class</span></span>

<span data-ttu-id="72913-104">用來將虛擬機器與其 BIOS 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="72913-104">Used to associate a virtual machine with its BIOS.</span></span>

<span data-ttu-id="72913-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="72913-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72913-106">語法</span><span class="sxs-lookup"><span data-stu-id="72913-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="72913-107">成員</span><span class="sxs-lookup"><span data-stu-id="72913-107">Members</span></span>

<span data-ttu-id="72913-108">**Msvm \_ SystemBIOS** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="72913-108">The **Msvm\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="72913-109">屬性</span><span class="sxs-lookup"><span data-stu-id="72913-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72913-110">屬性</span><span class="sxs-lookup"><span data-stu-id="72913-110">Properties</span></span>

<span data-ttu-id="72913-111">**Msvm \_ SystemBIOS** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="72913-111">The **Msvm\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72913-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="72913-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72913-113">資料類型： **[ **CIM \_** 未執行](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="72913-113">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="72913-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72913-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72913-115">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="72913-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="72913-116">從 BIOS 啟動的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="72913-116">The virtual machine that starts from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="72913-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="72913-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72913-118">資料類型： **[ **Msvm \_ BIOSElement**](msvm-bioselement.md)**</span><span class="sxs-lookup"><span data-stu-id="72913-118">Data type: **[**Msvm\_BIOSElement**](msvm-bioselement.md)**</span></span>
</dt> <dt>

<span data-ttu-id="72913-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72913-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72913-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="72913-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="72913-121">與虛擬機器相關聯的 BIOS。</span><span class="sxs-lookup"><span data-stu-id="72913-121">The BIOS associated with the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72913-122">備註</span><span class="sxs-lookup"><span data-stu-id="72913-122">Remarks</span></span>

<span data-ttu-id="72913-123">存取 **Msvm \_ SystemBIOS** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="72913-123">Access to the **Msvm\_SystemBIOS** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="72913-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="72913-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="72913-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="72913-125">Requirements</span></span>



| <span data-ttu-id="72913-126">需求</span><span class="sxs-lookup"><span data-stu-id="72913-126">Requirement</span></span> | <span data-ttu-id="72913-127">值</span><span class="sxs-lookup"><span data-stu-id="72913-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72913-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72913-128">Minimum supported client</span></span><br/> | <span data-ttu-id="72913-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72913-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72913-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72913-130">Minimum supported server</span></span><br/> | <span data-ttu-id="72913-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72913-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72913-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="72913-132">Namespace</span></span><br/>                | <span data-ttu-id="72913-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="72913-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72913-134">MOF</span><span class="sxs-lookup"><span data-stu-id="72913-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72913-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="72913-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72913-136">DLL</span><span class="sxs-lookup"><span data-stu-id="72913-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72913-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72913-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72913-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72913-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72913-139">**CIM \_ SystemBIOS**</span><span class="sxs-lookup"><span data-stu-id="72913-139">**CIM\_SystemBIOS**</span></span>](cim-systembios.md)
</dt> <dt>

[<span data-ttu-id="72913-140">BIOS 類別</span><span class="sxs-lookup"><span data-stu-id="72913-140">BIOS Classes</span></span>](bios-classes.md)
</dt> </dl>

 


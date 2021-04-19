---
description: Msvm \_ VirtualSystemSettingData 實例與 Msvm VirtualSystemSettingData 實例之間的關聯 \_ ，代表這個物件所依據的最新快照集。
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Msvm_ParentChildSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000186"
---
# <a name="msvm_parentchildsettingdata-class"></a><span data-ttu-id="90467-103">Msvm \_ ParentChildSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="90467-103">Msvm\_ParentChildSettingData class</span></span>

<span data-ttu-id="90467-104">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)實例與 **Msvm \_ VirtualSystemSettingData** 實例之間的關聯，代表這個物件所依據的最新快照集。</span><span class="sxs-lookup"><span data-stu-id="90467-104">An association between an instance of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) and the **Msvm\_VirtualSystemSettingData** instance that represents the most recent snapshot upon which this object is based.</span></span>

<span data-ttu-id="90467-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="90467-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90467-106">語法</span><span class="sxs-lookup"><span data-stu-id="90467-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="90467-107">成員</span><span class="sxs-lookup"><span data-stu-id="90467-107">Members</span></span>

<span data-ttu-id="90467-108">**Msvm \_ ParentChildSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="90467-108">The **Msvm\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="90467-109">屬性</span><span class="sxs-lookup"><span data-stu-id="90467-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90467-110">屬性</span><span class="sxs-lookup"><span data-stu-id="90467-110">Properties</span></span>

<span data-ttu-id="90467-111">**Msvm \_ ParentChildSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="90467-111">The **Msvm\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90467-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="90467-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90467-113">資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="90467-113">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="90467-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90467-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90467-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) </span><span class="sxs-lookup"><span data-stu-id="90467-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="90467-116">子設定資料所依據的快照集設定資料。</span><span class="sxs-lookup"><span data-stu-id="90467-116">The snapshot setting data upon which the child setting data is based.</span></span>

</dd> <dt>

<span data-ttu-id="90467-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="90467-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90467-118">資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="90467-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="90467-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="90467-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90467-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="90467-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="90467-121">虛擬機器的設定資料，代表父系的子系。</span><span class="sxs-lookup"><span data-stu-id="90467-121">The setting data for the virtual machine that represents the child of the parent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90467-122">備註</span><span class="sxs-lookup"><span data-stu-id="90467-122">Remarks</span></span>

<span data-ttu-id="90467-123">存取 **Msvm \_ ParentChildSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="90467-123">Access to the **Msvm\_ParentChildSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="90467-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="90467-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="90467-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="90467-125">Requirements</span></span>



| <span data-ttu-id="90467-126">需求</span><span class="sxs-lookup"><span data-stu-id="90467-126">Requirement</span></span> | <span data-ttu-id="90467-127">值</span><span class="sxs-lookup"><span data-stu-id="90467-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90467-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90467-128">Minimum supported client</span></span><br/> | <span data-ttu-id="90467-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90467-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="90467-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90467-130">Minimum supported server</span></span><br/> | <span data-ttu-id="90467-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90467-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90467-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="90467-132">Namespace</span></span><br/>                | <span data-ttu-id="90467-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="90467-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90467-134">MOF</span><span class="sxs-lookup"><span data-stu-id="90467-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90467-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="90467-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90467-136">DLL</span><span class="sxs-lookup"><span data-stu-id="90467-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90467-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90467-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90467-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90467-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90467-139">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="90467-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="90467-140">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="90467-140">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[<span data-ttu-id="90467-141">虛擬系統類別</span><span class="sxs-lookup"><span data-stu-id="90467-141">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 


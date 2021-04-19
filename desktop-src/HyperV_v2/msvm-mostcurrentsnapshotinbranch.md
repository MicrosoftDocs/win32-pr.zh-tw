---
description: 將代表虛擬系統之 Msvm 系統的實例 \_ 或 Msvm \_ PlannedComputerSystem 類別的實例，與 \_ 代表相依快照集中最新快照集之虛擬系統快照集的 Msvm VirtualSystemSettingData 類別的實例產生關聯。
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Msvm_MostCurrentSnapshotInBranch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994539"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="6ecb5-103">Msvm \_ MostCurrentSnapshotInBranch 類別</span><span class="sxs-lookup"><span data-stu-id="6ecb5-103">Msvm\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="6ecb5-104">將代表虛擬系統之 [**Msvm \_**](msvm-computersystem.md) 系統的實例或 [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) 類別的實例，與代表相依快照集中最新快照集之虛擬系統快照集的 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別的實例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6ecb5-104">Associates an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing a virtual system, with an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class representing the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span>

<span data-ttu-id="6ecb5-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ecb5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ecb5-106">語法</span><span class="sxs-lookup"><span data-stu-id="6ecb5-106">Syntax</span></span>

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6ecb5-107">成員</span><span class="sxs-lookup"><span data-stu-id="6ecb5-107">Members</span></span>

<span data-ttu-id="6ecb5-108">**Msvm \_ MostCurrentSnapshotInBranch** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6ecb5-108">The **Msvm\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="6ecb5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6ecb5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ecb5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6ecb5-110">Properties</span></span>

<span data-ttu-id="6ecb5-111">**Msvm \_ MostCurrentSnapshotInBranch** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6ecb5-111">The **Msvm\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ecb5-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="6ecb5-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ecb5-113">資料類型： **[ **CIM \_** 未執行](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="6ecb5-113">Data type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>
</dt> <dt>

<span data-ttu-id="6ecb5-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ecb5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ecb5-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="6ecb5-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6ecb5-116">代表虛擬系統的 [**Msvm \_**](msvm-computersystem.md) 系統實例或 [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) 類別之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="6ecb5-116">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing the virtual system.</span></span> <span data-ttu-id="6ecb5-117">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="6ecb5-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="6ecb5-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6ecb5-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ecb5-119">資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="6ecb5-119">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6ecb5-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ecb5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ecb5-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="6ecb5-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6ecb5-122">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別之實例的參考，代表在相依快照集中分支中最新快照集的虛擬系統快照。</span><span class="sxs-lookup"><span data-stu-id="6ecb5-122">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span> <span data-ttu-id="6ecb5-123">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="6ecb5-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ecb5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ecb5-124">Requirements</span></span>



| <span data-ttu-id="6ecb5-125">需求</span><span class="sxs-lookup"><span data-stu-id="6ecb5-125">Requirement</span></span> | <span data-ttu-id="6ecb5-126">值</span><span class="sxs-lookup"><span data-stu-id="6ecb5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecb5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ecb5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ecb5-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ecb5-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ecb5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ecb5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ecb5-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ecb5-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ecb5-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ecb5-131">Namespace</span></span><br/>                | <span data-ttu-id="6ecb5-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6ecb5-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ecb5-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6ecb5-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ecb5-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb5-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ecb5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6ecb5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ecb5-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb5-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


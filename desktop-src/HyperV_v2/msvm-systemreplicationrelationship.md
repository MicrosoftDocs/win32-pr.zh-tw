---
description: 代表 Msvm 的實例（ \_ 代表虛擬機器的實例）與代表虛擬機器之複寫關聯性的 Msvm ReplicationRelationship 實例之間的關聯 \_ 。
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936652"
---
# <a name="msvm_systemreplicationrelationship-class"></a><span data-ttu-id="fa4fe-103">Msvm \_ SystemReplicationRelationship 類別</span><span class="sxs-lookup"><span data-stu-id="fa4fe-103">Msvm\_SystemReplicationRelationship class</span></span>

<span data-ttu-id="fa4fe-104">代表 Msvm 的實例（代表虛擬 [**機 \_**](msvm-computersystem.md) 的實例）與代表虛擬機器之複寫關聯性的 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 實例之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="fa4fe-104">Represents an association between an instance of [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the virtual machine and an instance of [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) that represents a replication relationship of the virtual machine.</span></span> <span data-ttu-id="fa4fe-105">此類別衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency) 性類別。</span><span class="sxs-lookup"><span data-stu-id="fa4fe-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="fa4fe-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa4fe-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4fe-107">語法</span><span class="sxs-lookup"><span data-stu-id="fa4fe-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fa4fe-108">成員</span><span class="sxs-lookup"><span data-stu-id="fa4fe-108">Members</span></span>

<span data-ttu-id="fa4fe-109">**Msvm \_ SystemReplicationRelationship** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fa4fe-109">The **Msvm\_SystemReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="fa4fe-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fa4fe-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa4fe-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fa4fe-111">Properties</span></span>

<span data-ttu-id="fa4fe-112">**Msvm \_ SystemReplicationRelationship** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fa4fe-112">The **Msvm\_SystemReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa4fe-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="fa4fe-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa4fe-114">資料類型： **Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="fa4fe-114">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="fa4fe-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa4fe-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa4fe-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) </span><span class="sxs-lookup"><span data-stu-id="fa4fe-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fa4fe-117">代表虛擬機器之 Msvm 實例 [**類別 \_**](msvm-computersystem.md) 的實例參考。</span><span class="sxs-lookup"><span data-stu-id="fa4fe-117">Reference to the instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fa4fe-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="fa4fe-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa4fe-119">資料類型： **Msvm \_ ReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="fa4fe-119">Data type: **Msvm\_ReplicationRelationship**</span></span>
</dt> <dt>

<span data-ttu-id="fa4fe-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa4fe-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa4fe-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="fa4fe-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fa4fe-122">參考 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別的實例，代表虛擬系統的複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="fa4fe-122">Reference to the instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that represents the replication relationship of a virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa4fe-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa4fe-123">Requirements</span></span>



| <span data-ttu-id="fa4fe-124">需求</span><span class="sxs-lookup"><span data-stu-id="fa4fe-124">Requirement</span></span> | <span data-ttu-id="fa4fe-125">值</span><span class="sxs-lookup"><span data-stu-id="fa4fe-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4fe-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa4fe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa4fe-127">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa4fe-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fa4fe-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa4fe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa4fe-129">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa4fe-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fa4fe-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa4fe-130">Namespace</span></span><br/>                | <span data-ttu-id="fa4fe-131">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="fa4fe-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa4fe-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fa4fe-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa4fe-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fa4fe-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa4fe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fa4fe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa4fe-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa4fe-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa4fe-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa4fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa4fe-137">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="fa4fe-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="fa4fe-138">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="fa4fe-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 


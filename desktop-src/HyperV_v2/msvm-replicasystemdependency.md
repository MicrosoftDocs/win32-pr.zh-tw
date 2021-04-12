---
description: 代表 CIM 系統類型實例之間的關聯 \_ ，該類別代表虛擬機器複本，以及 \_ 表示測試虛擬機器複本的 cim 系統類型實例。
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Msvm_ReplicaSystemDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192986"
---
# <a name="msvm_replicasystemdependency-class"></a><span data-ttu-id="d7059-103">Msvm \_ ReplicaSystemDependency 類別</span><span class="sxs-lookup"><span data-stu-id="d7059-103">Msvm\_ReplicaSystemDependency class</span></span>

<span data-ttu-id="d7059-104">代表 Cim 系統類型實例之間的關聯 [**， \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 該類別代表虛擬機器複本，以及表示測試虛擬機器複本的 **cim \_ 系統類型** 實例。</span><span class="sxs-lookup"><span data-stu-id="d7059-104">Represents an association between an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica and an instance of the **CIM\_ComputerSystem** class that represents the test virtual machine replica.</span></span>

<span data-ttu-id="d7059-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7059-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7059-106">語法</span><span class="sxs-lookup"><span data-stu-id="d7059-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d7059-107">成員</span><span class="sxs-lookup"><span data-stu-id="d7059-107">Members</span></span>

<span data-ttu-id="d7059-108">**Msvm \_ ReplicaSystemDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7059-108">The **Msvm\_ReplicaSystemDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="d7059-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d7059-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7059-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d7059-110">Properties</span></span>

<span data-ttu-id="d7059-111">**Msvm \_ ReplicaSystemDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7059-111">The **Msvm\_ReplicaSystemDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7059-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="d7059-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7059-113">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="d7059-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d7059-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7059-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7059-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) </span><span class="sxs-lookup"><span data-stu-id="d7059-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d7059-116">代表虛擬機器複本之 CIM 系統 [**類型 \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 實例的參考。</span><span class="sxs-lookup"><span data-stu-id="d7059-116">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica.</span></span> <span data-ttu-id="d7059-117">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="d7059-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="d7059-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="d7059-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7059-119">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="d7059-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d7059-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7059-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7059-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="d7059-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d7059-122">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)系統類型實例的參考，代表 [**Msvm \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md)方法所建立的測試虛擬機器複本。</span><span class="sxs-lookup"><span data-stu-id="d7059-122">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the test virtual machine replica created by the [**Msvm\_ReplicationService.TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) method.</span></span> <span data-ttu-id="d7059-123">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="d7059-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7059-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7059-124">Requirements</span></span>



| <span data-ttu-id="d7059-125">需求</span><span class="sxs-lookup"><span data-stu-id="d7059-125">Requirement</span></span> | <span data-ttu-id="d7059-126">值</span><span class="sxs-lookup"><span data-stu-id="d7059-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7059-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7059-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d7059-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7059-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d7059-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7059-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d7059-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7059-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7059-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7059-131">Namespace</span></span><br/>                | <span data-ttu-id="d7059-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d7059-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d7059-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d7059-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7059-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d7059-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7059-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d7059-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7059-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7059-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


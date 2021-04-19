---
description: 表示兩個計量定義或兩個度量值之間的關聯。
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Msvm_MetricCollectionDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982719"
---
# <a name="msvm_metriccollectiondependency-class"></a><span data-ttu-id="478e4-103">Msvm \_ MetricCollectionDependency 類別</span><span class="sxs-lookup"><span data-stu-id="478e4-103">Msvm\_MetricCollectionDependency class</span></span>

<span data-ttu-id="478e4-104">表示兩個計量定義或兩個度量值之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="478e4-104">Represents the association between two metric definitions or two metric values.</span></span>

<span data-ttu-id="478e4-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="478e4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="478e4-106">語法</span><span class="sxs-lookup"><span data-stu-id="478e4-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="478e4-107">成員</span><span class="sxs-lookup"><span data-stu-id="478e4-107">Members</span></span>

<span data-ttu-id="478e4-108">**Msvm \_ MetricCollectionDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="478e4-108">The **Msvm\_MetricCollectionDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="478e4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="478e4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="478e4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="478e4-110">Properties</span></span>

<span data-ttu-id="478e4-111">**Msvm \_ MetricCollectionDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="478e4-111">The **Msvm\_MetricCollectionDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="478e4-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="478e4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="478e4-113">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="478e4-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="478e4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="478e4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="478e4-115">[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別實例的參考，代表獨立的度量定義或計量值。</span><span class="sxs-lookup"><span data-stu-id="478e4-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the independent metric definition or metric value.</span></span> <span data-ttu-id="478e4-116">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="478e4-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="478e4-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="478e4-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="478e4-118">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="478e4-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="478e4-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="478e4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="478e4-120">[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別實例的參考，該類別表示相依于 **前面** 的計量定義或計量值。</span><span class="sxs-lookup"><span data-stu-id="478e4-120">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition or metric value that is dependent on the **Antecedent**.</span></span> <span data-ttu-id="478e4-121">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="478e4-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="478e4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="478e4-122">Requirements</span></span>



| <span data-ttu-id="478e4-123">需求</span><span class="sxs-lookup"><span data-stu-id="478e4-123">Requirement</span></span> | <span data-ttu-id="478e4-124">值</span><span class="sxs-lookup"><span data-stu-id="478e4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478e4-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="478e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="478e4-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="478e4-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="478e4-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="478e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="478e4-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="478e4-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="478e4-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="478e4-129">Namespace</span></span><br/>                | <span data-ttu-id="478e4-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="478e4-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="478e4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="478e4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="478e4-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="478e4-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="478e4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="478e4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="478e4-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="478e4-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


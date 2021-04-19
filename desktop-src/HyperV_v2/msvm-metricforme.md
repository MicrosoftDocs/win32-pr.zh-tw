---
description: 此關聯會將 managed 元素連結至為其維護的度量值。
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Msvm_MetricForME 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988433"
---
# <a name="msvm_metricforme-class"></a><span data-ttu-id="305a7-103">Msvm \_ MetricForME 類別</span><span class="sxs-lookup"><span data-stu-id="305a7-103">Msvm\_MetricForME class</span></span>

<span data-ttu-id="305a7-104">此關聯會將 managed 元素連結至為其維護的度量值。</span><span class="sxs-lookup"><span data-stu-id="305a7-104">This association links a managed element to the metric values being maintained for it.</span></span>

<span data-ttu-id="305a7-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="305a7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="305a7-106">語法</span><span class="sxs-lookup"><span data-stu-id="305a7-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="305a7-107">成員</span><span class="sxs-lookup"><span data-stu-id="305a7-107">Members</span></span>

<span data-ttu-id="305a7-108">**Msvm \_ MetricForME** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="305a7-108">The **Msvm\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="305a7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="305a7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="305a7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="305a7-110">Properties</span></span>

<span data-ttu-id="305a7-111">**Msvm \_ MetricForME** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="305a7-111">The **Msvm\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="305a7-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="305a7-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="305a7-113">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="305a7-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="305a7-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="305a7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="305a7-115">[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別之實例的參考，該類別表示具有由 **相依** 維護的計量所定義之計量的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="305a7-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that has metrics defined by **Dependent** maintained for it.</span></span> <span data-ttu-id="305a7-116">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="305a7-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="305a7-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="305a7-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="305a7-118">資料類型： \* \* \* \* CIM \_ BaseMetricValue \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="305a7-118">Data type: \*\*\*\*CIM\_BaseMetricValue\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="305a7-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="305a7-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="305a7-120">**CIM \_ BaseMetricValue** 類別實例的參考，表示之前為它 **收集的度量**。</span><span class="sxs-lookup"><span data-stu-id="305a7-120">A reference to an instance of the **CIM\_BaseMetricValue** class that represents the metric that the **Antecedent** has collected for it.</span></span> <span data-ttu-id="305a7-121">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="305a7-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="305a7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="305a7-122">Requirements</span></span>



| <span data-ttu-id="305a7-123">需求</span><span class="sxs-lookup"><span data-stu-id="305a7-123">Requirement</span></span> | <span data-ttu-id="305a7-124">值</span><span class="sxs-lookup"><span data-stu-id="305a7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="305a7-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="305a7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="305a7-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="305a7-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="305a7-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="305a7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="305a7-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="305a7-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="305a7-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="305a7-129">Namespace</span></span><br/>                | <span data-ttu-id="305a7-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="305a7-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="305a7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="305a7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="305a7-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="305a7-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="305a7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="305a7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="305a7-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="305a7-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


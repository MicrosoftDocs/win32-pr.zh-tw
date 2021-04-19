---
description: 定義 Msvm \_ BaseMetricDefinition 與 CIM ManagedElement 之間的關聯， \_ 以定義後者的度量。 計量定義是由 ManagedElement 提供的內容，這就是定義相依于元素的原因。
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Msvm_MetricDefForME 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983618"
---
# <a name="msvm_metricdefforme-class"></a><span data-ttu-id="4bcf7-104">Msvm \_ MetricDefForME 類別</span><span class="sxs-lookup"><span data-stu-id="4bcf7-104">Msvm\_MetricDefForME class</span></span>

<span data-ttu-id="4bcf7-105">定義 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 與 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 之間的關聯，以定義後者的度量。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-105">Defines the association between an [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) and a [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to define metrics for the latter.</span></span> <span data-ttu-id="4bcf7-106">計量定義是由 ManagedElement 提供的內容，這就是定義相依于元素的原因。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-106">The metrics definition is given context by the ManagedElement, which is why the definition is dependent on the element.</span></span>

<span data-ttu-id="4bcf7-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bcf7-108">語法</span><span class="sxs-lookup"><span data-stu-id="4bcf7-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="4bcf7-109">成員</span><span class="sxs-lookup"><span data-stu-id="4bcf7-109">Members</span></span>

<span data-ttu-id="4bcf7-110">**Msvm \_ MetricDefForME** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4bcf7-110">The **Msvm\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="4bcf7-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4bcf7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bcf7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4bcf7-112">Properties</span></span>

<span data-ttu-id="4bcf7-113">**Msvm \_ MetricDefForME** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-113">The **Msvm\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bcf7-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="4bcf7-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bcf7-115">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="4bcf7-115">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="4bcf7-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4bcf7-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bcf7-117">[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別之實例的參考，該類別代表可以套用 **相依的相依** 型別度量的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-117">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that can have metrics of the type defined by **Dependent** applied to it.</span></span> <span data-ttu-id="4bcf7-118">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="4bcf7-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="4bcf7-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bcf7-120">資料類型： **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="4bcf7-120">Data type: **[**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="4bcf7-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4bcf7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bcf7-122">[**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別實例的參考，該類別代表前 **一個可套用到它的度量** 定義。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-122">A reference to an instance of the [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition that the **Antecedent** can have applied to it.</span></span> <span data-ttu-id="4bcf7-123">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="4bcf7-124">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="4bcf7-124">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bcf7-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4bcf7-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4bcf7-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4bcf7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bcf7-127">指出是否正在為 **Antecedent** 收集 **相依** 的度量。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-127">Indicates whether the metric defined by **Dependent** is being collected for the **Antecedent**.</span></span> <span data-ttu-id="4bcf7-128">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-128">This will be one of the following values.</span></span>



| <span data-ttu-id="4bcf7-129">值</span><span class="sxs-lookup"><span data-stu-id="4bcf7-129">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="4bcf7-130">意義</span><span class="sxs-lookup"><span data-stu-id="4bcf7-130">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="4bcf7-131"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf7-131"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="4bcf7-132">正在收集度量。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-132">The metric is being collected.</span></span><br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="4bcf7-133"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf7-133"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="4bcf7-134">未收集度量。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-134">The metric is not being collected.</span></span><br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="4bcf7-135"><dt>**保留**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf7-135"><dt>**Reserved**</dt> <dt>4</dt></span></span> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <span data-ttu-id="4bcf7-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf7-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span></span> </dl> | <span data-ttu-id="4bcf7-137">系統會針對部分（而非全部）裝置收集度量。</span><span class="sxs-lookup"><span data-stu-id="4bcf7-137">The metric is being collected for some, but not all, devices.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bcf7-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bcf7-138">Requirements</span></span>



| <span data-ttu-id="4bcf7-139">需求</span><span class="sxs-lookup"><span data-stu-id="4bcf7-139">Requirement</span></span> | <span data-ttu-id="4bcf7-140">值</span><span class="sxs-lookup"><span data-stu-id="4bcf7-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcf7-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bcf7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4bcf7-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bcf7-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4bcf7-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bcf7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4bcf7-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bcf7-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4bcf7-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="4bcf7-145">Namespace</span></span><br/>                | <span data-ttu-id="4bcf7-146">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4bcf7-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4bcf7-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4bcf7-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bcf7-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf7-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bcf7-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4bcf7-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bcf7-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4bcf7-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


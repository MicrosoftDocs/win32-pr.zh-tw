---
description: CIM \_ SoftwareFeatureSAPImplementation 類別代表服務存取點之間的關聯 (SAP) 以及如何在軟體中執行。
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSAPImplementation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847052"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a><span data-ttu-id="8784f-103">CIM \_ SoftwareFeatureSAPImplementation 類別</span><span class="sxs-lookup"><span data-stu-id="8784f-103">CIM\_SoftwareFeatureSAPImplementation class</span></span>

<span data-ttu-id="8784f-104">**CIM \_ SoftwareFeatureSAPImplementation** 類別代表服務存取點之間的關聯 (SAP) 以及如何在軟體中執行。</span><span class="sxs-lookup"><span data-stu-id="8784f-104">The **CIM\_SoftwareFeatureSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented in software.</span></span> <span data-ttu-id="8784f-105">SAP 可由一個以上的軟體功能提供，以便彼此搭配運作。</span><span class="sxs-lookup"><span data-stu-id="8784f-105">A SAP can be provided by more than one software feature to operate in conjunction with one another.</span></span> <span data-ttu-id="8784f-106">此外，軟體功能可以提供一個以上的 SAP。</span><span class="sxs-lookup"><span data-stu-id="8784f-106">Additionally, a software feature can provide more than one SAP.</span></span> <span data-ttu-id="8784f-107">當有許多軟體功能與單一 SAP 相關聯時，會假設這些專案會搭配運作以提供存取點。</span><span class="sxs-lookup"><span data-stu-id="8784f-107">When many software features are associated with a single SAP, it is assumed that the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="8784f-108">如果有不同的 SAP 執行，每個實施都會導致 SAP 物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="8784f-108">If different implementations of a SAP exist, each implementation would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="8784f-109">然後，個別具現化會與唯一的實作為關聯。</span><span class="sxs-lookup"><span data-stu-id="8784f-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8784f-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8784f-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8784f-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8784f-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8784f-112">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8784f-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8784f-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8784f-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8784f-114">語法</span><span class="sxs-lookup"><span data-stu-id="8784f-114">Syntax</span></span>

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8784f-115">成員</span><span class="sxs-lookup"><span data-stu-id="8784f-115">Members</span></span>

<span data-ttu-id="8784f-116">**CIM \_ SoftwareFeatureSAPImplementation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8784f-116">The **CIM\_SoftwareFeatureSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="8784f-117">屬性</span><span class="sxs-lookup"><span data-stu-id="8784f-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8784f-118">屬性</span><span class="sxs-lookup"><span data-stu-id="8784f-118">Properties</span></span>

<span data-ttu-id="8784f-119">**CIM \_ SoftwareFeatureSAPImplementation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8784f-119">The **CIM\_SoftwareFeatureSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8784f-120">**先行**</span><span class="sxs-lookup"><span data-stu-id="8784f-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8784f-121">資料類型： **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="8784f-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="8784f-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8784f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8784f-123">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="8784f-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8784f-124">描述之前的軟體功能的 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) 。</span><span class="sxs-lookup"><span data-stu-id="8784f-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="8784f-125">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8784f-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8784f-126">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="8784f-126">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="8784f-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8784f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8784f-128">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="8784f-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8784f-129">描述相依服務存取點的 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) 。</span><span class="sxs-lookup"><span data-stu-id="8784f-129">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the dependent service access point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8784f-130">備註</span><span class="sxs-lookup"><span data-stu-id="8784f-130">Remarks</span></span>

<span data-ttu-id="8784f-131">**Cim \_ SoftwareFeatureSAPImplementation** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="8784f-131">The **CIM\_SoftwareFeatureSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8784f-132">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="8784f-132">WMI does not implement this class.</span></span>

<span data-ttu-id="8784f-133">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8784f-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8784f-134">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8784f-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8784f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="8784f-135">Requirements</span></span>



| <span data-ttu-id="8784f-136">需求</span><span class="sxs-lookup"><span data-stu-id="8784f-136">Requirement</span></span> | <span data-ttu-id="8784f-137">值</span><span class="sxs-lookup"><span data-stu-id="8784f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8784f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8784f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8784f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8784f-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8784f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8784f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8784f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8784f-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8784f-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="8784f-142">Namespace</span></span><br/>                | <span data-ttu-id="8784f-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8784f-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8784f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8784f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8784f-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8784f-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8784f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8784f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8784f-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8784f-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8784f-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8784f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8784f-149">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="8784f-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


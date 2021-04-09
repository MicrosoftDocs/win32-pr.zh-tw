---
description: CIM \_ ApplicationSystemSoftwareFeature 類別代表的關聯會識別組成特定應用程式系統的軟體功能。 軟體功能可以包含在不同的產品中。
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: CIM_ApplicationSystemSoftwareFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847444"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a><span data-ttu-id="24b7e-104">CIM \_ ApplicationSystemSoftwareFeature 類別</span><span class="sxs-lookup"><span data-stu-id="24b7e-104">CIM\_ApplicationSystemSoftwareFeature class</span></span>

<span data-ttu-id="24b7e-105">**CIM \_ ApplicationSystemSoftwareFeature** 類別代表的關聯會識別組成特定應用程式系統的軟體功能。</span><span class="sxs-lookup"><span data-stu-id="24b7e-105">The **CIM\_ApplicationSystemSoftwareFeature** class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="24b7e-106">軟體功能可以包含在不同的產品中。</span><span class="sxs-lookup"><span data-stu-id="24b7e-106">The software features can be included in different products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24b7e-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="24b7e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="24b7e-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="24b7e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="24b7e-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="24b7e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="24b7e-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="24b7e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b7e-111">語法</span><span class="sxs-lookup"><span data-stu-id="24b7e-111">Syntax</span></span>

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="24b7e-112">成員</span><span class="sxs-lookup"><span data-stu-id="24b7e-112">Members</span></span>

<span data-ttu-id="24b7e-113">**CIM \_ ApplicationSystemSoftwareFeature** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24b7e-113">The **CIM\_ApplicationSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="24b7e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="24b7e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24b7e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="24b7e-115">Properties</span></span>

<span data-ttu-id="24b7e-116">**CIM \_ ApplicationSystemSoftwareFeature** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="24b7e-116">The **CIM\_ApplicationSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24b7e-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="24b7e-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b7e-118">資料類型： **CIM \_ ApplicationSystem**</span><span class="sxs-lookup"><span data-stu-id="24b7e-118">Data type: **CIM\_ApplicationSystem**</span></span>
</dt> <dt>

<span data-ttu-id="24b7e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b7e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b7e-120">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="24b7e-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="24b7e-121">在關聯中包含父系統的 [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="24b7e-121">A [**CIM\_ApplicationSystem**](cim-applicationsystem.md) that contains the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="24b7e-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="24b7e-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b7e-123">資料類型： **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="24b7e-123">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="24b7e-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b7e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b7e-125">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="24b7e-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="24b7e-126">[**CIM \_ SoftwareFeature**](cim-softwarefeature.md) ，其中包含屬於系統元件的子項目。</span><span class="sxs-lookup"><span data-stu-id="24b7e-126">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that contain the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24b7e-127">備註</span><span class="sxs-lookup"><span data-stu-id="24b7e-127">Remarks</span></span>

<span data-ttu-id="24b7e-128">**Cim \_ ApplicationSystemSoftwareFeature** 類別衍生自 [**cim \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="24b7e-128">The **CIM\_ApplicationSystemSoftwareFeature** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="24b7e-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="24b7e-129">WMI does not implement this class.</span></span>

<span data-ttu-id="24b7e-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="24b7e-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="24b7e-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="24b7e-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b7e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="24b7e-132">Requirements</span></span>



| <span data-ttu-id="24b7e-133">需求</span><span class="sxs-lookup"><span data-stu-id="24b7e-133">Requirement</span></span> | <span data-ttu-id="24b7e-134">值</span><span class="sxs-lookup"><span data-stu-id="24b7e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24b7e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24b7e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="24b7e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24b7e-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24b7e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24b7e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="24b7e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24b7e-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24b7e-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="24b7e-139">Namespace</span></span><br/>                | <span data-ttu-id="24b7e-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="24b7e-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24b7e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="24b7e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24b7e-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="24b7e-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24b7e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="24b7e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24b7e-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24b7e-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b7e-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24b7e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b7e-146">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="24b7e-146">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 


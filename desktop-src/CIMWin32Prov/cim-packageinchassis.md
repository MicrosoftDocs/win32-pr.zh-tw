---
description: CIM \_ PackageInChassis 關聯代表底座可包含其他套件的關聯性，例如其他底座和卡片。
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: CIM_PackageInChassis 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468265"
---
# <a name="cim_packageinchassis-class"></a><span data-ttu-id="48248-103">CIM \_ PackageInChassis 類別</span><span class="sxs-lookup"><span data-stu-id="48248-103">CIM\_PackageInChassis class</span></span>

<span data-ttu-id="48248-104">**CIM \_ PackageInChassis** 關聯代表底座可包含其他套件的關聯性，例如其他底座和卡片。</span><span class="sxs-lookup"><span data-stu-id="48248-104">The **CIM\_PackageInChassis** association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48248-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="48248-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48248-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="48248-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48248-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="48248-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="48248-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="48248-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48248-109">語法</span><span class="sxs-lookup"><span data-stu-id="48248-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="48248-110">成員</span><span class="sxs-lookup"><span data-stu-id="48248-110">Members</span></span>

<span data-ttu-id="48248-111">**CIM \_ PackageInChassis** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="48248-111">The **CIM\_PackageInChassis** class has these types of members:</span></span>

-   [<span data-ttu-id="48248-112">屬性</span><span class="sxs-lookup"><span data-stu-id="48248-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48248-113">屬性</span><span class="sxs-lookup"><span data-stu-id="48248-113">Properties</span></span>

<span data-ttu-id="48248-114">**CIM \_ PackageInChassis** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="48248-114">The **CIM\_PackageInChassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48248-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="48248-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48248-116">資料類型： **CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="48248-116">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="48248-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="48248-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48248-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="48248-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="48248-119">[**CIM \_ 底座**](cim-chassis.md)，描述包含其他實體套件的底座。</span><span class="sxs-lookup"><span data-stu-id="48248-119">A [**CIM\_Chassis**](cim-chassis.md) describing the chassis that contains other physical packages.</span></span>

</dd> <dt>

<span data-ttu-id="48248-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="48248-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48248-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="48248-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48248-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="48248-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48248-123">自由格式的字串，表示實體元素在實體封裝內的位置。</span><span class="sxs-lookup"><span data-stu-id="48248-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="48248-124">與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="48248-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="48248-125">此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="48248-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="48248-126">這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="48248-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="48248-127">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="48248-127">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48248-128">資料類型： **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="48248-128">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="48248-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="48248-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48248-130">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="48248-130">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="48248-131">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，描述包含在底座中的實體套件。</span><span class="sxs-lookup"><span data-stu-id="48248-131">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package which is contained in the chassis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48248-132">備註</span><span class="sxs-lookup"><span data-stu-id="48248-132">Remarks</span></span>

<span data-ttu-id="48248-133">**Cim \_ PackageInChassis** 類別衍生自 [**cim \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="48248-133">The **CIM\_PackageInChassis** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="48248-134">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="48248-134">WMI does not implement this class.</span></span>

<span data-ttu-id="48248-135">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="48248-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48248-136">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="48248-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48248-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="48248-137">Requirements</span></span>



| <span data-ttu-id="48248-138">需求</span><span class="sxs-lookup"><span data-stu-id="48248-138">Requirement</span></span> | <span data-ttu-id="48248-139">值</span><span class="sxs-lookup"><span data-stu-id="48248-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48248-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48248-140">Minimum supported client</span></span><br/> | <span data-ttu-id="48248-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48248-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48248-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48248-142">Minimum supported server</span></span><br/> | <span data-ttu-id="48248-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48248-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48248-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="48248-144">Namespace</span></span><br/>                | <span data-ttu-id="48248-145">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="48248-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48248-146">MOF</span><span class="sxs-lookup"><span data-stu-id="48248-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48248-147"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="48248-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48248-148">DLL</span><span class="sxs-lookup"><span data-stu-id="48248-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48248-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48248-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48248-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48248-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48248-151">**CIM \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="48248-151">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 


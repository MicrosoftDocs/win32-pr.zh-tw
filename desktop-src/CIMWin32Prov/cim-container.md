---
description: CIM \_ 容器類別表示包含的實體元素與包含的實體專案之間的關聯。 包含的物件必須是實體封裝。
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: CIM_Container 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70aca54c80a954deed88d1ec740f0057753bf5e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936355"
---
# <a name="cim_container-class"></a><span data-ttu-id="02e53-104">CIM \_ 容器類別</span><span class="sxs-lookup"><span data-stu-id="02e53-104">CIM\_Container class</span></span>

<span data-ttu-id="02e53-105">**CIM \_ 容器** 類別表示包含的實體元素與包含的實體專案之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="02e53-105">The **CIM\_Container** class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="02e53-106">包含的物件必須是實體封裝。</span><span class="sxs-lookup"><span data-stu-id="02e53-106">A containing object must be a physical package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02e53-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="02e53-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02e53-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="02e53-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="02e53-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="02e53-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="02e53-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="02e53-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e53-111">語法</span><span class="sxs-lookup"><span data-stu-id="02e53-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a><span data-ttu-id="02e53-112">成員</span><span class="sxs-lookup"><span data-stu-id="02e53-112">Members</span></span>

<span data-ttu-id="02e53-113">**CIM \_ 容器** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="02e53-113">The **CIM\_Container** class has these types of members:</span></span>

-   [<span data-ttu-id="02e53-114">屬性</span><span class="sxs-lookup"><span data-stu-id="02e53-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02e53-115">屬性</span><span class="sxs-lookup"><span data-stu-id="02e53-115">Properties</span></span>

<span data-ttu-id="02e53-116">**CIM \_ 容器** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="02e53-116">The **CIM\_Container** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02e53-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="02e53-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02e53-118">資料類型： **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="02e53-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="02e53-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02e53-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02e53-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="02e53-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="02e53-121">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，代表包含其他實體元素（包括其他封裝）的實體套件。</span><span class="sxs-lookup"><span data-stu-id="02e53-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that represents the physical package that contains other physical elements, including other packages.</span></span>

</dd> <dt>

<span data-ttu-id="02e53-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="02e53-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02e53-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02e53-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02e53-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02e53-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02e53-125">自由格式的字串，表示實體元素在實體封裝內的位置。</span><span class="sxs-lookup"><span data-stu-id="02e53-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="02e53-126">與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="02e53-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="02e53-127">此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="02e53-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="02e53-128">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="02e53-128">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02e53-129">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="02e53-129">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="02e53-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02e53-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02e53-131">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="02e53-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="02e53-132">[**CIM \_ PhysicalElement**](cim-physicalelement.md) ，描述包含在封裝中的實體元素。</span><span class="sxs-lookup"><span data-stu-id="02e53-132">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02e53-133">備註</span><span class="sxs-lookup"><span data-stu-id="02e53-133">Remarks</span></span>

<span data-ttu-id="02e53-134">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="02e53-134">WMI does not implement this class.</span></span> <span data-ttu-id="02e53-135">如需衍生自 **CIM \_ 容器** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="02e53-135">For more information about classes derived from **CIM\_Container**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="02e53-136">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="02e53-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02e53-137">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="02e53-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e53-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="02e53-138">Requirements</span></span>



| <span data-ttu-id="02e53-139">需求</span><span class="sxs-lookup"><span data-stu-id="02e53-139">Requirement</span></span> | <span data-ttu-id="02e53-140">值</span><span class="sxs-lookup"><span data-stu-id="02e53-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e53-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02e53-141">Minimum supported client</span></span><br/> | <span data-ttu-id="02e53-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02e53-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02e53-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02e53-143">Minimum supported server</span></span><br/> | <span data-ttu-id="02e53-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02e53-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02e53-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="02e53-145">Namespace</span></span><br/>                | <span data-ttu-id="02e53-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="02e53-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02e53-147">MOF</span><span class="sxs-lookup"><span data-stu-id="02e53-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02e53-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="02e53-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02e53-149">DLL</span><span class="sxs-lookup"><span data-stu-id="02e53-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e53-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02e53-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02e53-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02e53-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e53-152">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="02e53-152">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


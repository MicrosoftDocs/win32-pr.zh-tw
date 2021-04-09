---
description: CIM \_ ConnectorOnPackage 類別代表的關聯，會明確指出連接器與封裝之間的內含專案關聯性。 實體套件包含連接器和其他實體元素。
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: CIM_ConnectorOnPackage 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847398"
---
# <a name="cim_connectoronpackage-class"></a><span data-ttu-id="5e3bf-104">CIM \_ ConnectorOnPackage 類別</span><span class="sxs-lookup"><span data-stu-id="5e3bf-104">CIM\_ConnectorOnPackage class</span></span>

<span data-ttu-id="5e3bf-105">**CIM \_ ConnectorOnPackage** 類別代表的關聯，會明確指出連接器與封裝之間的內含專案關聯性。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-105">The **CIM\_ConnectorOnPackage** class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="5e3bf-106">實體套件包含連接器和其他實體元素。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-106">Physical packages contain connectors as well as other physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e3bf-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5e3bf-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5e3bf-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5e3bf-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e3bf-111">語法</span><span class="sxs-lookup"><span data-stu-id="5e3bf-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="5e3bf-112">成員</span><span class="sxs-lookup"><span data-stu-id="5e3bf-112">Members</span></span>

<span data-ttu-id="5e3bf-113">**CIM \_ ConnectorOnPackage** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5e3bf-113">The **CIM\_ConnectorOnPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="5e3bf-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5e3bf-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e3bf-115">屬性</span><span class="sxs-lookup"><span data-stu-id="5e3bf-115">Properties</span></span>

<span data-ttu-id="5e3bf-116">**CIM \_ ConnectorOnPackage** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-116">The **CIM\_ConnectorOnPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e3bf-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3bf-118">資料類型： **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="5e3bf-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e3bf-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e3bf-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="5e3bf-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5e3bf-121">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，描述具有連接器的實體套件。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="5e3bf-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3bf-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e3bf-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e3bf-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3bf-125">自由格式的字串，表示實體元素在實體封裝內的位置。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="5e3bf-126">與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="5e3bf-127">此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="5e3bf-128">這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e3bf-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3bf-130">資料類型： **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-130">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="5e3bf-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e3bf-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e3bf-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="5e3bf-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5e3bf-133">描述實體連接器的 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) 。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-133">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e3bf-134">備註</span><span class="sxs-lookup"><span data-stu-id="5e3bf-134">Remarks</span></span>

<span data-ttu-id="5e3bf-135">**Cim \_ ConnectorOnPackage** 類別衍生自 [**cim \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-135">The **CIM\_ConnectorOnPackage** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="5e3bf-136">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-136">WMI does not implement this class.</span></span>

<span data-ttu-id="5e3bf-137">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5e3bf-138">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5e3bf-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3bf-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e3bf-139">Requirements</span></span>



| <span data-ttu-id="5e3bf-140">需求</span><span class="sxs-lookup"><span data-stu-id="5e3bf-140">Requirement</span></span> | <span data-ttu-id="5e3bf-141">值</span><span class="sxs-lookup"><span data-stu-id="5e3bf-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3bf-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e3bf-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3bf-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e3bf-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e3bf-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e3bf-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3bf-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e3bf-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e3bf-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="5e3bf-146">Namespace</span></span><br/>                | <span data-ttu-id="5e3bf-147">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5e3bf-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e3bf-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5e3bf-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e3bf-149"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e3bf-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e3bf-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5e3bf-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e3bf-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e3bf-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e3bf-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e3bf-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3bf-153">**CIM \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 


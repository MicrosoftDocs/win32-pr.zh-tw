---
description: CIM \_ ChassisInRack 關聯代表 &\# 0034; 包含&\# 0034; 機架與其包含的底座之間的關聯性。
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: CIM_ChassisInRack 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110997"
---
# <a name="cim_chassisinrack-class"></a><span data-ttu-id="89b3b-103">CIM \_ ChassisInRack 類別</span><span class="sxs-lookup"><span data-stu-id="89b3b-103">CIM\_ChassisInRack class</span></span>

<span data-ttu-id="89b3b-104">**CIM \_ ChassisInRack** 關聯代表機架與其包含的底座之間的「包含」關聯性。</span><span class="sxs-lookup"><span data-stu-id="89b3b-104">The **CIM\_ChassisInRack** association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89b3b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="89b3b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89b3b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="89b3b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89b3b-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="89b3b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="89b3b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="89b3b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b3b-109">語法</span><span class="sxs-lookup"><span data-stu-id="89b3b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a><span data-ttu-id="89b3b-110">成員</span><span class="sxs-lookup"><span data-stu-id="89b3b-110">Members</span></span>

<span data-ttu-id="89b3b-111">**CIM \_ ChassisInRack** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89b3b-111">The **CIM\_ChassisInRack** class has these types of members:</span></span>

-   [<span data-ttu-id="89b3b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="89b3b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89b3b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="89b3b-113">Properties</span></span>

<span data-ttu-id="89b3b-114">**CIM \_ ChassisInRack** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="89b3b-114">The **CIM\_ChassisInRack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89b3b-115">**BottomU**</span><span class="sxs-lookup"><span data-stu-id="89b3b-115">**BottomU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b3b-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89b3b-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89b3b-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89b3b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b3b-118">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Us" ) </span><span class="sxs-lookup"><span data-stu-id="89b3b-118">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="89b3b-119">整數，表示裝載底座的最低或底部 "U"。</span><span class="sxs-lookup"><span data-stu-id="89b3b-119">Integer that indicates the lowest or bottom "U" in which the chassis is mounted.</span></span> <span data-ttu-id="89b3b-120">「U」是一種標準測量單位，適用于機架的高度或可供機架使用的元件，並等於1.75 英寸或4.445 釐米。</span><span class="sxs-lookup"><span data-stu-id="89b3b-120">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="89b3b-121">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="89b3b-121">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b3b-122">資料類型： **CIM \_ 機架**</span><span class="sxs-lookup"><span data-stu-id="89b3b-122">Data type: **CIM\_Rack**</span></span>
</dt> <dt>

<span data-ttu-id="89b3b-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89b3b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b3b-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="89b3b-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="89b3b-125">[**CIM \_ 機架**](cim-rack.md)，描述包含底座的機架。</span><span class="sxs-lookup"><span data-stu-id="89b3b-125">A [**CIM\_Rack**](cim-rack.md) that describes the rack that contains the chassis.</span></span>

</dd> <dt>

<span data-ttu-id="89b3b-126">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="89b3b-126">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b3b-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89b3b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89b3b-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89b3b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89b3b-129">自由格式的字串，表示實體元素在實體封裝內的位置。</span><span class="sxs-lookup"><span data-stu-id="89b3b-129">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="89b3b-130">與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="89b3b-130">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="89b3b-131">此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="89b3b-131">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="89b3b-132">這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="89b3b-132">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="89b3b-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="89b3b-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b3b-134">資料類型： **CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="89b3b-134">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="89b3b-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89b3b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b3b-136">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="89b3b-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="89b3b-137">[**CIM \_ 底座**](cim-chassis.md)，可描述掛接在機架中的底座。</span><span class="sxs-lookup"><span data-stu-id="89b3b-137">A [**CIM\_Chassis**](cim-chassis.md) that describes the chassis which is mounted in the rack.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89b3b-138">備註</span><span class="sxs-lookup"><span data-stu-id="89b3b-138">Remarks</span></span>

<span data-ttu-id="89b3b-139">**Cim \_ ChassisInRack** 類別衍生自 [**cim \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="89b3b-139">The **CIM\_ChassisInRack** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="89b3b-140">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="89b3b-140">WMI does not implement this class.</span></span>

<span data-ttu-id="89b3b-141">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="89b3b-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89b3b-142">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="89b3b-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b3b-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="89b3b-143">Requirements</span></span>



| <span data-ttu-id="89b3b-144">需求</span><span class="sxs-lookup"><span data-stu-id="89b3b-144">Requirement</span></span> | <span data-ttu-id="89b3b-145">值</span><span class="sxs-lookup"><span data-stu-id="89b3b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89b3b-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89b3b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="89b3b-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89b3b-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89b3b-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89b3b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="89b3b-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89b3b-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89b3b-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="89b3b-150">Namespace</span></span><br/>                | <span data-ttu-id="89b3b-151">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="89b3b-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89b3b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="89b3b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89b3b-153"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="89b3b-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89b3b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="89b3b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89b3b-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89b3b-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b3b-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89b3b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b3b-157">**CIM \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="89b3b-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 


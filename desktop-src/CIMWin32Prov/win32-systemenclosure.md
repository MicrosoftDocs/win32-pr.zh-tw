---
description: 代表與實體系統主機殼相關聯的屬性。
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Win32_SystemEnclosure 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936482"
---
# <a name="win32_systemenclosure-class"></a><span data-ttu-id="5a865-103">Win32 \_ SystemEnclosure 類別</span><span class="sxs-lookup"><span data-stu-id="5a865-103">Win32\_SystemEnclosure class</span></span>

<span data-ttu-id="5a865-104">**Win32 \_ SystemEnclosure** [WMI 類別](../wmisdk/retrieving-a-class.md)代表與實體系統主機殼相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a865-104">The **Win32\_SystemEnclosure** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties that are associated with a physical system enclosure.</span></span>

<span data-ttu-id="5a865-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a865-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5a865-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5a865-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a865-107">語法</span><span class="sxs-lookup"><span data-stu-id="5a865-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="5a865-108">成員</span><span class="sxs-lookup"><span data-stu-id="5a865-108">Members</span></span>

<span data-ttu-id="5a865-109">**Win32 \_ SystemEnclosure** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5a865-109">The **Win32\_SystemEnclosure** class has these types of members:</span></span>

-   [<span data-ttu-id="5a865-110">方法</span><span class="sxs-lookup"><span data-stu-id="5a865-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a865-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5a865-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a865-112">方法</span><span class="sxs-lookup"><span data-stu-id="5a865-112">Methods</span></span>

<span data-ttu-id="5a865-113">**Win32 \_ SystemEnclosure** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5a865-113">The **Win32\_SystemEnclosure** class has these methods.</span></span>



| <span data-ttu-id="5a865-114">方法</span><span class="sxs-lookup"><span data-stu-id="5a865-114">Method</span></span>           | <span data-ttu-id="5a865-115">描述</span><span class="sxs-lookup"><span data-stu-id="5a865-115">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="5a865-116">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="5a865-116">**IsCompatible**</span></span> | <span data-ttu-id="5a865-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="5a865-117">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5a865-118">屬性</span><span class="sxs-lookup"><span data-stu-id="5a865-118">Properties</span></span>

<span data-ttu-id="5a865-119">**Win32 \_ SystemEnclosure** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5a865-119">The **Win32\_SystemEnclosure** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a865-120">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="5a865-120">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-121">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5a865-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-123">若 **為 TRUE**，則框架具有可聽見的警示。</span><span class="sxs-lookup"><span data-stu-id="5a865-123">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="5a865-124">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-124">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-125">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="5a865-125">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-128">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**") </span><span class="sxs-lookup"><span data-stu-id="5a865-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-129">**SecurityBreach** 屬性指出發生安全性相關事件時提供詳細資訊的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="5a865-129">Free-form string that provides more information if the **SecurityBreach** property indicates that a security-related event occurred.</span></span>

<span data-ttu-id="5a865-130">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-130">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-131">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="5a865-131">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-134">自由格式的字串，其中包含有關如何連接及配套框架的各種纜線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5a865-134">Free-form string that contains information about how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="5a865-135">使用許多網路、儲存體相關和電源線，纜線管理可能是複雜且富有挑戰性的工作。</span><span class="sxs-lookup"><span data-stu-id="5a865-135">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="5a865-136">這個屬性所包含的資訊可協助框架的元件和服務。</span><span class="sxs-lookup"><span data-stu-id="5a865-136">This property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="5a865-137">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-137">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="5a865-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-141">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-141">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-142">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="5a865-142">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="5a865-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-144">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="5a865-144">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-145">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5a865-145">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a865-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-147">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 實體容器 Global Table \| 002.1 ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ 底座**](cim-chassis.md)。**TypeDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="5a865-147">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-148">底座類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="5a865-148">Array of chassis types.</span></span>

<span data-ttu-id="5a865-149">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="5a865-149">This value comes from the **Type** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5a865-150">這個屬性繼承自 [**CIM \_ 底座**](cim-chassis.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-150">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a865-151">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5a865-151">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a865-152">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5a865-152">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="5a865-153">**桌面** (3) </span><span class="sxs-lookup"><span data-stu-id="5a865-153">**Desktop** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="5a865-154">**低設定檔桌面** (4) </span><span class="sxs-lookup"><span data-stu-id="5a865-154">**Low Profile Desktop** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="5a865-155">**比薩 Box** (5) </span><span class="sxs-lookup"><span data-stu-id="5a865-155">**Pizza Box** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="5a865-156">**迷你塔式** (6) </span><span class="sxs-lookup"><span data-stu-id="5a865-156">**Mini Tower** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="5a865-157">**塔** (7) </span><span class="sxs-lookup"><span data-stu-id="5a865-157">**Tower** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="5a865-158">**便攜** (8) </span><span class="sxs-lookup"><span data-stu-id="5a865-158">**Portable** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="5a865-159">**膝上型電腦** (9) </span><span class="sxs-lookup"><span data-stu-id="5a865-159">**Laptop** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="5a865-160">**筆記本** (10) </span><span class="sxs-lookup"><span data-stu-id="5a865-160">**Notebook** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="5a865-161">**保留** (11) </span><span class="sxs-lookup"><span data-stu-id="5a865-161">**Hand Held** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="5a865-162">**銜接站** (12) </span><span class="sxs-lookup"><span data-stu-id="5a865-162">**Docking Station** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="5a865-163">**全都在一個** (13) </span><span class="sxs-lookup"><span data-stu-id="5a865-163">**All in One** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="5a865-164">**子筆記本** (14) </span><span class="sxs-lookup"><span data-stu-id="5a865-164">**Sub Notebook** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="5a865-165">**節省空間** (15) </span><span class="sxs-lookup"><span data-stu-id="5a865-165">**Space-Saving** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="5a865-166"> (16) **午餐箱**</span><span class="sxs-lookup"><span data-stu-id="5a865-166">**Lunch Box** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="5a865-167">**主要系統底座** (17) </span><span class="sxs-lookup"><span data-stu-id="5a865-167">**Main System Chassis** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="5a865-168">**擴充底座** (18) </span><span class="sxs-lookup"><span data-stu-id="5a865-168">**Expansion Chassis** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="5a865-169">**SubChassis** (19) </span><span class="sxs-lookup"><span data-stu-id="5a865-169">**SubChassis** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="5a865-170">**匯流排擴充底座** (20) </span><span class="sxs-lookup"><span data-stu-id="5a865-170">**Bus Expansion Chassis** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="5a865-171">**週邊底座** (21) </span><span class="sxs-lookup"><span data-stu-id="5a865-171">**Peripheral Chassis** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="5a865-172">**儲存體底座** (22) </span><span class="sxs-lookup"><span data-stu-id="5a865-172">**Storage Chassis** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="5a865-173">**機架掛接底座** (23) </span><span class="sxs-lookup"><span data-stu-id="5a865-173">**Rack Mount Chassis** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="5a865-174">**Sealed-CASE PC** (24) </span><span class="sxs-lookup"><span data-stu-id="5a865-174">**Sealed-Case PC** (24)</span></span>

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

<span data-ttu-id="5a865-175">**Tablet** (30) </span><span class="sxs-lookup"><span data-stu-id="5a865-175">**Tablet** (30)</span></span>

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

<span data-ttu-id="5a865-176">**可轉換** (31) </span><span class="sxs-lookup"><span data-stu-id="5a865-176">**Convertible** (31)</span></span>

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

<span data-ttu-id="5a865-177">可卸離 **的 (32**) </span><span class="sxs-lookup"><span data-stu-id="5a865-177">**Detachable** (32)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a865-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a865-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-181">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="5a865-181">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a865-182">第一個實體類別的名稱，這個類別會出現在用於建立實例的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="5a865-182">Name of the first concrete class that appears in the inheritance chain that is used in the creation of an instance.</span></span> <span data-ttu-id="5a865-183">搭配類別的其他索引鍵屬性使用時，此屬性可讓您以唯一的方式識別此類別和其子類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="5a865-183">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="5a865-184">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-184">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-185">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="5a865-185">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-186">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="5a865-186">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-188">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "安培 at 120 伏特" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-188">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-189">120V 底座所需的最新。</span><span class="sxs-lookup"><span data-stu-id="5a865-189">Current that is required by the chassis at 120V.</span></span> <span data-ttu-id="5a865-190">如果電源是由底座提供—就像是不斷電供應系統供應 (UPS) 一樣，此屬性可能會指出 amperage 產生的 (是) 的負數。</span><span class="sxs-lookup"><span data-stu-id="5a865-190">If power is provided by the chassis—as in the case of an uninterruptible power supply (UPS)—this property may indicate the amperage produced (as a negative number).</span></span>

<span data-ttu-id="5a865-191">這個屬性繼承自 [**CIM \_ 底座**](cim-chassis.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-191">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-192">**深度**</span><span class="sxs-lookup"><span data-stu-id="5a865-192">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-193">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="5a865-193">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-195">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-195">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-196">實體封裝的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a865-196">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="5a865-197">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-197">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-198">**說明**</span><span class="sxs-lookup"><span data-stu-id="5a865-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-201">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-201">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-202">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5a865-202">Description of the object.</span></span>

<span data-ttu-id="5a865-203">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-204">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="5a865-204">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-205">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5a865-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-207">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每小時 BTU」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-207">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-208">底座在 BTU/小時內產生的熱度數量。</span><span class="sxs-lookup"><span data-stu-id="5a865-208">Amount of heat that is generated by the chassis in BTU/hour.</span></span>

<span data-ttu-id="5a865-209">這個屬性繼承自 [**CIM \_ 底座**](cim-chassis.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-209">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-210">**高度**</span><span class="sxs-lookup"><span data-stu-id="5a865-210">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-211">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="5a865-211">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-213">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-213">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-214">實體封裝的高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a865-214">Height of the physical package—in inches.</span></span>

<span data-ttu-id="5a865-215">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-215">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-216">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="5a865-216">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-217">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5a865-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-219">若為 **TRUE**，則實體封裝可進行熱交換 (如果可以將專案取代為實體不同但對等的專案，但包含的套件已套用電源) 。</span><span class="sxs-lookup"><span data-stu-id="5a865-219">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="5a865-220">例如，使用 SCA 連接器插入的磁片磁碟機封裝會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="5a865-220">For example, a disk drive package that is inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="5a865-221">所有可以熱交換的封裝，本質上都是卸載且可取代的。</span><span class="sxs-lookup"><span data-stu-id="5a865-221">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="5a865-222">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-222">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-223">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5a865-223">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-224">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5a865-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-226">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="5a865-226">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-227">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5a865-227">Date and time the object was installed.</span></span> <span data-ttu-id="5a865-228">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="5a865-228">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5a865-229">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-230">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="5a865-230">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5a865-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-233">若 **為 TRUE**，則會使用鎖定來保護框架。</span><span class="sxs-lookup"><span data-stu-id="5a865-233">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="5a865-234">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-234">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-235">**製造商**</span><span class="sxs-lookup"><span data-stu-id="5a865-235">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-238">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="5a865-238">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a865-239">產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="5a865-239">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="5a865-240">此值來自于 **系統主機殼** 的 **製造商** 成員或 SMBIOS 資訊中的底座結構。</span><span class="sxs-lookup"><span data-stu-id="5a865-240">This value comes from the **Manufacturer** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5a865-241">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-241">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-242">**型號**</span><span class="sxs-lookup"><span data-stu-id="5a865-242">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-245">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5a865-245">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a865-246">已知實體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a865-246">Name by which the physical element is known.</span></span>

<span data-ttu-id="5a865-247">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-247">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-248">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5a865-248">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-251">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-251">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-252">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="5a865-252">Label by which the object is known.</span></span> <span data-ttu-id="5a865-253">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="5a865-253">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5a865-254">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-255">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="5a865-255">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-256">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5a865-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-258">必須連接到底座才能操作所有元件的電源線數目。</span><span class="sxs-lookup"><span data-stu-id="5a865-258">Number of power cords that must be connected to the chassis for all of the components to operate.</span></span>

<span data-ttu-id="5a865-259">這個屬性繼承自 [**CIM \_ 底座**](cim-chassis.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-259">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-260">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5a865-260">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-263">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="5a865-263">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5a865-264">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="5a865-264">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="5a865-265">請注意，如果只有條碼資料可供使用，而且是唯一的或可作為專案索引鍵，則在 tag 屬性中，此屬性會是 **Null** 和用來當做類別索引鍵的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="5a865-265">Be aware that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="5a865-266">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-266">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-267">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="5a865-267">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-270">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="5a865-270">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a865-271">由產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="5a865-271">Part number that is assigned by the organization that produces or manufacturing the physical element.</span></span>

<span data-ttu-id="5a865-272">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-272">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-273">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="5a865-273">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-274">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5a865-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-276">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="5a865-276">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="5a865-277">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-277">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-278">**移動**</span><span class="sxs-lookup"><span data-stu-id="5a865-278">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-279">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5a865-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-281">若 **為 TRUE**，就會卸載實體封裝 (如果它是設計成要在通常找到它的實體容器中取出，則不會因而影響整體封裝) 的功能。</span><span class="sxs-lookup"><span data-stu-id="5a865-281">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="5a865-282">如果電源必須是「關閉」以執行移除，則套件仍可以卸載。</span><span class="sxs-lookup"><span data-stu-id="5a865-282">A package can still be removable if the power must be "OFF" to perform the removal.</span></span> <span data-ttu-id="5a865-283">如果封裝可以在電源開啟時移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="5a865-283">If the package can be removed while the power is ON, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="5a865-284">例如，膝上型電腦中的額外電池會卸載，如同使用伺服器設定應用程式插入的磁片磁碟機套件 (SCA) 連接器。</span><span class="sxs-lookup"><span data-stu-id="5a865-284">For example, an extra battery in a laptop is removable, as is a disk drive package that is inserted using Server Configuration Application (SCA) connectors.</span></span> <span data-ttu-id="5a865-285">不過，後者可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="5a865-285">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="5a865-286">膝上型電腦顯示器不是可移動的，也不是 nonredundant 電源供應器。</span><span class="sxs-lookup"><span data-stu-id="5a865-286">A laptop display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="5a865-287">移除這些元件會影響整體封裝的功能，或因為封裝的緊密整合而無法運作。</span><span class="sxs-lookup"><span data-stu-id="5a865-287">Removing these components would affect the function of the overall packaging or is impossible because of the tight integration of the package.</span></span>

<span data-ttu-id="5a865-288">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-288">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-289">**更換**</span><span class="sxs-lookup"><span data-stu-id="5a865-289">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-290">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5a865-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-292">若 **為 TRUE**，則可將此實體媒體元件取代為實際不同的元件。</span><span class="sxs-lookup"><span data-stu-id="5a865-292">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="5a865-293">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="5a865-293">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="5a865-294">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="5a865-294">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="5a865-295">另一個範例是掛接在滑動滑軌上的電源供應器套件。</span><span class="sxs-lookup"><span data-stu-id="5a865-295">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="5a865-296">所有卸載式套件本質上都是可取代的。</span><span class="sxs-lookup"><span data-stu-id="5a865-296">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="5a865-297">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-297">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-298">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="5a865-298">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-299">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5a865-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-301">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 實體容器 Global Table \| 002.12 ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**BreachDescription**") </span><span class="sxs-lookup"><span data-stu-id="5a865-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-302">框架實體缺口的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a865-302">Status of a physical breach of the frame.</span></span>

<span data-ttu-id="5a865-303">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-303">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a865-304">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5a865-304">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a865-305">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5a865-305">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="5a865-306">**無缺口** (3) </span><span class="sxs-lookup"><span data-stu-id="5a865-306">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="5a865-307"> (4) **嘗試缺口**</span><span class="sxs-lookup"><span data-stu-id="5a865-307">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="5a865-308">**缺口成功** (5) </span><span class="sxs-lookup"><span data-stu-id="5a865-308">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a865-309">**SecurityStatus**</span><span class="sxs-lookup"><span data-stu-id="5a865-309">**SecurityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-310">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5a865-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-312">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 3 \| Security Status" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-312">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Security Status")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-313">外部輸入的安全性設定，例如鍵盤、電腦。</span><span class="sxs-lookup"><span data-stu-id="5a865-313">Security setting for external input, for example, a keyboard, to a computer.</span></span>

<span data-ttu-id="5a865-314">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **安全性狀態** 成員。</span><span class="sxs-lookup"><span data-stu-id="5a865-314">This value comes from the **Security Status** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a865-315">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5a865-315">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a865-316">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5a865-316">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5a865-317">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="5a865-317">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="5a865-318">**外部介面被鎖定** (4) </span><span class="sxs-lookup"><span data-stu-id="5a865-318">**External interface locked out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="5a865-319">**已啟用外部介面** (5) </span><span class="sxs-lookup"><span data-stu-id="5a865-319">**External interface enabled** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a865-320">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5a865-320">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-323">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5a865-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a865-324">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="5a865-324">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5a865-325">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **序號** 成員。</span><span class="sxs-lookup"><span data-stu-id="5a865-325">This value comes from the **Serial Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5a865-326">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-327">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5a865-327">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-328">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5a865-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a865-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-330">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServicePhilosophy**") </span><span class="sxs-lookup"><span data-stu-id="5a865-330">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-331">**ServicePhilosophy** 陣列中任何專案的更詳細說明的陣列。</span><span class="sxs-lookup"><span data-stu-id="5a865-331">Array of more detailed explanations for any of the entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="5a865-332">請注意，這個陣列的每個專案都與 **ServicePhilosophy** 中位於相同索引的專案相關。</span><span class="sxs-lookup"><span data-stu-id="5a865-332">Be aware that each entry of this array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="5a865-333">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-333">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-334">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="5a865-334">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-335">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5a865-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a865-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-337">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServiceDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="5a865-337">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-338">陣列，其中包含從頂端、前端、背面或側邊提供的框架、是否有滑動的紙匣或卸載式側邊，以及框架是否為可移動的（例如，有滾筒匣）。</span><span class="sxs-lookup"><span data-stu-id="5a865-338">Array that includes whether the frame is serviced from the top, front, back, or side, whether the frame has sliding trays or removable sides, and whether the frame is moveable—for example, having rollers.</span></span>

<span data-ttu-id="5a865-339">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-339">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a865-340">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5a865-340">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a865-341">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5a865-341">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="5a865-342">**從 Top** (2) 的服務</span><span class="sxs-lookup"><span data-stu-id="5a865-342">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="5a865-343">前 (3) **的服務**</span><span class="sxs-lookup"><span data-stu-id="5a865-343">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="5a865-344">**從背面** (4) 的服務</span><span class="sxs-lookup"><span data-stu-id="5a865-344">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="5a865-345">**服務從側** (5) </span><span class="sxs-lookup"><span data-stu-id="5a865-345">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="5a865-346">**滑動紙** 匣 (6) </span><span class="sxs-lookup"><span data-stu-id="5a865-346">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="5a865-347">**可移動側** (7) </span><span class="sxs-lookup"><span data-stu-id="5a865-347">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="5a865-348">**可移動** (8) </span><span class="sxs-lookup"><span data-stu-id="5a865-348">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a865-349">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5a865-349">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-352">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5a865-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a865-353">實體元素的庫存單位數。</span><span class="sxs-lookup"><span data-stu-id="5a865-353">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="5a865-354">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-355">**SMBIOSAssetTag**</span><span class="sxs-lookup"><span data-stu-id="5a865-355">**SMBIOSAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-356">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-358">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 3 \| 資產標記" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Asset Tag")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-359">系統主機殼的資產標記編號。</span><span class="sxs-lookup"><span data-stu-id="5a865-359">Asset tag number of the system enclosure.</span></span>

<span data-ttu-id="5a865-360">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **資產標記編號** 成員。</span><span class="sxs-lookup"><span data-stu-id="5a865-360">This value comes from the **Asset Tag Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="5a865-361">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5a865-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-362">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-364">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-364">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-365">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5a865-365">Current status of the object.</span></span> <span data-ttu-id="5a865-366">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="5a865-366">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5a865-367">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="5a865-367">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5a865-368">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="5a865-368">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5a865-369">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="5a865-369">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5a865-370">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="5a865-370">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5a865-371">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5a865-372">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="5a865-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5a865-373">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="5a865-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5a865-374">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5a865-375">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a865-376">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5a865-377">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5a865-378">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5a865-379">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5a865-380">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5a865-381">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5a865-382">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5a865-383">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5a865-384">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a865-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5a865-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-386">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-388">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Tag" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-388">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-389">系統主機殼的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a865-389">Unique identifier of the system enclosure.</span></span>

<span data-ttu-id="5a865-390">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-390">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="5a865-391">範例：「系統主機殼1」</span><span class="sxs-lookup"><span data-stu-id="5a865-391">Example: "System Enclosure 1"</span></span>

</dd> <dt>

<span data-ttu-id="5a865-392">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5a865-392">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-393">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5a865-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a865-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-395">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ 底座**](cim-chassis.md).**ChassisTypes**") </span><span class="sxs-lookup"><span data-stu-id="5a865-395">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-396">**ChassisTypes** 陣列專案的詳細資訊陣列。</span><span class="sxs-lookup"><span data-stu-id="5a865-396">Array of more information about the **ChassisTypes** array entries.</span></span> <span data-ttu-id="5a865-397">請注意，這個陣列的每個專案都與 **ChassisTypes** 中位於相同索引的專案相關。</span><span class="sxs-lookup"><span data-stu-id="5a865-397">Be aware that each entry of this array is related to the entry in **ChassisTypes** that is located at the same index.</span></span>

<span data-ttu-id="5a865-398">這個屬性繼承自 [**CIM \_ 底座**](cim-chassis.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-398">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-399">**版本**</span><span class="sxs-lookup"><span data-stu-id="5a865-399">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5a865-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-401">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-402">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5a865-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a865-403">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="5a865-403">Version of the physical element.</span></span>

<span data-ttu-id="5a865-404">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **版本** 成員。</span><span class="sxs-lookup"><span data-stu-id="5a865-404">This value comes from the **Version** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5a865-405">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-405">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-406">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="5a865-406">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-407">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5a865-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a865-409">若 **為 TRUE**，表示設備包含可見的警示。</span><span class="sxs-lookup"><span data-stu-id="5a865-409">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="5a865-410">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-410">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-411">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5a865-411">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-412">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="5a865-412">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-414">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="5a865-414">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-415">實體套件的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a865-415">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="5a865-416">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-416">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a865-417">**寬度**</span><span class="sxs-lookup"><span data-stu-id="5a865-417">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a865-418">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="5a865-418">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a865-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5a865-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a865-420">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="5a865-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5a865-421">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a865-421">Width of the physical package in inches.</span></span>

<span data-ttu-id="5a865-422">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-422">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a865-423">備註</span><span class="sxs-lookup"><span data-stu-id="5a865-423">Remarks</span></span>

<span data-ttu-id="5a865-424">**Win32 \_ SystemEnclosure** 類別衍生自 [**CIM \_ 底座**](cim-chassis.md)。</span><span class="sxs-lookup"><span data-stu-id="5a865-424">The **Win32\_SystemEnclosure** class is derived from [**CIM\_Chassis**](cim-chassis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5a865-425">範例</span><span class="sxs-lookup"><span data-stu-id="5a865-425">Examples</span></span>

<span data-ttu-id="5a865-426">在 TechNet 資源庫上 [以 powershell powershell 範例收集的多執行緒系統資產](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) ，會使用許多類別（包括 **Win32 \_ SystemEnclosure**）從系統取出資料。</span><span class="sxs-lookup"><span data-stu-id="5a865-426">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell example on TechNet gallery uses a number of classes, including **Win32\_SystemEnclosure**, to retrieve data from a system.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a865-427">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a865-427">Requirements</span></span>



| <span data-ttu-id="5a865-428">需求</span><span class="sxs-lookup"><span data-stu-id="5a865-428">Requirement</span></span> | <span data-ttu-id="5a865-429">值</span><span class="sxs-lookup"><span data-stu-id="5a865-429">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a865-430">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a865-430">Minimum supported client</span></span><br/> | <span data-ttu-id="5a865-431">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a865-431">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a865-432">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a865-432">Minimum supported server</span></span><br/> | <span data-ttu-id="5a865-433">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a865-433">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a865-434">命名空間</span><span class="sxs-lookup"><span data-stu-id="5a865-434">Namespace</span></span><br/>                | <span data-ttu-id="5a865-435">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5a865-435">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5a865-436">MOF</span><span class="sxs-lookup"><span data-stu-id="5a865-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a865-437"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a865-437"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a865-438">DLL</span><span class="sxs-lookup"><span data-stu-id="5a865-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a865-439"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a865-439"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a865-440">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a865-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a865-441">**CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="5a865-441">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="5a865-442">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="5a865-442">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5a865-443">WMI 工作：電腦硬體</span><span class="sxs-lookup"><span data-stu-id="5a865-443">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 

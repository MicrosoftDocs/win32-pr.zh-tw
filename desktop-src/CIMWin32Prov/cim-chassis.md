---
description: CIM \_ 底座類別代表包含其他元素的實體元素，並提供可定義的功能，例如桌面、處理節點、UPS、磁片或磁帶存放裝置，或這些專案的組合。
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: CIM_Chassis 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111000"
---
# <a name="cim_chassis-class"></a><span data-ttu-id="0c280-103">CIM \_ 底座類別</span><span class="sxs-lookup"><span data-stu-id="0c280-103">CIM\_Chassis class</span></span>

<span data-ttu-id="0c280-104">**CIM \_ 底座** 類別代表包含其他元素的實體元素，並提供可定義的功能，例如桌面、處理節點、UPS、磁片或磁帶存放裝置，或這些專案的組合。</span><span class="sxs-lookup"><span data-stu-id="0c280-104">The **CIM\_Chassis** class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c280-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0c280-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0c280-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0c280-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0c280-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0c280-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0c280-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0c280-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c280-109">語法</span><span class="sxs-lookup"><span data-stu-id="0c280-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="0c280-110">成員</span><span class="sxs-lookup"><span data-stu-id="0c280-110">Members</span></span>

<span data-ttu-id="0c280-111">**CIM \_ 底座** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0c280-111">The **CIM\_Chassis** class has these types of members:</span></span>

-   [<span data-ttu-id="0c280-112">方法</span><span class="sxs-lookup"><span data-stu-id="0c280-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c280-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0c280-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c280-114">方法</span><span class="sxs-lookup"><span data-stu-id="0c280-114">Methods</span></span>

<span data-ttu-id="0c280-115">**CIM \_ 底座** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0c280-115">The **CIM\_Chassis** class has these methods.</span></span>



| <span data-ttu-id="0c280-116">方法</span><span class="sxs-lookup"><span data-stu-id="0c280-116">Method</span></span>                                                           | <span data-ttu-id="0c280-117">描述</span><span class="sxs-lookup"><span data-stu-id="0c280-117">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c280-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="0c280-118">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-chassis.md) | <span data-ttu-id="0c280-119">確認參考的實體元素是否可包含或插入實體封裝中。</span><span class="sxs-lookup"><span data-stu-id="0c280-119">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="0c280-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0c280-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0c280-121">屬性</span><span class="sxs-lookup"><span data-stu-id="0c280-121">Properties</span></span>

<span data-ttu-id="0c280-122">**CIM \_ 底座** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0c280-122">The **CIM\_Chassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c280-123">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="0c280-123">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-124">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c280-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-126">若 **為 TRUE**，則框架具有可聽見的警示。</span><span class="sxs-lookup"><span data-stu-id="0c280-126">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="0c280-127">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-127">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="0c280-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**") </span><span class="sxs-lookup"><span data-stu-id="0c280-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-132">提供詳細資訊的自由格式字串，如果 **SecurityBreach** 屬性指出發生缺口或某些其他安全性相關事件，則會提供更多資訊。</span><span class="sxs-lookup"><span data-stu-id="0c280-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="0c280-133">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-133">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-134">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="0c280-134">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-137">自由格式的字串，其中包含有關如何連接及配套框架的各種纜線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0c280-137">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="0c280-138">使用許多網路、儲存體相關和電源線，纜線管理可能是複雜且富有挑戰性的工作。</span><span class="sxs-lookup"><span data-stu-id="0c280-138">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="0c280-139">此字串屬性包含的資訊可協助框架的元件和服務。</span><span class="sxs-lookup"><span data-stu-id="0c280-139">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="0c280-140">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-140">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-141">**標題**</span><span class="sxs-lookup"><span data-stu-id="0c280-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-144">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-145">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0c280-145">A short textual description of the object.</span></span>

<span data-ttu-id="0c280-146">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-147">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="0c280-147">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0c280-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c280-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-150">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 實體容器 Global Table \| 002.1 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 底座**。**TypeDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="0c280-150">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-151">列舉的整數值陣列，指出底座的類型。</span><span class="sxs-lookup"><span data-stu-id="0c280-151">Enumerated, integer-valued array that indicates the type of chassis.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c280-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0c280-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-153">其他。</span><span class="sxs-lookup"><span data-stu-id="0c280-153">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c280-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0c280-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-155">不明。</span><span class="sxs-lookup"><span data-stu-id="0c280-155">Unknown.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="0c280-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**桌面** (3) </span><span class="sxs-lookup"><span data-stu-id="0c280-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-157">桌上型電腦。</span><span class="sxs-lookup"><span data-stu-id="0c280-157">Desktop.</span></span>

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="0c280-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**低設定檔桌面** (4) </span><span class="sxs-lookup"><span data-stu-id="0c280-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Low Profile Desktop** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-159">低設定檔桌面。</span><span class="sxs-lookup"><span data-stu-id="0c280-159">Low-profile desktop.</span></span>

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="0c280-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**比薩 Box** (5) </span><span class="sxs-lookup"><span data-stu-id="0c280-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-161">比薩方塊。</span><span class="sxs-lookup"><span data-stu-id="0c280-161">Pizza box.</span></span>

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="0c280-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**迷你塔式** (6) </span><span class="sxs-lookup"><span data-stu-id="0c280-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Tower** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-163">迷你塔式。</span><span class="sxs-lookup"><span data-stu-id="0c280-163">Mini tower.</span></span>

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="0c280-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**塔** (7) </span><span class="sxs-lookup"><span data-stu-id="0c280-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-165">[立式]：</span><span class="sxs-lookup"><span data-stu-id="0c280-165">Tower.</span></span>

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="0c280-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**便攜** (8) </span><span class="sxs-lookup"><span data-stu-id="0c280-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-167">可擕式。</span><span class="sxs-lookup"><span data-stu-id="0c280-167">Portable.</span></span>

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="0c280-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**膝上型電腦** (9) </span><span class="sxs-lookup"><span data-stu-id="0c280-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-169">[膝上型電腦]：</span><span class="sxs-lookup"><span data-stu-id="0c280-169">Laptop.</span></span>

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="0c280-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**筆記本** (10) </span><span class="sxs-lookup"><span data-stu-id="0c280-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-171">筆記本。</span><span class="sxs-lookup"><span data-stu-id="0c280-171">Notebook.</span></span>

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="0c280-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**保留** (11) </span><span class="sxs-lookup"><span data-stu-id="0c280-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-173">掌上型。</span><span class="sxs-lookup"><span data-stu-id="0c280-173">Hand-held.</span></span>

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="0c280-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**銜接站** (12) </span><span class="sxs-lookup"><span data-stu-id="0c280-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-175">銜接站。</span><span class="sxs-lookup"><span data-stu-id="0c280-175">Docking station.</span></span>

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="0c280-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**全都在一個** (13) </span><span class="sxs-lookup"><span data-stu-id="0c280-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**All in One** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-177">全部-一。</span><span class="sxs-lookup"><span data-stu-id="0c280-177">All-in-one.</span></span>

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="0c280-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**子筆記本** (14) </span><span class="sxs-lookup"><span data-stu-id="0c280-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-179">Subnotebook.</span><span class="sxs-lookup"><span data-stu-id="0c280-179">Subnotebook.</span></span>

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="0c280-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**節省空間** (15) </span><span class="sxs-lookup"><span data-stu-id="0c280-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Space-Saving** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-181">節省空間。</span><span class="sxs-lookup"><span data-stu-id="0c280-181">Space-saving.</span></span>

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="0c280-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span> (16) **午餐箱**</span><span class="sxs-lookup"><span data-stu-id="0c280-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-183">飯盒。</span><span class="sxs-lookup"><span data-stu-id="0c280-183">Lunch box.</span></span>

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="0c280-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**主要系統底座** (17) </span><span class="sxs-lookup"><span data-stu-id="0c280-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Main System Chassis** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-185">主要系統底座。</span><span class="sxs-lookup"><span data-stu-id="0c280-185">Main system chassis.</span></span>

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="0c280-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**擴充底座** (18) </span><span class="sxs-lookup"><span data-stu-id="0c280-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Expansion Chassis** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-187">擴充底座。</span><span class="sxs-lookup"><span data-stu-id="0c280-187">Expansion chassis.</span></span>

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="0c280-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19) </span><span class="sxs-lookup"><span data-stu-id="0c280-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-189">Subchassis.</span><span class="sxs-lookup"><span data-stu-id="0c280-189">Subchassis.</span></span>

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="0c280-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**匯流排擴充底座** (20) </span><span class="sxs-lookup"><span data-stu-id="0c280-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Bus Expansion Chassis** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-191">匯流排-擴充底座。</span><span class="sxs-lookup"><span data-stu-id="0c280-191">Bus-expansion chassis.</span></span>

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="0c280-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**週邊底座** (21) </span><span class="sxs-lookup"><span data-stu-id="0c280-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripheral Chassis** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-193">週邊底座。</span><span class="sxs-lookup"><span data-stu-id="0c280-193">Peripheral chassis.</span></span>

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="0c280-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**儲存體底座** (22) </span><span class="sxs-lookup"><span data-stu-id="0c280-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage Chassis** (22)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-195">儲存體底座。</span><span class="sxs-lookup"><span data-stu-id="0c280-195">Storage chassis.</span></span>

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="0c280-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**機架掛接底座** (23) </span><span class="sxs-lookup"><span data-stu-id="0c280-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-197">機架掛接底座。</span><span class="sxs-lookup"><span data-stu-id="0c280-197">Rack-mount chassis.</span></span>

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="0c280-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-CASE PC** (24) </span><span class="sxs-lookup"><span data-stu-id="0c280-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case PC** (24)</span></span>


</dt> <dd>

<span data-ttu-id="0c280-199">密封的案例電腦。</span><span class="sxs-lookup"><span data-stu-id="0c280-199">Sealed-case computer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c280-200">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c280-200">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-203">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="0c280-203">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-204">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c280-204">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0c280-205">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="0c280-205">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0c280-206">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-207">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="0c280-207">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-208">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="0c280-208">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-210">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "安培 at 120 伏特" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-211">目前，底座的120伏要求。</span><span class="sxs-lookup"><span data-stu-id="0c280-211">Currently required by the chassis at 120 volts.</span></span> <span data-ttu-id="0c280-212">如果電源是由底座提供 (就像在 UPS) 的情況下，此屬性可能會指出產生的 amperage 為負數。</span><span class="sxs-lookup"><span data-stu-id="0c280-212">If power is provided by the chassis (as in the case of a UPS), this property can indicate the amperage produced, as a negative number.</span></span>

</dd> <dt>

<span data-ttu-id="0c280-213">**深度**</span><span class="sxs-lookup"><span data-stu-id="0c280-213">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-214">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="0c280-214">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-216">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-216">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-217">實體套件的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="0c280-217">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="0c280-218">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-218">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-219">**說明**</span><span class="sxs-lookup"><span data-stu-id="0c280-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-222">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-223">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0c280-223">A textual description of the object.</span></span>

<span data-ttu-id="0c280-224">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-225">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="0c280-225">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-226">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0c280-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-228">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每小時 BTU」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-228">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-229">底座在 Btu/小時內產生的熱度數量。</span><span class="sxs-lookup"><span data-stu-id="0c280-229">Amount of heat generated by the chassis in Btu/hour.</span></span>

</dd> <dt>

<span data-ttu-id="0c280-230">**高度**</span><span class="sxs-lookup"><span data-stu-id="0c280-230">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-231">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="0c280-231">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-233">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-233">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-234">實體封裝的高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="0c280-234">Height of the physical package, in inches.</span></span>

<span data-ttu-id="0c280-235">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-235">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-236">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="0c280-236">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-237">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c280-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-239">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="0c280-239">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="0c280-240">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="0c280-240">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="0c280-241">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="0c280-241">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="0c280-242">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="0c280-242">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="0c280-243">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-243">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-244">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0c280-244">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-245">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0c280-245">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-247">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0c280-247">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-248">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="0c280-248">Indicates when the object was installed.</span></span> <span data-ttu-id="0c280-249">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0c280-249">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0c280-250">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-250">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-251">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="0c280-251">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-252">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c280-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-254">若 **為 TRUE**，則會使用鎖定來保護框架。</span><span class="sxs-lookup"><span data-stu-id="0c280-254">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="0c280-255">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-255">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-256">**製造商**</span><span class="sxs-lookup"><span data-stu-id="0c280-256">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-259">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="0c280-259">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-260">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="0c280-260">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="0c280-261">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0c280-261">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="0c280-262">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-263">**型號**</span><span class="sxs-lookup"><span data-stu-id="0c280-263">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-266">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0c280-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-267">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c280-267">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="0c280-268">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-269">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0c280-269">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-272">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-272">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-273">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0c280-273">Label by which the object is known.</span></span> <span data-ttu-id="0c280-274">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="0c280-274">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0c280-275">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-276">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="0c280-276">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-277">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0c280-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-279">必須連接到底座才能操作所有元件的電源線數目。</span><span class="sxs-lookup"><span data-stu-id="0c280-279">Number of power cords that must be connected to the chassis so that all of the components can operate.</span></span>

</dd> <dt>

<span data-ttu-id="0c280-280">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0c280-280">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-283">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="0c280-283">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="0c280-284">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="0c280-284">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="0c280-285">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="0c280-285">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="0c280-286">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-287">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="0c280-287">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-290">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="0c280-290">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-291">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="0c280-291">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="0c280-292">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-293">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="0c280-293">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-294">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c280-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-296">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="0c280-296">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="0c280-297">否則，它目前為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="0c280-297">Otherwise, it is currently off.</span></span>

<span data-ttu-id="0c280-298">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-299">**移動**</span><span class="sxs-lookup"><span data-stu-id="0c280-299">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-300">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c280-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-302">若 **為 TRUE**，則會將封裝設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="0c280-302">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="0c280-303">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="0c280-303">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="0c280-304">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="0c280-304">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="0c280-305">例如，「可升級處理器」晶片是卸載式的。</span><span class="sxs-lookup"><span data-stu-id="0c280-305">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="0c280-306">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-306">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-307">**更換**</span><span class="sxs-lookup"><span data-stu-id="0c280-307">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-308">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c280-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-310">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="0c280-310">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="0c280-311">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="0c280-311">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="0c280-312">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="0c280-312">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="0c280-313">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="0c280-313">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="0c280-314">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-314">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-315">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="0c280-315">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-316">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0c280-316">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-318">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體容器 Global Table \| 002.12 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**BreachDescription**") </span><span class="sxs-lookup"><span data-stu-id="0c280-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-319">指出是否嘗試執行框架的實體缺口，但不成功或嘗試成功。</span><span class="sxs-lookup"><span data-stu-id="0c280-319">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<span data-ttu-id="0c280-320">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-320">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c280-321">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0c280-321">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c280-322">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0c280-322">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="0c280-323">**無缺口** (3) </span><span class="sxs-lookup"><span data-stu-id="0c280-323">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="0c280-324"> (4) **嘗試缺口**</span><span class="sxs-lookup"><span data-stu-id="0c280-324">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="0c280-325">**缺口成功** (5) </span><span class="sxs-lookup"><span data-stu-id="0c280-325">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c280-326">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0c280-326">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-327">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-329">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0c280-329">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-330">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="0c280-330">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="0c280-331">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-331">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-332">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0c280-332">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-333">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0c280-333">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c280-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-335">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServicePhilosophy**") </span><span class="sxs-lookup"><span data-stu-id="0c280-335">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-336">提供 **ServicePhilosophy** 陣列中專案詳細說明的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="0c280-336">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="0c280-337">這個陣列的每個專案都與 **ServicePhilosophy** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="0c280-337">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

<span data-ttu-id="0c280-338">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-338">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-339">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="0c280-339">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-340">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0c280-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c280-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-342">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServiceDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="0c280-342">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-343">指出框架是否從頂端、前端、背面或側邊提供服務;以及是否有滑動的紙匣或卸載式邊，以及是否有可移動的框架 (例如，有滾筒) 。</span><span class="sxs-lookup"><span data-stu-id="0c280-343">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="0c280-344">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-344">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c280-345">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0c280-345">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c280-346">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0c280-346">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="0c280-347">**從 Top** (2) 的服務</span><span class="sxs-lookup"><span data-stu-id="0c280-347">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="0c280-348">前 (3) **的服務**</span><span class="sxs-lookup"><span data-stu-id="0c280-348">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="0c280-349">**從背面** (4) 的服務</span><span class="sxs-lookup"><span data-stu-id="0c280-349">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="0c280-350">**服務從側** (5) </span><span class="sxs-lookup"><span data-stu-id="0c280-350">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="0c280-351">**滑動紙** 匣 (6) </span><span class="sxs-lookup"><span data-stu-id="0c280-351">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="0c280-352">**可移動側** (7) </span><span class="sxs-lookup"><span data-stu-id="0c280-352">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="0c280-353">**可移動** (8) </span><span class="sxs-lookup"><span data-stu-id="0c280-353">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c280-354">**SKU**</span><span class="sxs-lookup"><span data-stu-id="0c280-354">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-357">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0c280-357">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-358">此實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="0c280-358">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="0c280-359">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-359">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-360">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0c280-360">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-363">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-363">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-364">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0c280-364">String that indicates the current status of the object.</span></span> <span data-ttu-id="0c280-365">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="0c280-365">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0c280-366">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="0c280-366">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0c280-367">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="0c280-367">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0c280-368">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0c280-368">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0c280-369">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="0c280-369">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0c280-370">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0c280-370">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0c280-371">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0c280-372">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0c280-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0c280-373">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0c280-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0c280-374">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0c280-375">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c280-376">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0c280-377">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0c280-378">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0c280-379">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0c280-380">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0c280-381">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0c280-382">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0c280-383">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0c280-384">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c280-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="0c280-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-386">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-388">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="0c280-388">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-389">可唯一識別實體元素，並作為專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0c280-389">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="0c280-390">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="0c280-390">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="0c280-391">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="0c280-391">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="0c280-392">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="0c280-392">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="0c280-393">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="0c280-393">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="0c280-394">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="0c280-394">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="0c280-395">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-395">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-396">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0c280-396">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-397">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0c280-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c280-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-399">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ 底座**.**ChassisTypes**") </span><span class="sxs-lookup"><span data-stu-id="0c280-399">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-400">提供 **ChassisTypes** 陣列專案相關資訊之自由格式字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="0c280-400">Array of free-form strings that provides information about the **ChassisTypes** array entries.</span></span>

> [!Note]  
> <span data-ttu-id="0c280-401">每個陣列專案都與 **ChassisTypes** 屬性中的專案相關，該專案位於相同的索引處。</span><span class="sxs-lookup"><span data-stu-id="0c280-401">Each array entry is related to the entry in the **ChassisTypes** property, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="0c280-402">**版本**</span><span class="sxs-lookup"><span data-stu-id="0c280-402">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c280-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-405">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0c280-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0c280-406">指出實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="0c280-406">Indicates the version of the physical element.</span></span>

<span data-ttu-id="0c280-407">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-407">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-408">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="0c280-408">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-409">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0c280-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c280-411">若 **為 TRUE**，表示設備包含可見的警示。</span><span class="sxs-lookup"><span data-stu-id="0c280-411">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="0c280-412">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-412">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-413">**Weight**</span><span class="sxs-lookup"><span data-stu-id="0c280-413">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-414">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="0c280-414">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-416">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="0c280-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-417">實體封裝的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="0c280-417">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="0c280-418">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-418">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c280-419">**寬度**</span><span class="sxs-lookup"><span data-stu-id="0c280-419">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c280-420">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="0c280-420">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0c280-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c280-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c280-422">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="0c280-422">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0c280-423">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="0c280-423">Width of the physical package, in inches.</span></span>

<span data-ttu-id="0c280-424">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-424">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c280-425">備註</span><span class="sxs-lookup"><span data-stu-id="0c280-425">Remarks</span></span>

<span data-ttu-id="0c280-426">**Cim \_ 底座** 類別衍生自 [**cim \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-426">The **CIM\_Chassis** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="0c280-427">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0c280-427">WMI does not implement this class.</span></span> <span data-ttu-id="0c280-428">如需衍生自 **CIM \_ 底座** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="0c280-428">For more information about classes derived from **CIM\_Chassis**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0c280-429">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0c280-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0c280-430">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0c280-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c280-431">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c280-431">Requirements</span></span>



| <span data-ttu-id="0c280-432">需求</span><span class="sxs-lookup"><span data-stu-id="0c280-432">Requirement</span></span> | <span data-ttu-id="0c280-433">值</span><span class="sxs-lookup"><span data-stu-id="0c280-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c280-434">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c280-434">Minimum supported client</span></span><br/> | <span data-ttu-id="0c280-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c280-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c280-436">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c280-436">Minimum supported server</span></span><br/> | <span data-ttu-id="0c280-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c280-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c280-438">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c280-438">Namespace</span></span><br/>                | <span data-ttu-id="0c280-439">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0c280-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c280-440">MOF</span><span class="sxs-lookup"><span data-stu-id="0c280-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c280-441"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c280-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c280-442">DLL</span><span class="sxs-lookup"><span data-stu-id="0c280-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c280-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c280-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c280-444">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c280-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c280-445">**CIM \_ PhysicalFrame**</span><span class="sxs-lookup"><span data-stu-id="0c280-445">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 


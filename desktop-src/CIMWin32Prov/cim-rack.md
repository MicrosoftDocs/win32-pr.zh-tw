---
description: CIM \_ 機架類別代表機架 (實體框架或主機殼) 在其中儲存底座。 通常，機架代表主機殼;所有運作中的元件都會封裝在底座中。
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: CIM_Rack 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688795"
---
# <a name="cim_rack-class"></a><span data-ttu-id="e2f11-104">CIM \_ 機架類別</span><span class="sxs-lookup"><span data-stu-id="e2f11-104">CIM\_Rack class</span></span>

<span data-ttu-id="e2f11-105">**CIM \_ 機架** 類別代表機架 (實體框架或主機殼) 在其中儲存底座。</span><span class="sxs-lookup"><span data-stu-id="e2f11-105">The **CIM\_Rack** class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="e2f11-106">通常，機架代表主機殼;所有運作中的元件都會封裝在底座中。</span><span class="sxs-lookup"><span data-stu-id="e2f11-106">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2f11-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e2f11-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2f11-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e2f11-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f11-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e2f11-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e2f11-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f11-111">語法</span><span class="sxs-lookup"><span data-stu-id="e2f11-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="e2f11-112">成員</span><span class="sxs-lookup"><span data-stu-id="e2f11-112">Members</span></span>

<span data-ttu-id="e2f11-113">**CIM \_ 機架** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e2f11-113">The **CIM\_Rack** class has these types of members:</span></span>

-   [<span data-ttu-id="e2f11-114">方法</span><span class="sxs-lookup"><span data-stu-id="e2f11-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2f11-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e2f11-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2f11-116">方法</span><span class="sxs-lookup"><span data-stu-id="e2f11-116">Methods</span></span>

<span data-ttu-id="e2f11-117">**CIM \_ 機架** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e2f11-117">The **CIM\_Rack** class has these methods.</span></span>



| <span data-ttu-id="e2f11-118">方法</span><span class="sxs-lookup"><span data-stu-id="e2f11-118">Method</span></span>                                                        | <span data-ttu-id="e2f11-119">描述</span><span class="sxs-lookup"><span data-stu-id="e2f11-119">Description</span></span>                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2f11-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="e2f11-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-rack.md) | <span data-ttu-id="e2f11-121">確認參考的實體元素是否可包含或插入實體封裝中。</span><span class="sxs-lookup"><span data-stu-id="e2f11-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="e2f11-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e2f11-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e2f11-123">屬性</span><span class="sxs-lookup"><span data-stu-id="e2f11-123">Properties</span></span>

<span data-ttu-id="e2f11-124">**CIM \_ 機架** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f11-124">The **CIM\_Rack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2f11-125">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="e2f11-125">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f11-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-128">若 **為 TRUE**，則框架具有可聽見的警示。</span><span class="sxs-lookup"><span data-stu-id="e2f11-128">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="e2f11-129">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-129">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-130">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="e2f11-130">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-133">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**") </span><span class="sxs-lookup"><span data-stu-id="e2f11-133">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-134">提供資訊的自由格式字串，如果 **SecurityBreach** 屬性指出發生缺口或某些其他安全性相關事件，則會提供資訊。</span><span class="sxs-lookup"><span data-stu-id="e2f11-134">Free-form string that provides information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="e2f11-135">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-135">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-136">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="e2f11-136">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-139">自由格式的字串，其中包含有關如何連接及配套框架的各種纜線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e2f11-139">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="e2f11-140">使用許多網路、儲存體相關和電源線，纜線管理可能是複雜且富有挑戰性的工作。</span><span class="sxs-lookup"><span data-stu-id="e2f11-140">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="e2f11-141">此字串屬性包含的資訊可協助框架的元件和服務。</span><span class="sxs-lookup"><span data-stu-id="e2f11-141">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="e2f11-142">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-142">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-143">**標題**</span><span class="sxs-lookup"><span data-stu-id="e2f11-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-146">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-147">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e2f11-147">Short textual description of the object.</span></span>

<span data-ttu-id="e2f11-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-149">**CountryDesignation**</span><span class="sxs-lookup"><span data-stu-id="e2f11-149">**CountryDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-152">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 機架**」。**TypeOfRack**") </span><span class="sxs-lookup"><span data-stu-id="e2f11-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**TypeOfRack**")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-153">設計機架的國家或地區。</span><span class="sxs-lookup"><span data-stu-id="e2f11-153">Country or region for which the rack is designed.</span></span> <span data-ttu-id="e2f11-154">國家或地區程式碼字串是由 ISO/IEC 3166 所定義。</span><span class="sxs-lookup"><span data-stu-id="e2f11-154">Country or region code strings are as defined by ISO/IEC 3166.</span></span> <span data-ttu-id="e2f11-155">機架類型是在 **TypeOfRack** 屬性中指定的。</span><span class="sxs-lookup"><span data-stu-id="e2f11-155">The rack type is specified in the **TypeOfRack** property.</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2f11-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-159">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e2f11-159">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-160">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2f11-160">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e2f11-161">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="e2f11-161">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e2f11-162">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-162">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-163">**深度**</span><span class="sxs-lookup"><span data-stu-id="e2f11-163">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-164">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e2f11-164">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-166">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-166">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-167">實體套件的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f11-167">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="e2f11-168">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-169">**說明**</span><span class="sxs-lookup"><span data-stu-id="e2f11-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-172">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-172">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-173">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e2f11-173">Textual description of the object.</span></span>

<span data-ttu-id="e2f11-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-175">**高度**</span><span class="sxs-lookup"><span data-stu-id="e2f11-175">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-176">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e2f11-176">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-178">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Height" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Us" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-178">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-179">實體封裝的高度，使用「U」測量單位。</span><span class="sxs-lookup"><span data-stu-id="e2f11-179">Height of the physical package, using the "U" unit of measure.</span></span> <span data-ttu-id="e2f11-180">「U」是一種標準測量單位，適用于機架的高度或可供機架使用的元件，並等於1.75 英寸或4.445 釐米。</span><span class="sxs-lookup"><span data-stu-id="e2f11-180">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

<span data-ttu-id="e2f11-181">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-181">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-182">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="e2f11-182">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-183">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f11-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-185">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="e2f11-185">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="e2f11-186">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="e2f11-186">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="e2f11-187">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="e2f11-187">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="e2f11-188">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="e2f11-188">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="e2f11-189">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-189">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-190">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2f11-190">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-191">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e2f11-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-193">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e2f11-193">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-194">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e2f11-194">Date and time the object was installed.</span></span> <span data-ttu-id="e2f11-195">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e2f11-195">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e2f11-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-197">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="e2f11-197">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-198">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f11-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-200">若 **為 TRUE**，則會使用鎖定來保護框架。</span><span class="sxs-lookup"><span data-stu-id="e2f11-200">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="e2f11-201">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-201">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-202">**製造商**</span><span class="sxs-lookup"><span data-stu-id="e2f11-202">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-205">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e2f11-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-206">產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="e2f11-206">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="e2f11-207">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f11-207">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="e2f11-208">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-208">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-209">**型號**</span><span class="sxs-lookup"><span data-stu-id="e2f11-209">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-212">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e2f11-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-213">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2f11-213">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="e2f11-214">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-214">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-215">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e2f11-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-218">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-218">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-219">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e2f11-219">Label by which the object is known.</span></span> <span data-ttu-id="e2f11-220">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f11-220">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e2f11-221">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-222">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e2f11-222">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-225">其他資料，除了資產標記資訊之外，還可以用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="e2f11-225">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="e2f11-226">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="e2f11-226">One example is bar-code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="e2f11-227">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="e2f11-228">如果只有條碼資料可供使用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="e2f11-228">If only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="e2f11-229">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="e2f11-229">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-232">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e2f11-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-233">由產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="e2f11-233">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="e2f11-234">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-234">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-235">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="e2f11-235">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-236">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f11-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-238">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="e2f11-238">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="e2f11-239">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-240">**移動**</span><span class="sxs-lookup"><span data-stu-id="e2f11-240">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-241">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f11-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-243">若 **為 TRUE**，則會將這個專案設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="e2f11-243">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="e2f11-244">即使電源必須是「關閉」才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="e2f11-244">A package is considered removable even if the power must be "off" to perform the removal.</span></span> <span data-ttu-id="e2f11-245">如果電源可以是 "on" 且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="e2f11-245">If the power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="e2f11-246">例如，膝上型電腦中的額外電池會卸載，也就是使用 SCA 連接器插入的磁片磁碟機套件;不過，後者可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="e2f11-246">For example, an extra battery in a laptop is removable, as is a disk-drive package inserted using SCA connectors; however, the latter can be hot-swapped.</span></span> <span data-ttu-id="e2f11-247">膝上型電腦的顯示器不是可移動的，也不是不重複的電源供應器。</span><span class="sxs-lookup"><span data-stu-id="e2f11-247">A laptop's display is not removable, nor is a non-redundant power supply.</span></span> <span data-ttu-id="e2f11-248">移除這些元件會影響整體封裝的功能，或由於封裝的緊密整合而無法進行。</span><span class="sxs-lookup"><span data-stu-id="e2f11-248">Removing these components impacts the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="e2f11-249">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-249">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-250">**更換**</span><span class="sxs-lookup"><span data-stu-id="e2f11-250">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-251">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f11-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-253">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="e2f11-253">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="e2f11-254">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="e2f11-254">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="e2f11-255">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="e2f11-255">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="e2f11-256">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="e2f11-256">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="e2f11-257">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-257">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-258">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="e2f11-258">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-259">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f11-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-261">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體容器 Global Table \| 002.12 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**BreachDescription**") </span><span class="sxs-lookup"><span data-stu-id="e2f11-261">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-262">指出是否嘗試執行框架的實體缺口，但不成功或嘗試成功。</span><span class="sxs-lookup"><span data-stu-id="e2f11-262">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span> <span data-ttu-id="e2f11-263">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-263">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e2f11-264">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f11-264">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f11-265">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e2f11-265">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="e2f11-266">**無缺口** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f11-266">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="e2f11-267"> (4) **嘗試缺口**</span><span class="sxs-lookup"><span data-stu-id="e2f11-267">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="e2f11-268">**缺口成功** (5) </span><span class="sxs-lookup"><span data-stu-id="e2f11-268">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f11-269">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e2f11-269">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-272">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e2f11-272">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-273">用來識別機架的製造商配置數位。</span><span class="sxs-lookup"><span data-stu-id="e2f11-273">Manufacturer-allocated number used to identify the rack.</span></span>

<span data-ttu-id="e2f11-274">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-274">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-275">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e2f11-275">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-276">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e2f11-276">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-278">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServicePhilosophy**") </span><span class="sxs-lookup"><span data-stu-id="e2f11-278">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-279">提供 **ServicePhilosophy** 陣列中專案詳細說明的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="e2f11-279">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="e2f11-280">請注意，陣列的每個專案都與 **ServicePhilosophy** 中位於相同索引的專案相關。</span><span class="sxs-lookup"><span data-stu-id="e2f11-280">Note, each entry of the array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="e2f11-281">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-281">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-282">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="e2f11-282">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-283">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e2f11-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-285">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServiceDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="e2f11-285">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-286">指出框架是否從頂端、前端、背面或側邊提供服務;以及是否有滑動的紙匣或卸載式邊，以及是否有可移動的框架 (例如，有滾筒) 。</span><span class="sxs-lookup"><span data-stu-id="e2f11-286">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="e2f11-287">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-287">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f11-288">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e2f11-288">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e2f11-289">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f11-289">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="e2f11-290">**從 Top** (2) 的服務</span><span class="sxs-lookup"><span data-stu-id="e2f11-290">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="e2f11-291">前 (3) **的服務**</span><span class="sxs-lookup"><span data-stu-id="e2f11-291">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="e2f11-292">**從背面** (4) 的服務</span><span class="sxs-lookup"><span data-stu-id="e2f11-292">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="e2f11-293">**服務從側** (5) </span><span class="sxs-lookup"><span data-stu-id="e2f11-293">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="e2f11-294">**滑動紙** 匣 (6) </span><span class="sxs-lookup"><span data-stu-id="e2f11-294">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="e2f11-295">**可移動側** (7) </span><span class="sxs-lookup"><span data-stu-id="e2f11-295">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="e2f11-296">**可移動** (8) </span><span class="sxs-lookup"><span data-stu-id="e2f11-296">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f11-297">**SKU**</span><span class="sxs-lookup"><span data-stu-id="e2f11-297">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-300">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e2f11-300">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-301">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="e2f11-301">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="e2f11-302">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-303">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e2f11-303">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-306">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-307">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f11-307">Current status of the object.</span></span> <span data-ttu-id="e2f11-308">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e2f11-309">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="e2f11-309">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e2f11-310">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-310">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e2f11-311">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-311">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2f11-312">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-312">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f11-313">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-313">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e2f11-314">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-314">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e2f11-315">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-315">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e2f11-316">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-316">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e2f11-317">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-317">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e2f11-318">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-318">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e2f11-319">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-319">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e2f11-320">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-320">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e2f11-321">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-321">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f11-322">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e2f11-322">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-325">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e2f11-325">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-326">可唯一識別實體元素並作為專案索引鍵的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="e2f11-326">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="e2f11-327">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="e2f11-327">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="e2f11-328">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="e2f11-328">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="e2f11-329">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="e2f11-329">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="e2f11-330">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="e2f11-330">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="e2f11-331">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="e2f11-331">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="e2f11-332">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-332">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-333">**TypeOfRack**</span><span class="sxs-lookup"><span data-stu-id="e2f11-333">**TypeOfRack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-334">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f11-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-336">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 機架**」。**CountryDesignation**") </span><span class="sxs-lookup"><span data-stu-id="e2f11-336">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**CountryDesignation**")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-337">機架的類型。</span><span class="sxs-lookup"><span data-stu-id="e2f11-337">Type of rack.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f11-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e2f11-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span data-ttu-id="e2f11-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**標準19英寸** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f11-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Inch** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e2f11-340">標準 19-英寸</span><span class="sxs-lookup"><span data-stu-id="e2f11-340">Standard 19-inch</span></span>

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span data-ttu-id="e2f11-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**電信** (2) </span><span class="sxs-lookup"><span data-stu-id="e2f11-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span data-ttu-id="e2f11-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**設備貨架** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f11-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Equipment Shelf** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span data-ttu-id="e2f11-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**非標準** (4) </span><span class="sxs-lookup"><span data-stu-id="e2f11-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non-Standard** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f11-344">**版本**</span><span class="sxs-lookup"><span data-stu-id="e2f11-344">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f11-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-347">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e2f11-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-348">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="e2f11-348">Version of the physical element.</span></span>

<span data-ttu-id="e2f11-349">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-349">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-350">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="e2f11-350">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-351">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f11-351">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-353">若 **為 TRUE**，表示設備包含可見的警示。</span><span class="sxs-lookup"><span data-stu-id="e2f11-353">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="e2f11-354">這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-354">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-355">**Weight**</span><span class="sxs-lookup"><span data-stu-id="e2f11-355">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-356">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e2f11-356">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-358">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-358">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-359">實體封裝的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f11-359">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="e2f11-360">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-360">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f11-361">**寬度**</span><span class="sxs-lookup"><span data-stu-id="e2f11-361">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f11-362">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e2f11-362">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f11-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f11-364">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="e2f11-364">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="e2f11-365">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f11-365">Width of the physical package, in inches.</span></span>

<span data-ttu-id="e2f11-366">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-366">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2f11-367">備註</span><span class="sxs-lookup"><span data-stu-id="e2f11-367">Remarks</span></span>

<span data-ttu-id="e2f11-368">**Cim \_ 機架** 類別衍生自 [**cim \_ PhysicalFrame**](cim-physicalframe.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f11-368">The **CIM\_Rack** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="e2f11-369">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e2f11-369">WMI does not implement this class.</span></span>

<span data-ttu-id="e2f11-370">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e2f11-370">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2f11-371">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e2f11-371">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f11-372">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2f11-372">Requirements</span></span>



| <span data-ttu-id="e2f11-373">需求</span><span class="sxs-lookup"><span data-stu-id="e2f11-373">Requirement</span></span> | <span data-ttu-id="e2f11-374">值</span><span class="sxs-lookup"><span data-stu-id="e2f11-374">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f11-375">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2f11-375">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f11-376">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2f11-376">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2f11-377">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2f11-377">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f11-378">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2f11-378">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2f11-379">命名空間</span><span class="sxs-lookup"><span data-stu-id="e2f11-379">Namespace</span></span><br/>                | <span data-ttu-id="e2f11-380">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e2f11-380">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2f11-381">MOF</span><span class="sxs-lookup"><span data-stu-id="e2f11-381">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2f11-382"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2f11-382"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2f11-383">DLL</span><span class="sxs-lookup"><span data-stu-id="e2f11-383">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f11-384"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f11-384"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f11-385">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2f11-385">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f11-386">**CIM \_ PhysicalFrame**</span><span class="sxs-lookup"><span data-stu-id="e2f11-386">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 


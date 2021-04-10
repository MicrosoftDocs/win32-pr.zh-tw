---
description: CIM \_ PhysicalFrame 類別是機架、底座和其他框架主機殼的父類別，因為它們是在擴充類別中定義的。
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: CIM_PhysicalFrame 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111265"
---
# <a name="cim_physicalframe-class"></a><span data-ttu-id="e4d6e-103">CIM \_ PhysicalFrame 類別</span><span class="sxs-lookup"><span data-stu-id="e4d6e-103">CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="e4d6e-104">**CIM \_ PhysicalFrame** 類別是機架、底座和其他框架主機殼的父類別，因為它們是在擴充類別中定義的。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-104">The **CIM\_PhysicalFrame** class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="e4d6e-105">**VisibleAlarm** 和 **AudibleAlarm** 等屬性，以及與安全性缺口相關的資料會包含在這個父類別中。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-105">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4d6e-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e4d6e-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e4d6e-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e4d6e-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d6e-110">語法</span><span class="sxs-lookup"><span data-stu-id="e4d6e-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
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
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="e4d6e-111">成員</span><span class="sxs-lookup"><span data-stu-id="e4d6e-111">Members</span></span>

<span data-ttu-id="e4d6e-112">**CIM \_ PhysicalFrame** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e4d6e-112">The **CIM\_PhysicalFrame** class has these types of members:</span></span>

-   [<span data-ttu-id="e4d6e-113">方法</span><span class="sxs-lookup"><span data-stu-id="e4d6e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e4d6e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e4d6e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e4d6e-115">方法</span><span class="sxs-lookup"><span data-stu-id="e4d6e-115">Methods</span></span>

<span data-ttu-id="e4d6e-116">**CIM \_ PhysicalFrame** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-116">The **CIM\_PhysicalFrame** class has these methods.</span></span>



| <span data-ttu-id="e4d6e-117">方法</span><span class="sxs-lookup"><span data-stu-id="e4d6e-117">Method</span></span>                                                                 | <span data-ttu-id="e4d6e-118">描述</span><span class="sxs-lookup"><span data-stu-id="e4d6e-118">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4d6e-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalframe.md) | <span data-ttu-id="e4d6e-120">確認參考的實體元素是否可包含或插入實體封裝中。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-120">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="e4d6e-121">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e4d6e-122">屬性</span><span class="sxs-lookup"><span data-stu-id="e4d6e-122">Properties</span></span>

<span data-ttu-id="e4d6e-123">**CIM \_ PhysicalFrame** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-123">The **CIM\_PhysicalFrame** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4d6e-124">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-124">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-125">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-127">若 **為 TRUE**，則框架具有可聽見的警示。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-127">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ PhysicalFrame**.**SecurityBreach**") </span><span class="sxs-lookup"><span data-stu-id="e4d6e-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-132">提供詳細資訊的自由格式字串，如果 **SecurityBreach** 屬性指出發生缺口或某些其他安全性相關事件，則會提供更多資訊。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-133">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-133">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-136">自由格式的字串，其中包含有關如何連接及配套框架的各種纜線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-136">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="e4d6e-137">使用許多網路、儲存體相關和電源線，纜線管理可能是複雜且富有挑戰性的工作。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-137">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="e4d6e-138">此字串屬性包含的資訊可協助框架的元件和服務。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-138">This string property contains information to aid in assembly and service of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-142">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-143">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-143">Short textual description of the object.</span></span>

<span data-ttu-id="e4d6e-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-148">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-148">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-149">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-149">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e4d6e-150">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-150">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e4d6e-151">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-151">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-152">**深度**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-152">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-153">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-153">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-155">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-155">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-156">實體套件的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-156">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="e4d6e-157">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-157">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-158">**說明**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-161">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-162">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-162">Textual description of the object.</span></span>

<span data-ttu-id="e4d6e-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-164">**高度**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-164">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-165">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-165">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-167">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-168">實體封裝的高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-168">Height of the physical package, in inches.</span></span>

<span data-ttu-id="e4d6e-169">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-169">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-170">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-170">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-171">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-173">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-173">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="e4d6e-174">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-174">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="e4d6e-175">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-175">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="e4d6e-176">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-176">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="e4d6e-177">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-177">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-178">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-178">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-179">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-179">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-181">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e4d6e-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-182">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-182">Date and time the object was installed.</span></span> <span data-ttu-id="e4d6e-183">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-183">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e4d6e-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-185">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-185">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-186">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-188">若 **為 TRUE**，則會使用鎖定來保護框架。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-188">If **TRUE**, the frame is protected with a lock.</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-189">**製造商**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-189">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-192">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-193">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-193">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="e4d6e-194">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-194">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="e4d6e-195">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-195">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-196">**型號**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-196">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-199">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-199">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-200">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-200">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="e4d6e-201">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-202">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-205">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-206">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-206">Label by which the object is known.</span></span> <span data-ttu-id="e4d6e-207">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-207">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e4d6e-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-209">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-209">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-212">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-212">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="e4d6e-213">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-213">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="e4d6e-214">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-214">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="e4d6e-215">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-216">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-216">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-219">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-220">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-220">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="e4d6e-221">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-222">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-222">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-223">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-225">若 **為 TRUE**，則表示實體元素開啟電源;否則，它目前為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-225">If **TRUE**, the physical element is powered on; otherwise, it is currently off.</span></span>

<span data-ttu-id="e4d6e-226">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-226">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-227">**移動**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-227">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-228">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-230">若 **為 TRUE**，則會將這個專案設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-230">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="e4d6e-231">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-231">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="e4d6e-232">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-232">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="e4d6e-233">例如，「可升級處理器」晶片是卸載式的。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-233">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="e4d6e-234">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-234">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-235">**更換**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-235">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-236">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-238">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-238">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="e4d6e-239">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-239">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="e4d6e-240">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-240">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="e4d6e-241">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-241">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="e4d6e-242">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-242">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-243">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-243">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-244">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-246">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體容器 Global Table \| 002.12 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**。**BreachDescription**") </span><span class="sxs-lookup"><span data-stu-id="e4d6e-246">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-247">指出是否嘗試執行框架的實體缺口，但不成功或嘗試成功。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-247">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e4d6e-248">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-248">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4d6e-249">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-249">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="e4d6e-250">**無缺口** (3) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-250">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="e4d6e-251"> (4) **嘗試缺口**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-251">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="e4d6e-252">**缺口成功** (5) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-252">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4d6e-253">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-253">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-256">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-256">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-257">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-257">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="e4d6e-258">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-258">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-259">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-259">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-260">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e4d6e-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-262">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ PhysicalFrame**。**ServicePhilosophy**") </span><span class="sxs-lookup"><span data-stu-id="e4d6e-262">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-263">提供 **ServicePhilosophy** 陣列中專案詳細說明的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-263">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="e4d6e-264">這個陣列的每個專案都與 **ServicePhilosophy** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-264">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="e4d6e-265">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-265">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-266">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e4d6e-266">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-268">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ PhysicalFrame**。**ServiceDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="e4d6e-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-269">指出框架是否從頂端、前端、背面或側邊提供服務;以及是否有滑動的紙匣或卸載式邊，以及是否有可移動的框架 (例如，有滾筒) 。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-269">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4d6e-270">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-270">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e4d6e-271">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-271">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="e4d6e-272">**從 Top** (2) 的服務</span><span class="sxs-lookup"><span data-stu-id="e4d6e-272">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="e4d6e-273">前 (3) **的服務**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-273">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="e4d6e-274">**從背面** (4) 的服務</span><span class="sxs-lookup"><span data-stu-id="e4d6e-274">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="e4d6e-275">**服務從側** (5) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-275">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="e4d6e-276">**滑動紙** 匣 (6) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-276">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="e4d6e-277">**可移動側** (7) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-277">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="e4d6e-278">**可移動** (8) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-278">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4d6e-279">**SKU**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-279">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-282">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-282">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-283">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-283">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="e4d6e-284">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-284">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-285">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-288">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-288">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-289">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-289">Current status of the object.</span></span>

<span data-ttu-id="e4d6e-290">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e4d6e-291">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="e4d6e-291">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e4d6e-292">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-292">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e4d6e-293">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-293">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e4d6e-294">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-294">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4d6e-295">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-295">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e4d6e-296">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-296">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e4d6e-297">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-297">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e4d6e-298">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-298">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e4d6e-299">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-299">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e4d6e-300">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-300">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e4d6e-301">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-301">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e4d6e-302">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-302">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e4d6e-303">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-303">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4d6e-304">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-304">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-307">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-308">可唯一識別實體元素並作為專案索引鍵的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-308">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="e4d6e-309">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-309">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="e4d6e-310">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中非常高的位置，以獨立識別硬體/實體，無論 (或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-310">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="e4d6e-311">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-311">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="e4d6e-312">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-312">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="e4d6e-313">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-313">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="e4d6e-314">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-315">**版本**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-315">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-318">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-319">表示實體元素版本的字串。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-319">String that indicates the version of the physical element.</span></span>

<span data-ttu-id="e4d6e-320">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-321">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-321">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-322">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-324">若 **為 TRUE**，表示設備包含可見的警示。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-324">If **TRUE**, the equipment includes a visible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-325">**Weight**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-325">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-326">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-326">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-328">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-329">實體封裝的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-329">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="e4d6e-330">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-330">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d6e-331">**寬度**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-331">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d6e-332">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-332">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4d6e-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d6e-334">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="e4d6e-334">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="e4d6e-335">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-335">Width of the physical package, in inches.</span></span>

<span data-ttu-id="e4d6e-336">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-336">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4d6e-337">備註</span><span class="sxs-lookup"><span data-stu-id="e4d6e-337">Remarks</span></span>

<span data-ttu-id="e4d6e-338">**Cim \_ PhysicalFrame** 類別衍生自 [**cim \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-338">The **CIM\_PhysicalFrame** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="e4d6e-339">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-339">WMI does not implement this class.</span></span> <span data-ttu-id="e4d6e-340">針對衍生自 **CIM \_ PHYSICALFRAME** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-340">For WMI classes derived from **CIM\_PhysicalFrame**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e4d6e-341">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-341">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e4d6e-342">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e4d6e-342">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d6e-343">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4d6e-343">Requirements</span></span>



| <span data-ttu-id="e4d6e-344">需求</span><span class="sxs-lookup"><span data-stu-id="e4d6e-344">Requirement</span></span> | <span data-ttu-id="e4d6e-345">值</span><span class="sxs-lookup"><span data-stu-id="e4d6e-345">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d6e-346">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4d6e-346">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d6e-347">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d6e-347">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4d6e-348">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4d6e-348">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d6e-349">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4d6e-349">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4d6e-350">命名空間</span><span class="sxs-lookup"><span data-stu-id="e4d6e-350">Namespace</span></span><br/>                | <span data-ttu-id="e4d6e-351">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e4d6e-351">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e4d6e-352">MOF</span><span class="sxs-lookup"><span data-stu-id="e4d6e-352">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4d6e-353"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4d6e-353"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4d6e-354">DLL</span><span class="sxs-lookup"><span data-stu-id="e4d6e-354">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4d6e-355"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4d6e-355"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d6e-356">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4d6e-356">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d6e-357">**CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="e4d6e-357">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 


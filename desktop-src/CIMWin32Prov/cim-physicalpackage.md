---
description: CIM \_ PhysicalPackage 類別代表包含或裝載其他元件的實體元素。 範例包括機架主機殼或介面卡。
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: CIM_PhysicalPackage 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1905467fd949e2c18d8be9e7a7bfff39ad8d1477
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985391"
---
# <a name="cim_physicalpackage-class"></a><span data-ttu-id="2f7f5-104">CIM \_ PhysicalPackage 類別</span><span class="sxs-lookup"><span data-stu-id="2f7f5-104">CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="2f7f5-105">**CIM \_ PhysicalPackage** 類別代表包含或裝載其他元件的實體元素。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-105">The **CIM\_PhysicalPackage** class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="2f7f5-106">範例包括機架主機殼或介面卡。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-106">Examples are a rack enclosure or an adapter card.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f7f5-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2f7f5-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2f7f5-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2f7f5-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7f5-111">語法</span><span class="sxs-lookup"><span data-stu-id="2f7f5-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="2f7f5-112">成員</span><span class="sxs-lookup"><span data-stu-id="2f7f5-112">Members</span></span>

<span data-ttu-id="2f7f5-113">**CIM \_ PhysicalPackage** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2f7f5-113">The **CIM\_PhysicalPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="2f7f5-114">方法</span><span class="sxs-lookup"><span data-stu-id="2f7f5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f7f5-115">屬性</span><span class="sxs-lookup"><span data-stu-id="2f7f5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f7f5-116">方法</span><span class="sxs-lookup"><span data-stu-id="2f7f5-116">Methods</span></span>

<span data-ttu-id="2f7f5-117">**CIM \_ PhysicalPackage** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-117">The **CIM\_PhysicalPackage** class has these methods.</span></span>



| <span data-ttu-id="2f7f5-118">方法</span><span class="sxs-lookup"><span data-stu-id="2f7f5-118">Method</span></span>                                                                   | <span data-ttu-id="2f7f5-119">描述</span><span class="sxs-lookup"><span data-stu-id="2f7f5-119">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f7f5-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md) | <span data-ttu-id="2f7f5-121">確認參考的實體元素是否可包含或插入實體封裝中。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="2f7f5-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2f7f5-123">屬性</span><span class="sxs-lookup"><span data-stu-id="2f7f5-123">Properties</span></span>

<span data-ttu-id="2f7f5-124">**CIM \_ PhysicalPackage** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-124">The **CIM\_PhysicalPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f7f5-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-128">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-129">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-129">Short textual description of the object.</span></span>

<span data-ttu-id="2f7f5-130">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-134">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-135">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-135">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2f7f5-136">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-136">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2f7f5-137">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-138">**深度**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-139">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-141">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-142">實體套件的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-142">Depth of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-143">**說明**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-146">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-147">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-147">Textual description of the object.</span></span>

<span data-ttu-id="2f7f5-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-149">**高度**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-150">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-152">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-153">實體封裝的高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-153">Height of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-154">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-154">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-155">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-155">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-157">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-157">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="2f7f5-158">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-158">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="2f7f5-159">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-159">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="2f7f5-160">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-160">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-162">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-164">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="2f7f5-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-165">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-165">Date and time the object was installed.</span></span> <span data-ttu-id="2f7f5-166">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2f7f5-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-168">**製造商**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-168">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-171">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-172">產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-172">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="2f7f5-173">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-173">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="2f7f5-174">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-175">**型號**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-175">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-178">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-179">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-179">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="2f7f5-180">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-181">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-184">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-184">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-185">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-185">Label by which the object is known.</span></span> <span data-ttu-id="2f7f5-186">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-186">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2f7f5-187">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-188">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-188">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-191">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-191">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="2f7f5-192">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-192">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="2f7f5-193">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-193">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="2f7f5-194">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-195">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-195">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-198">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-199">由產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-199">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="2f7f5-200">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-201">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-201">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-202">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-204">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-204">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="2f7f5-205">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-206">**移動**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-206">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-207">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-209">若 **為 TRUE**，則會將封裝設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-209">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="2f7f5-210">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-210">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="2f7f5-211">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-211">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="2f7f5-212">例如，「可升級處理器」晶片是卸載式的。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-212">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-213">**更換**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-213">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-214">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-216">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-216">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="2f7f5-217">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-217">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="2f7f5-218">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-218">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="2f7f5-219">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-219">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-223">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-223">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-224">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="2f7f5-225">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-229">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-230">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="2f7f5-231">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-232">**狀態**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-235">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-235">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-236">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-236">Current status of the object.</span></span>

<span data-ttu-id="2f7f5-237">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2f7f5-238">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="2f7f5-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2f7f5-239">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2f7f5-240">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2f7f5-241">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f7f5-242">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2f7f5-243">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2f7f5-244">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2f7f5-245">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2f7f5-246">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2f7f5-247">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2f7f5-248">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2f7f5-249">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2f7f5-250">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f7f5-251">**Tag**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-251">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-254">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-254">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-255">可唯一識別實體元素並作為專案索引鍵的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-255">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="2f7f5-256">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-256">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="2f7f5-257">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-257">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="2f7f5-258">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-258">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="2f7f5-259">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-259">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="2f7f5-260">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-260">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="2f7f5-261">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-262">**版本**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-265">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-265">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-266">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-266">Version of the physical element.</span></span>

<span data-ttu-id="2f7f5-267">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-267">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-269">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-269">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-271">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-271">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-272">實體封裝的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-272">Weight of the physical package, in pounds.</span></span>

</dd> <dt>

<span data-ttu-id="2f7f5-273">**寬度**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-273">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f7f5-274">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-274">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f7f5-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f7f5-276">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="2f7f5-276">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="2f7f5-277">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-277">Width of the physical package, in inches.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f7f5-278">備註</span><span class="sxs-lookup"><span data-stu-id="2f7f5-278">Remarks</span></span>

<span data-ttu-id="2f7f5-279">**Cim \_ PhysicalPackage** 類別衍生自 [**cim \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-279">The **CIM\_PhysicalPackage** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="2f7f5-280">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-280">WMI does not implement this class.</span></span> <span data-ttu-id="2f7f5-281">針對衍生自 **CIM \_ PHYSICALPACKAGE** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-281">For WMI classes that are derived from **CIM\_PhysicalPackage**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2f7f5-282">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-282">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2f7f5-283">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2f7f5-283">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7f5-284">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f7f5-284">Requirements</span></span>



| <span data-ttu-id="2f7f5-285">需求</span><span class="sxs-lookup"><span data-stu-id="2f7f5-285">Requirement</span></span> | <span data-ttu-id="2f7f5-286">值</span><span class="sxs-lookup"><span data-stu-id="2f7f5-286">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7f5-287">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f7f5-287">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7f5-288">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f7f5-288">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f7f5-289">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f7f5-289">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7f5-290">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f7f5-290">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f7f5-291">命名空間</span><span class="sxs-lookup"><span data-stu-id="2f7f5-291">Namespace</span></span><br/>                | <span data-ttu-id="2f7f5-292">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2f7f5-292">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f7f5-293">MOF</span><span class="sxs-lookup"><span data-stu-id="2f7f5-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f7f5-294"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f7f5-294"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f7f5-295">DLL</span><span class="sxs-lookup"><span data-stu-id="2f7f5-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f7f5-296"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f7f5-296"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7f5-297">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f7f5-297">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7f5-298">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="2f7f5-298">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 


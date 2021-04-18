---
description: 「CIM 記憶 \_ 卡」類別代表一種實體容器類型，可插入另一張卡片或主控電路板，或本身是底座中的主控電路板/主機板。
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: CIM_Card 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b10478e5d0e34020f64d8775e857d9fa6af94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971320"
---
# <a name="cim_card-class"></a><span data-ttu-id="ab916-103">CIM \_ 卡片類別</span><span class="sxs-lookup"><span data-stu-id="ab916-103">CIM\_Card class</span></span>

<span data-ttu-id="ab916-104">「 **CIM 記憶 \_ 卡** 」類別代表一種實體容器類型，可插入另一張卡片或主控電路板，或本身是底座中的主控電路板/主機板。</span><span class="sxs-lookup"><span data-stu-id="ab916-104">The **CIM\_Card** class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="ab916-105">此類別包含任何能夠攜帶信號的封裝，並提供實體元件的掛接點，例如晶片或其他實體套件（例如其他卡片）。</span><span class="sxs-lookup"><span data-stu-id="ab916-105">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab916-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="ab916-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ab916-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="ab916-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ab916-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ab916-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ab916-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ab916-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab916-110">語法</span><span class="sxs-lookup"><span data-stu-id="ab916-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
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
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a><span data-ttu-id="ab916-111">成員</span><span class="sxs-lookup"><span data-stu-id="ab916-111">Members</span></span>

<span data-ttu-id="ab916-112">**CIM 記憶 \_ 卡** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ab916-112">The **CIM\_Card** class has these types of members:</span></span>

-   [<span data-ttu-id="ab916-113">方法</span><span class="sxs-lookup"><span data-stu-id="ab916-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab916-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ab916-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab916-115">方法</span><span class="sxs-lookup"><span data-stu-id="ab916-115">Methods</span></span>

<span data-ttu-id="ab916-116">**CIM 記憶 \_ 卡** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ab916-116">The **CIM\_Card** class has these methods.</span></span>



| <span data-ttu-id="ab916-117">方法</span><span class="sxs-lookup"><span data-stu-id="ab916-117">Method</span></span>                                                        | <span data-ttu-id="ab916-118">描述</span><span class="sxs-lookup"><span data-stu-id="ab916-118">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab916-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="ab916-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-card.md) | <span data-ttu-id="ab916-120">確認參考的實體元素是否可包含或插入實體封裝中。</span><span class="sxs-lookup"><span data-stu-id="ab916-120">Verifies whether the referenced physical element may be contained by or inserted into the physical package.</span></span> <span data-ttu-id="ab916-121">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ab916-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ab916-122">屬性</span><span class="sxs-lookup"><span data-stu-id="ab916-122">Properties</span></span>

<span data-ttu-id="ab916-123">**CIM 記憶 \_ 卡** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ab916-123">The **CIM\_Card** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab916-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="ab916-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-127">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-128">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="ab916-128">A short textual description of the object.</span></span>

<span data-ttu-id="ab916-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ab916-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-133">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ab916-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-134">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab916-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ab916-135">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="ab916-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ab916-136">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-136">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-137">**深度**</span><span class="sxs-lookup"><span data-stu-id="ab916-137">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-138">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="ab916-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-140">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-141">實體套件的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="ab916-141">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="ab916-142">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-142">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-143">**說明**</span><span class="sxs-lookup"><span data-stu-id="ab916-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-146">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-147">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ab916-147">A textual description of the object.</span></span>

<span data-ttu-id="ab916-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-149">**高度**</span><span class="sxs-lookup"><span data-stu-id="ab916-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-150">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="ab916-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-152">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-153">實體封裝的高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="ab916-153">Height of the physical package, in inches.</span></span>

<span data-ttu-id="ab916-154">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-154">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-155">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="ab916-155">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-156">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab916-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-158">若 **為 TRUE**，則這張卡片是一種主機板，也就是更一般的主機殼。</span><span class="sxs-lookup"><span data-stu-id="ab916-158">If **TRUE**, this card is a motherboard or, more generically, a baseboard in a chassis.</span></span>

</dd> <dt>

<span data-ttu-id="ab916-159">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="ab916-159">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-160">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab916-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-162">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="ab916-162">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="ab916-163">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="ab916-163">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="ab916-164">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="ab916-164">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="ab916-165">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="ab916-165">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="ab916-166">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-166">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-167">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ab916-167">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-168">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ab916-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-170">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="ab916-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-171">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="ab916-171">Indicates when the object was installed.</span></span> <span data-ttu-id="ab916-172">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="ab916-172">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ab916-173">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-174">**製造商**</span><span class="sxs-lookup"><span data-stu-id="ab916-174">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-177">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ab916-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-178">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="ab916-178">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="ab916-179">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ab916-179">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="ab916-180">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-181">**型號**</span><span class="sxs-lookup"><span data-stu-id="ab916-181">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-184">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ab916-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-185">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab916-185">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="ab916-186">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-186">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-187">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ab916-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-190">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-190">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-191">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="ab916-191">Label by which the object is known.</span></span> <span data-ttu-id="ab916-192">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="ab916-192">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ab916-193">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-194">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ab916-194">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-197">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="ab916-197">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="ab916-198">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="ab916-198">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="ab916-199">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="ab916-199">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="ab916-200">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-201">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="ab916-201">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-204">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ab916-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-205">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="ab916-205">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="ab916-206">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-207">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="ab916-207">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-208">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab916-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-210">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="ab916-210">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="ab916-211">否則，它目前為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="ab916-211">Otherwise, it is currently off.</span></span>

<span data-ttu-id="ab916-212">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-213">**移動**</span><span class="sxs-lookup"><span data-stu-id="ab916-213">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-214">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab916-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-216">若 **為 TRUE**，則會將封裝設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="ab916-216">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="ab916-217">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="ab916-217">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="ab916-218">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="ab916-218">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="ab916-219">例如，「可升級處理器」晶片是卸載式的。</span><span class="sxs-lookup"><span data-stu-id="ab916-219">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="ab916-220">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-220">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-221">**更換**</span><span class="sxs-lookup"><span data-stu-id="ab916-221">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-222">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab916-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-224">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="ab916-224">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="ab916-225">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="ab916-225">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="ab916-226">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="ab916-226">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="ab916-227">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="ab916-227">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="ab916-228">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-228">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-229">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="ab916-229">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-232">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 卡**」。**SpecialRequirements**") </span><span class="sxs-lookup"><span data-stu-id="ab916-232">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-233">描述卡片與其他卡片實際獨特之方式的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="ab916-233">Free-form string that describes the ways in which the card is physically unique from other cards.</span></span> <span data-ttu-id="ab916-234">只有當對應的布林值屬性 **SpecialRequirements** 設為 **TRUE** 時，這個屬性才有意義。</span><span class="sxs-lookup"><span data-stu-id="ab916-234">This property only has meaning when the corresponding Boolean property, **SpecialRequirements**, is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab916-235">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="ab916-235">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-236">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab916-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-238">若為 **TRUE**，表示要正常運作，至少需要一個 daughterboard 或輔助卡片。</span><span class="sxs-lookup"><span data-stu-id="ab916-238">If **TRUE**, to function properly, at least one daughterboard or auxiliary card is required.</span></span>

</dd> <dt>

<span data-ttu-id="ab916-239">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ab916-239">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-242">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ab916-242">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-243">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="ab916-243">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="ab916-244">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-244">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-245">**SKU**</span><span class="sxs-lookup"><span data-stu-id="ab916-245">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-248">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ab916-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-249">此實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="ab916-249">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="ab916-250">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-250">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-251">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="ab916-251">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab916-254">描述位置位置的自由格式字串、一般使用方式、限制、個別位置間距，或卡片插槽的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ab916-254">Free-form string that describes the slot positioning, typical usage, restrictions, individual slot spacings, or other pertinent information for the slots on a card.</span></span>

</dd> <dt>

<span data-ttu-id="ab916-255">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="ab916-255">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-256">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab916-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-258">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 卡**」。**RequirementsDescription**") </span><span class="sxs-lookup"><span data-stu-id="ab916-258">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-259">若 **為 TRUE**，則卡片與相同類型的其他卡片實際上是唯一的，因此需要特殊插槽。</span><span class="sxs-lookup"><span data-stu-id="ab916-259">If **TRUE**, the card is physically unique from other cards of the same type and, therefore, requires a special slot.</span></span> <span data-ttu-id="ab916-260">例如，雙卡片需要兩個插槽。</span><span class="sxs-lookup"><span data-stu-id="ab916-260">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="ab916-261">另一個範例是當特定卡片可用於與其他卡片相同的一般功能時，但需要特殊插槽 (很長的時間，例如) ;然而，其他卡片可以放在任何可用的位置。</span><span class="sxs-lookup"><span data-stu-id="ab916-261">Another example is when a certain card can be used for the same general function as other cards, but requires a special slot (extra long, for example); whereas, other cards can be placed in any available slot.</span></span> <span data-ttu-id="ab916-262">若 **為 TRUE**，則對應的 **RequirementsDescription** 屬性應該指定卡片唯一性或用途的本質。</span><span class="sxs-lookup"><span data-stu-id="ab916-262">If **TRUE**, the corresponding **RequirementsDescription** property should specify the nature of the uniqueness or purpose of the card.</span></span>

</dd> <dt>

<span data-ttu-id="ab916-263">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ab916-263">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-266">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-267">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="ab916-267">String that indicates the current status of the object.</span></span> <span data-ttu-id="ab916-268">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="ab916-268">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ab916-269">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="ab916-269">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ab916-270">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="ab916-270">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ab916-271">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ab916-271">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ab916-272">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="ab916-272">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ab916-273">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ab916-273">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ab916-274">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-274">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ab916-275">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="ab916-275">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ab916-276">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ab916-276">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ab916-277">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-277">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ab916-278">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-278">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ab916-279">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-279">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ab916-280">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-280">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ab916-281">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-281">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ab916-282">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-282">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ab916-283">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-283">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ab916-284">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-284">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ab916-285">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-285">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ab916-286">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-286">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ab916-287">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-287">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ab916-288">**Tag**</span><span class="sxs-lookup"><span data-stu-id="ab916-288">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-291">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ab916-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-292">可唯一識別實體元素，並作為專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ab916-292">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="ab916-293">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="ab916-293">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="ab916-294">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="ab916-294">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="ab916-295">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="ab916-295">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="ab916-296">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="ab916-296">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="ab916-297">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="ab916-297">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="ab916-298">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-299">**版本**</span><span class="sxs-lookup"><span data-stu-id="ab916-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab916-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-302">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ab916-302">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ab916-303">指出實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="ab916-303">Indicates the version of the physical element.</span></span>

<span data-ttu-id="ab916-304">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-304">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-305">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ab916-305">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-306">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="ab916-306">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-308">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="ab916-308">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-309">實體封裝的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="ab916-309">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="ab916-310">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-310">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab916-311">**寬度**</span><span class="sxs-lookup"><span data-stu-id="ab916-311">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab916-312">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="ab916-312">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ab916-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab916-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab916-314">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="ab916-314">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ab916-315">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="ab916-315">Width of the physical package, in inches.</span></span>

<span data-ttu-id="ab916-316">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-316">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab916-317">備註</span><span class="sxs-lookup"><span data-stu-id="ab916-317">Remarks</span></span>

<span data-ttu-id="ab916-318">**Cim 記憶 \_ 卡** 類別衍生自 [**cim \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-318">The **CIM\_Card** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="ab916-319">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="ab916-319">WMI does not implement this class.</span></span> <span data-ttu-id="ab916-320">如需有關衍生自 **CIM \_ 卡片** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ab916-320">For more information about classes derived from **CIM\_Card**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ab916-321">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="ab916-321">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ab916-322">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ab916-322">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab916-323">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab916-323">Requirements</span></span>



| <span data-ttu-id="ab916-324">需求</span><span class="sxs-lookup"><span data-stu-id="ab916-324">Requirement</span></span> | <span data-ttu-id="ab916-325">值</span><span class="sxs-lookup"><span data-stu-id="ab916-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab916-326">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab916-326">Minimum supported client</span></span><br/> | <span data-ttu-id="ab916-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab916-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab916-328">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab916-328">Minimum supported server</span></span><br/> | <span data-ttu-id="ab916-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab916-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab916-330">命名空間</span><span class="sxs-lookup"><span data-stu-id="ab916-330">Namespace</span></span><br/>                | <span data-ttu-id="ab916-331">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ab916-331">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab916-332">MOF</span><span class="sxs-lookup"><span data-stu-id="ab916-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab916-333"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab916-333"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab916-334">DLL</span><span class="sxs-lookup"><span data-stu-id="ab916-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab916-335"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab916-335"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab916-336">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab916-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab916-337">**CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="ab916-337">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 


---
description: CIM \_ 晶片類別代表整合電路硬體的類型，包括 ASICs、處理器、記憶體晶片等等。
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: CIM_Chip 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468361"
---
# <a name="cim_chip-class"></a><span data-ttu-id="d7760-103">CIM \_ 晶片類別</span><span class="sxs-lookup"><span data-stu-id="d7760-103">CIM\_Chip class</span></span>

<span data-ttu-id="d7760-104">**CIM \_ 晶片** 類別代表整合電路硬體的類型，包括 ASICs、處理器、記憶體晶片等等。</span><span class="sxs-lookup"><span data-stu-id="d7760-104">The **CIM\_Chip** class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7760-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d7760-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d7760-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d7760-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d7760-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7760-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d7760-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="d7760-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7760-109">語法</span><span class="sxs-lookup"><span data-stu-id="d7760-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
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
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  uint16   FormFactor;
};
```

## <a name="members"></a><span data-ttu-id="d7760-110">成員</span><span class="sxs-lookup"><span data-stu-id="d7760-110">Members</span></span>

<span data-ttu-id="d7760-111">**CIM \_ 晶片** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7760-111">The **CIM\_Chip** class has these types of members:</span></span>

-   [<span data-ttu-id="d7760-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d7760-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7760-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d7760-113">Properties</span></span>

<span data-ttu-id="d7760-114">**CIM \_ 晶片** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7760-114">The **CIM\_Chip** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7760-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="d7760-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="d7760-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d7760-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="d7760-119">A short textual description of the object.</span></span>

<span data-ttu-id="d7760-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d7760-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-124">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d7760-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-125">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7760-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d7760-126">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="d7760-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d7760-127">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-127">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="d7760-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-131">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="d7760-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d7760-132">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="d7760-132">A textual description of the object.</span></span>

<span data-ttu-id="d7760-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-134">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="d7760-134">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7760-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7760-137">晶片的實外型規格。</span><span class="sxs-lookup"><span data-stu-id="d7760-137">Implementation form factor for the chip.</span></span> <span data-ttu-id="d7760-138">您可以指定下列值。</span><span class="sxs-lookup"><span data-stu-id="d7760-138">The following values can be specified.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d7760-139">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d7760-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d7760-140">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d7760-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="d7760-141">**SIP** (2) </span><span class="sxs-lookup"><span data-stu-id="d7760-141">**SIP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

<span data-ttu-id="d7760-142">**DIP** (3) </span><span class="sxs-lookup"><span data-stu-id="d7760-142">**DIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

<span data-ttu-id="d7760-143">**ZIP** (4) </span><span class="sxs-lookup"><span data-stu-id="d7760-143">**ZIP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

<span data-ttu-id="d7760-144">**SOJ** (5) </span><span class="sxs-lookup"><span data-stu-id="d7760-144">**SOJ** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="d7760-145">**專屬** (6) </span><span class="sxs-lookup"><span data-stu-id="d7760-145">**Proprietary** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

<span data-ttu-id="d7760-146">**SIMM** (7) </span><span class="sxs-lookup"><span data-stu-id="d7760-146">**SIMM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

<span data-ttu-id="d7760-147">**DIMM** (8) </span><span class="sxs-lookup"><span data-stu-id="d7760-147">**DIMM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

<span data-ttu-id="d7760-148">**TSOP** (9) </span><span class="sxs-lookup"><span data-stu-id="d7760-148">**TSOP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

<span data-ttu-id="d7760-149">**PGA** (10) </span><span class="sxs-lookup"><span data-stu-id="d7760-149">**PGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

<span data-ttu-id="d7760-150">**RIMM** (11) </span><span class="sxs-lookup"><span data-stu-id="d7760-150">**RIMM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

<span data-ttu-id="d7760-151">**SODIMM** (12) </span><span class="sxs-lookup"><span data-stu-id="d7760-151">**SODIMM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

<span data-ttu-id="d7760-152">**SRIMM** (13) </span><span class="sxs-lookup"><span data-stu-id="d7760-152">**SRIMM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

<span data-ttu-id="d7760-153">**SMD** (14) </span><span class="sxs-lookup"><span data-stu-id="d7760-153">**SMD** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

<span data-ttu-id="d7760-154">**SSMP** (15) </span><span class="sxs-lookup"><span data-stu-id="d7760-154">**SSMP** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

<span data-ttu-id="d7760-155">**QFP** (16) </span><span class="sxs-lookup"><span data-stu-id="d7760-155">**QFP** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

<span data-ttu-id="d7760-156">**TQFP** (17) </span><span class="sxs-lookup"><span data-stu-id="d7760-156">**TQFP** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

<span data-ttu-id="d7760-157">**SOIC** (18) </span><span class="sxs-lookup"><span data-stu-id="d7760-157">**SOIC** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

<span data-ttu-id="d7760-158">**LCC** (19) </span><span class="sxs-lookup"><span data-stu-id="d7760-158">**LCC** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

<span data-ttu-id="d7760-159">**PLCC** (20) </span><span class="sxs-lookup"><span data-stu-id="d7760-159">**PLCC** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

<span data-ttu-id="d7760-160">**BGA** (21) </span><span class="sxs-lookup"><span data-stu-id="d7760-160">**BGA** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

<span data-ttu-id="d7760-161">**FPBGA** (22) </span><span class="sxs-lookup"><span data-stu-id="d7760-161">**FPBGA** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

<span data-ttu-id="d7760-162">**LGA** (23) </span><span class="sxs-lookup"><span data-stu-id="d7760-162">**LGA** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

<span data-ttu-id="d7760-163">**FB-DIMM** (24) </span><span class="sxs-lookup"><span data-stu-id="d7760-163">**FB-DIMM** (24)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d7760-164">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="d7760-164">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-165">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7760-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7760-167">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="d7760-167">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="d7760-168">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="d7760-168">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="d7760-169">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="d7760-169">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="d7760-170">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="d7760-170">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="d7760-171">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-171">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d7760-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-173">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d7760-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-175">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="d7760-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d7760-176">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="d7760-176">Indicates when the object was installed.</span></span> <span data-ttu-id="d7760-177">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="d7760-177">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d7760-178">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-179">**製造商**</span><span class="sxs-lookup"><span data-stu-id="d7760-179">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-182">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d7760-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-183">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="d7760-183">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="d7760-184">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d7760-184">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="d7760-185">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-185">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-186">**型號**</span><span class="sxs-lookup"><span data-stu-id="d7760-186">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-189">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d7760-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-190">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7760-190">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="d7760-191">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-191">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-192">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d7760-192">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-195">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="d7760-195">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d7760-196">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="d7760-196">Label by which the object is known.</span></span> <span data-ttu-id="d7760-197">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="d7760-197">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d7760-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-199">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d7760-199">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7760-202">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="d7760-202">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="d7760-203">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="d7760-203">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="d7760-204">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="d7760-204">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="d7760-205">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-206">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="d7760-206">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-209">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d7760-209">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-210">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="d7760-210">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="d7760-211">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-211">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-212">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="d7760-212">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-213">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7760-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7760-215">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="d7760-215">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="d7760-216">否則，它目前為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="d7760-216">Otherwise, it is currently off.</span></span>

<span data-ttu-id="d7760-217">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-217">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-218">**移動**</span><span class="sxs-lookup"><span data-stu-id="d7760-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7760-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7760-221">若 **為 TRUE**，則會將這個專案設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="d7760-221">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="d7760-222">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="d7760-222">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="d7760-223">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="d7760-223">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="d7760-224">例如，「可升級處理器」晶片是卸載式的。</span><span class="sxs-lookup"><span data-stu-id="d7760-224">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="d7760-225">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-225">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-226">**更換**</span><span class="sxs-lookup"><span data-stu-id="d7760-226">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-227">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7760-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7760-229">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="d7760-229">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="d7760-230">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="d7760-230">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="d7760-231">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="d7760-231">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="d7760-232">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="d7760-232">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="d7760-233">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-233">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-234">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d7760-234">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-237">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d7760-237">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-238">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="d7760-238">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="d7760-239">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-240">**SKU**</span><span class="sxs-lookup"><span data-stu-id="d7760-240">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-243">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d7760-243">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-244">此實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="d7760-244">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="d7760-245">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-245">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-246">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d7760-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-249">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="d7760-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d7760-250">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="d7760-250">String that indicates the current status of the object.</span></span> <span data-ttu-id="d7760-251">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="d7760-251">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d7760-252">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="d7760-252">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d7760-253">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="d7760-253">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d7760-254">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d7760-254">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d7760-255">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="d7760-255">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d7760-256">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d7760-256">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d7760-257">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-257">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d7760-258">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="d7760-258">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d7760-259">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d7760-259">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d7760-260">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-260">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d7760-261">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-261">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d7760-262">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-262">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d7760-263">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-263">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d7760-264">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-264">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d7760-265">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-265">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d7760-266">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-266">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d7760-267">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-267">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d7760-268">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="d7760-268">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d7760-269">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-269">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d7760-270">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="d7760-270">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d7760-271">**Tag**</span><span class="sxs-lookup"><span data-stu-id="d7760-271">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-274">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d7760-274">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-275">可唯一識別實體元素，並作為專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d7760-275">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="d7760-276">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="d7760-276">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="d7760-277">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="d7760-277">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="d7760-278">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="d7760-278">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="d7760-279">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="d7760-279">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="d7760-280">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="d7760-280">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="d7760-281">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7760-282">**版本**</span><span class="sxs-lookup"><span data-stu-id="d7760-282">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7760-283">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7760-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7760-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7760-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7760-285">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d7760-285">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d7760-286">指出實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="d7760-286">Indicates the version of the physical element.</span></span>

<span data-ttu-id="d7760-287">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7760-288">備註</span><span class="sxs-lookup"><span data-stu-id="d7760-288">Remarks</span></span>

<span data-ttu-id="d7760-289">**Cim \_ 晶片** 類別衍生自 [**cim \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-289">The **CIM\_Chip** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="d7760-290">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="d7760-290">WMI does not implement this class.</span></span> <span data-ttu-id="d7760-291">如需衍生自 **CIM \_ 晶片** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d7760-291">For more information about classes derived from **CIM\_Chip**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d7760-292">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d7760-292">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d7760-293">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d7760-293">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7760-294">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7760-294">Requirements</span></span>



| <span data-ttu-id="d7760-295">需求</span><span class="sxs-lookup"><span data-stu-id="d7760-295">Requirement</span></span> | <span data-ttu-id="d7760-296">值</span><span class="sxs-lookup"><span data-stu-id="d7760-296">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7760-297">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7760-297">Minimum supported client</span></span><br/> | <span data-ttu-id="d7760-298">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7760-298">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7760-299">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7760-299">Minimum supported server</span></span><br/> | <span data-ttu-id="d7760-300">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7760-300">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7760-301">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7760-301">Namespace</span></span><br/>                | <span data-ttu-id="d7760-302">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d7760-302">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d7760-303">MOF</span><span class="sxs-lookup"><span data-stu-id="d7760-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7760-304"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7760-304"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7760-305">DLL</span><span class="sxs-lookup"><span data-stu-id="d7760-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7760-306"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7760-306"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7760-307">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7760-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7760-308">**CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="d7760-308">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 


---
description: CIM \_ PhysicalMedia 類別代表檔和儲存媒體的類型，例如磁帶、CD rom 等等。
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: CIM_PhysicalMedia 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195764"
---
# <a name="cim_physicalmedia-class"></a><span data-ttu-id="e68df-103">CIM \_ PhysicalMedia 類別</span><span class="sxs-lookup"><span data-stu-id="e68df-103">CIM\_PhysicalMedia class</span></span>

<span data-ttu-id="e68df-104">**CIM \_ PhysicalMedia** 類別代表檔和儲存媒體的類型，例如磁帶、CD rom 等等。</span><span class="sxs-lookup"><span data-stu-id="e68df-104">The **CIM\_PhysicalMedia** class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span> <span data-ttu-id="e68df-105">此類別通常用來尋找和管理卸載式媒體 (與媒體存取裝置以單一套件的形式密封媒體，例如硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="e68df-105">This class is typically used to locate and manage removable media (versus media sealed with the media access device as a single package, such as hard disks).</span></span> <span data-ttu-id="e68df-106">不過，當媒體與使用 [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) 關聯性的實體套件相關聯時，密封的媒體也可以使用這個類別來建立模型。</span><span class="sxs-lookup"><span data-stu-id="e68df-106">Sealed media, however, can also be modeled using this class when the media is associated with the physical package using the [**CIM\_PackagedComponent**](cim-packagedcomponent.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e68df-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e68df-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e68df-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e68df-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e68df-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e68df-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e68df-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e68df-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68df-111">語法</span><span class="sxs-lookup"><span data-stu-id="e68df-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
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
  boolean  WriteProtectOn;
};
```

## <a name="members"></a><span data-ttu-id="e68df-112">成員</span><span class="sxs-lookup"><span data-stu-id="e68df-112">Members</span></span>

<span data-ttu-id="e68df-113">**CIM \_ PhysicalMedia** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e68df-113">The **CIM\_PhysicalMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="e68df-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e68df-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e68df-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e68df-115">Properties</span></span>

<span data-ttu-id="e68df-116">**CIM \_ PhysicalMedia** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e68df-116">The **CIM\_PhysicalMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e68df-117">**容量**</span><span class="sxs-lookup"><span data-stu-id="e68df-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-118">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e68df-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-120">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="e68df-120">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-121">可以讀取或寫入媒體的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e68df-121">Number of bytes that can be read from, or written to, a media.</span></span> <span data-ttu-id="e68df-122">此屬性不適用於硬複製 (檔) 或更簡潔的媒體。</span><span class="sxs-lookup"><span data-stu-id="e68df-122">This property is not applicable to hard copy (documentation) or cleaner media.</span></span> <span data-ttu-id="e68df-123">不應假設資料壓縮，因為這樣會增加這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e68df-123">Data compression should not be assumed, as it would increase the value in this property.</span></span> <span data-ttu-id="e68df-124">若是磁帶，則應該假設媒體上不會記錄任何檔案標記或空白區域。</span><span class="sxs-lookup"><span data-stu-id="e68df-124">For tapes, it should be assumed that no file marks or blank space areas are recorded on the media.</span></span>

<span data-ttu-id="e68df-125">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="e68df-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="e68df-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-129">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e68df-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-130">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e68df-130">Short textual description of the object.</span></span>

<span data-ttu-id="e68df-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-132">**CleanerMedia**</span><span class="sxs-lookup"><span data-stu-id="e68df-132">**CleanerMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e68df-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e68df-135">若為 **TRUE**，則會使用實體媒體進行清理，而不是資料儲存。</span><span class="sxs-lookup"><span data-stu-id="e68df-135">If **TRUE**, the physical media is used for cleaning purposes, not data storage.</span></span>

</dd> <dt>

<span data-ttu-id="e68df-136">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e68df-136">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-139">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e68df-139">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-140">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e68df-140">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e68df-141">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="e68df-141">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e68df-142">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-142">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-143">**說明**</span><span class="sxs-lookup"><span data-stu-id="e68df-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-146">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e68df-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-147">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e68df-147">Textual description of the object.</span></span>

<span data-ttu-id="e68df-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="e68df-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-150">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e68df-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e68df-152">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="e68df-152">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="e68df-153">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="e68df-153">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="e68df-154">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="e68df-154">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="e68df-155">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="e68df-155">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="e68df-156">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-156">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e68df-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-158">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e68df-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-160">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e68df-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-161">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e68df-161">Date and time the object was installed.</span></span> <span data-ttu-id="e68df-162">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e68df-162">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e68df-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-164">**製造商**</span><span class="sxs-lookup"><span data-stu-id="e68df-164">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-167">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e68df-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-168">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="e68df-168">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="e68df-169">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e68df-169">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="e68df-170">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-170">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-171">**MediaDescription**</span><span class="sxs-lookup"><span data-stu-id="e68df-171">**MediaDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-174">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ PhysicalMedia**.**媒體媒體**) </span><span class="sxs-lookup"><span data-stu-id="e68df-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-175">與 **媒體** 類型列舉相關的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e68df-175">Additional detail related to the **MediaType** enumeration.</span></span> <span data-ttu-id="e68df-176">例如，如果已指定值 3 ( 「QIC 墨水匣」 ) ，此屬性會指出磁帶是寬或1/4 英寸、預先格式化、Travan 相容等。</span><span class="sxs-lookup"><span data-stu-id="e68df-176">For example, if value 3 ("QIC Cartridge") is specified, this property would indicate whether the tape is wide or 1/4 inch, pre-formatted, Travan compatible, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e68df-177">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="e68df-177">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-178">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e68df-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-180">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ PhysicalMedia**.**MediaDescription**") </span><span class="sxs-lookup"><span data-stu-id="e68df-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-181">實體媒體的類型。</span><span class="sxs-lookup"><span data-stu-id="e68df-181">Type of physical media.</span></span> <span data-ttu-id="e68df-182">**MediaDescription** 屬性可提供更明確的媒體類型定義。</span><span class="sxs-lookup"><span data-stu-id="e68df-182">The **MediaDescription** property provides more explicit definition of the media type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e68df-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e68df-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e68df-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e68df-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span data-ttu-id="e68df-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**磁帶盒** (2) </span><span class="sxs-lookup"><span data-stu-id="e68df-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Tape Cartridge** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span data-ttu-id="e68df-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span> (3) 的 **QIC 墨水匣**</span><span class="sxs-lookup"><span data-stu-id="e68df-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC Cartridge** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span data-ttu-id="e68df-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT 墨水匣** (4) </span><span class="sxs-lookup"><span data-stu-id="e68df-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT Cartridge** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span data-ttu-id="e68df-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**W3c-dtf 墨水匣** (5) </span><span class="sxs-lookup"><span data-stu-id="e68df-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF Cartridge** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span data-ttu-id="e68df-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT 墨水匣** (6) </span><span class="sxs-lookup"><span data-stu-id="e68df-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT Cartridge** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="e68df-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8 毫米的磁帶墨水匣** (7) </span><span class="sxs-lookup"><span data-stu-id="e68df-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8mm Tape Cartridge** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="e68df-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>19mm (8) 的 **磁帶墨水匣**</span><span class="sxs-lookup"><span data-stu-id="e68df-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19mm Tape Cartridge** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span data-ttu-id="e68df-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT 盒** (9) </span><span class="sxs-lookup"><span data-stu-id="e68df-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT Cartridge** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span data-ttu-id="e68df-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**半英寸磁性磁帶墨水匣** (10) </span><span class="sxs-lookup"><span data-stu-id="e68df-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Half-Inch Magnetic Tape Cartridge** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span data-ttu-id="e68df-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**磁帶磁片** (11) </span><span class="sxs-lookup"><span data-stu-id="e68df-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Cartridge Disk** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span data-ttu-id="e68df-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12) </span><span class="sxs-lookup"><span data-stu-id="e68df-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span data-ttu-id="e68df-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP 磁片** (13) </span><span class="sxs-lookup"><span data-stu-id="e68df-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP Disk** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span data-ttu-id="e68df-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14) </span><span class="sxs-lookup"><span data-stu-id="e68df-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span data-ttu-id="e68df-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**溫徹斯特抽取式磁碟** (15) </span><span class="sxs-lookup"><span data-stu-id="e68df-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester Removable Disk** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="e68df-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**Cd-rom** (16) </span><span class="sxs-lookup"><span data-stu-id="e68df-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="e68df-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**Cd-rom/XA** (17) </span><span class="sxs-lookup"><span data-stu-id="e68df-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="e68df-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18) </span><span class="sxs-lookup"><span data-stu-id="e68df-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="e68df-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD 可燒錄** (19) </span><span class="sxs-lookup"><span data-stu-id="e68df-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span data-ttu-id="e68df-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20) </span><span class="sxs-lookup"><span data-stu-id="e68df-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span data-ttu-id="e68df-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**磁光** (21) </span><span class="sxs-lookup"><span data-stu-id="e68df-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="e68df-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22) </span><span class="sxs-lookup"><span data-stu-id="e68df-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span data-ttu-id="e68df-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23) </span><span class="sxs-lookup"><span data-stu-id="e68df-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD+RW** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="e68df-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24) </span><span class="sxs-lookup"><span data-stu-id="e68df-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="e68df-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**Dvd-rom** (25) </span><span class="sxs-lookup"><span data-stu-id="e68df-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="e68df-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-影片** (26) </span><span class="sxs-lookup"><span data-stu-id="e68df-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="e68df-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27) </span><span class="sxs-lookup"><span data-stu-id="e68df-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span data-ttu-id="e68df-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**軟碟/磁片** (28) </span><span class="sxs-lookup"><span data-stu-id="e68df-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/Diskette** (28)</span></span>


</dt> <dd>

<span data-ttu-id="e68df-212">磁碟片</span><span class="sxs-lookup"><span data-stu-id="e68df-212">Floppy disk</span></span>

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span data-ttu-id="e68df-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**硬碟** (29) </span><span class="sxs-lookup"><span data-stu-id="e68df-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Hard Disk** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span data-ttu-id="e68df-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**記憶卡** (30) </span><span class="sxs-lookup"><span data-stu-id="e68df-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Memory Card** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span data-ttu-id="e68df-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**硬複製** (31) </span><span class="sxs-lookup"><span data-stu-id="e68df-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Hard Copy** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span data-ttu-id="e68df-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**按一下 Disk** (32) </span><span class="sxs-lookup"><span data-stu-id="e68df-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik Disk** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="e68df-217"><span id="CD-RW"></span><span id="cd-rw"></span>**Cd-rw (33**) </span><span class="sxs-lookup"><span data-stu-id="e68df-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="e68df-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34) </span><span class="sxs-lookup"><span data-stu-id="e68df-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="e68df-219"><span id="CD_"></span><span id="cd_"></span>**CD +** (35) </span><span class="sxs-lookup"><span data-stu-id="e68df-219"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="e68df-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD 可燒錄** (36) </span><span class="sxs-lookup"><span data-stu-id="e68df-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="e68df-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**Cd-rw** (37) </span><span class="sxs-lookup"><span data-stu-id="e68df-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="e68df-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-音訊** (38) </span><span class="sxs-lookup"><span data-stu-id="e68df-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="e68df-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39) </span><span class="sxs-lookup"><span data-stu-id="e68df-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="e68df-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40) </span><span class="sxs-lookup"><span data-stu-id="e68df-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="e68df-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41) </span><span class="sxs-lookup"><span data-stu-id="e68df-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="e68df-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42) </span><span class="sxs-lookup"><span data-stu-id="e68df-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span data-ttu-id="e68df-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span> (43) 的 **磁/光碟重寫**</span><span class="sxs-lookup"><span data-stu-id="e68df-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-Optical Rewriteable** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span data-ttu-id="e68df-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**光碟寫入一次** (44) </span><span class="sxs-lookup"><span data-stu-id="e68df-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-Optical Write Once** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span data-ttu-id="e68df-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**(LIMDOW)** (45) 的磁/光碟</span><span class="sxs-lookup"><span data-stu-id="e68df-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical Rewriteable (LIMDOW)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span data-ttu-id="e68df-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**階段變更寫入一次** (46) </span><span class="sxs-lookup"><span data-stu-id="e68df-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Change Write Once** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span data-ttu-id="e68df-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**階段變更能改寫** (47) </span><span class="sxs-lookup"><span data-stu-id="e68df-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Phase Change Rewriteable** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span data-ttu-id="e68df-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**階段變更雙重** 重複)  (48</span><span class="sxs-lookup"><span data-stu-id="e68df-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phase Change Dual Rewriteable** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span data-ttu-id="e68df-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write** (49) </span><span class="sxs-lookup"><span data-stu-id="e68df-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write Once** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span data-ttu-id="e68df-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**近距離欄位錄製** (50) </span><span class="sxs-lookup"><span data-stu-id="e68df-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near Field Recording** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span data-ttu-id="e68df-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51) </span><span class="sxs-lookup"><span data-stu-id="e68df-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span data-ttu-id="e68df-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52) </span><span class="sxs-lookup"><span data-stu-id="e68df-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span data-ttu-id="e68df-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span> (53) 的 **8 毫米金屬粒子**</span><span class="sxs-lookup"><span data-stu-id="e68df-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm Metal Particle** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span data-ttu-id="e68df-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8 毫米 Advanced 裸機 Evaporate** (54) </span><span class="sxs-lookup"><span data-stu-id="e68df-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal Evaporate** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span data-ttu-id="e68df-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55) </span><span class="sxs-lookup"><span data-stu-id="e68df-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span data-ttu-id="e68df-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56) </span><span class="sxs-lookup"><span data-stu-id="e68df-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span data-ttu-id="e68df-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57) </span><span class="sxs-lookup"><span data-stu-id="e68df-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span data-ttu-id="e68df-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 曲目磁帶** (58) </span><span class="sxs-lookup"><span data-stu-id="e68df-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Track Tape** (58)</span></span>


</dt> <dd>

<span data-ttu-id="e68df-243">9-追蹤磁帶</span><span class="sxs-lookup"><span data-stu-id="e68df-243">9-track tape</span></span>

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span data-ttu-id="e68df-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 曲目磁帶** (59) </span><span class="sxs-lookup"><span data-stu-id="e68df-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Track Tape** (59)</span></span>


</dt> <dd>

<span data-ttu-id="e68df-245">18-追蹤磁帶</span><span class="sxs-lookup"><span data-stu-id="e68df-245">18-track tape</span></span>

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span data-ttu-id="e68df-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 追蹤磁帶** (60) </span><span class="sxs-lookup"><span data-stu-id="e68df-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 Track Tape** (60)</span></span>


</dt> <dd>

<span data-ttu-id="e68df-247">36-追蹤磁帶</span><span class="sxs-lookup"><span data-stu-id="e68df-247">36-track tape</span></span>

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span data-ttu-id="e68df-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61) </span><span class="sxs-lookup"><span data-stu-id="e68df-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span data-ttu-id="e68df-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**MAGSTAR MP** (62) </span><span class="sxs-lookup"><span data-stu-id="e68df-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span data-ttu-id="e68df-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 磁帶** (63) </span><span class="sxs-lookup"><span data-stu-id="e68df-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 Tape** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span data-ttu-id="e68df-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**磁帶-DST Small** (64) </span><span class="sxs-lookup"><span data-stu-id="e68df-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape - DST Small** (64)</span></span>


</dt> <dd>

<span data-ttu-id="e68df-252">小型磁帶 DST</span><span class="sxs-lookup"><span data-stu-id="e68df-252">Tape   DST small</span></span>

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span data-ttu-id="e68df-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**磁帶-DST 中型** (65) </span><span class="sxs-lookup"><span data-stu-id="e68df-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Tape - DST Medium** (65)</span></span>


</dt> <dd>

<span data-ttu-id="e68df-254">磁帶 DST 媒體</span><span class="sxs-lookup"><span data-stu-id="e68df-254">Tape   DST medium</span></span>

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span data-ttu-id="e68df-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**磁帶-DST 大型** (66) </span><span class="sxs-lookup"><span data-stu-id="e68df-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape - DST Large** (66)</span></span>


</dt> <dd>

<span data-ttu-id="e68df-256">大型磁帶 DST</span><span class="sxs-lookup"><span data-stu-id="e68df-256">Tape   DST large</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e68df-257">**型號**</span><span class="sxs-lookup"><span data-stu-id="e68df-257">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-260">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e68df-260">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-261">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="e68df-261">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="e68df-262">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-263">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e68df-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-266">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="e68df-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-267">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e68df-267">Label by which the object is known.</span></span> <span data-ttu-id="e68df-268">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e68df-268">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e68df-269">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-269">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-270">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e68df-270">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e68df-273">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="e68df-273">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="e68df-274">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="e68df-274">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="e68df-275">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="e68df-275">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="e68df-276">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-276">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-277">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="e68df-277">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-280">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e68df-280">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-281">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="e68df-281">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="e68df-282">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-283">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="e68df-283">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-284">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e68df-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e68df-286">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="e68df-286">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="e68df-287">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-288">**移動**</span><span class="sxs-lookup"><span data-stu-id="e68df-288">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-289">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e68df-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e68df-291">若 **為 TRUE**，則會將這個專案設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="e68df-291">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="e68df-292">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="e68df-292">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="e68df-293">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="e68df-293">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="e68df-294">例如，ungradable 處理器晶片是可移動的。</span><span class="sxs-lookup"><span data-stu-id="e68df-294">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="e68df-295">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-295">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-296">**更換**</span><span class="sxs-lookup"><span data-stu-id="e68df-296">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-297">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e68df-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e68df-299">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="e68df-299">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="e68df-300">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="e68df-300">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="e68df-301">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="e68df-301">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="e68df-302">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="e68df-302">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="e68df-303">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-303">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-304">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e68df-304">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-307">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e68df-307">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-308">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="e68df-308">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="e68df-309">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-309">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-310">**SKU**</span><span class="sxs-lookup"><span data-stu-id="e68df-310">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-313">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e68df-313">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-314">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="e68df-314">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="e68df-315">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-315">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-316">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e68df-316">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-319">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e68df-319">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e68df-320">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e68df-320">Current status of the object.</span></span>

<span data-ttu-id="e68df-321">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e68df-322">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="e68df-322">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e68df-323">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e68df-323">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e68df-324">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-324">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e68df-325">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-325">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e68df-326">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-326">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e68df-327">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-327">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e68df-328">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-328">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e68df-329">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-329">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e68df-330">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-330">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e68df-331">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-331">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e68df-332">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e68df-332">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e68df-333">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-333">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e68df-334">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e68df-334">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e68df-335">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e68df-335">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-338">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e68df-338">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-339">可唯一識別實體元素並作為專案索引鍵的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="e68df-339">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="e68df-340">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="e68df-340">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="e68df-341">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="e68df-341">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="e68df-342">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="e68df-342">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="e68df-343">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="e68df-343">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="e68df-344">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="e68df-344">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="e68df-345">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-345">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-346">**版本**</span><span class="sxs-lookup"><span data-stu-id="e68df-346">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e68df-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e68df-349">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e68df-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e68df-350">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="e68df-350">Version of the physical element.</span></span>

<span data-ttu-id="e68df-351">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-351">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e68df-352">**WriteProtectOn**</span><span class="sxs-lookup"><span data-stu-id="e68df-352">**WriteProtectOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e68df-353">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e68df-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e68df-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e68df-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e68df-355">若 **為 TRUE**，則表示媒體目前是以實體機制寫入保護，例如磁片上的 [保護] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="e68df-355">If **TRUE**, the media is currently write-protected by a physical mechanism, such as a protect tab on a floppy disk.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e68df-356">備註</span><span class="sxs-lookup"><span data-stu-id="e68df-356">Remarks</span></span>

<span data-ttu-id="e68df-357">**Cim \_ PhysicalMedia** 類別衍生自 [**cim \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="e68df-357">The **CIM\_PhysicalMedia** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="e68df-358">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e68df-358">WMI does not implement this class.</span></span>

<span data-ttu-id="e68df-359">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e68df-359">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e68df-360">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e68df-360">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e68df-361">規格需求</span><span class="sxs-lookup"><span data-stu-id="e68df-361">Requirements</span></span>



| <span data-ttu-id="e68df-362">需求</span><span class="sxs-lookup"><span data-stu-id="e68df-362">Requirement</span></span> | <span data-ttu-id="e68df-363">值</span><span class="sxs-lookup"><span data-stu-id="e68df-363">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e68df-364">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e68df-364">Minimum supported client</span></span><br/> | <span data-ttu-id="e68df-365">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e68df-365">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e68df-366">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e68df-366">Minimum supported server</span></span><br/> | <span data-ttu-id="e68df-367">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e68df-367">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e68df-368">命名空間</span><span class="sxs-lookup"><span data-stu-id="e68df-368">Namespace</span></span><br/>                | <span data-ttu-id="e68df-369">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e68df-369">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e68df-370">MOF</span><span class="sxs-lookup"><span data-stu-id="e68df-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e68df-371"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e68df-371"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e68df-372">DLL</span><span class="sxs-lookup"><span data-stu-id="e68df-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e68df-373"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e68df-373"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68df-374">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e68df-374">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68df-375">**CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="e68df-375">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 


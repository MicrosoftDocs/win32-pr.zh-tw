---
description: CIM 位置 \_ 類別代表要插入封裝的連接器。
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: CIM_Slot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468501"
---
# <a name="cim_slot-class"></a><span data-ttu-id="a6e3e-103">CIM \_ 插槽類別</span><span class="sxs-lookup"><span data-stu-id="a6e3e-103">CIM\_Slot class</span></span>

<span data-ttu-id="a6e3e-104">**CIM 位置 \_** 類別代表要插入封裝的連接器。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-104">The **CIM\_Slot** class represents connectors into which packages are inserted.</span></span> <span data-ttu-id="a6e3e-105">例如，您可以將磁片磁碟機的實體封裝插入到 SCA 插槽，或 ([CIM \_ PhysicalPackage](cim-physicalpackage.md) 的子類別，) 可以插入至裝載面板上的16、32或64位擴充位置。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-105">For example, a physical package that is a disk drive can be inserted into an SCA slot, or a card (a subclass of [CIM\_PhysicalPackage](cim-physicalpackage.md)) can be inserted into a 16-, 32-, or 64-bit expansion slot on a hosting board.</span></span> <span data-ttu-id="a6e3e-106">PCI 或 PCMCIA 類型 III 插槽是後者的範例。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-106">PCI or PCMCIA Type III Slots are examples of the latter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6e3e-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a6e3e-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a6e3e-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a6e3e-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e3e-111">語法</span><span class="sxs-lookup"><span data-stu-id="a6e3e-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="a6e3e-112">成員</span><span class="sxs-lookup"><span data-stu-id="a6e3e-112">Members</span></span>

<span data-ttu-id="a6e3e-113">**CIM \_ 插槽** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a6e3e-113">The **CIM\_Slot** class has these types of members:</span></span>

-   [<span data-ttu-id="a6e3e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a6e3e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6e3e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a6e3e-115">Properties</span></span>

<span data-ttu-id="a6e3e-116">**CIM \_ 插槽** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-116">The **CIM\_Slot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6e3e-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-121">Short textual description of the object.</span></span>

<span data-ttu-id="a6e3e-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-123">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-123">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-126">描述 pin 設定的自由格式字串，以及實體連接器的使用信號。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-126">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

<span data-ttu-id="a6e3e-127">這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-127">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-129">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a6e3e-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-131">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ConnectorType" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.2 ") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.2")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-132">實體連接器的類型。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-132">Type of physical connector.</span></span> <span data-ttu-id="a6e3e-133">指定陣列以允許連接器資訊組合的描述。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-133">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="a6e3e-134">例如，一個陣列專案可以指定 RS-232，另一個資料庫-25，第三個則可以將連接器定義為「男性」。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-134">For example, one array entry could specify RS-232, another DB-25, and a third could define the connector as "Male".</span></span>

<span data-ttu-id="a6e3e-135">這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-135">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<dt>

<span data-ttu-id="a6e3e-136">0</span><span class="sxs-lookup"><span data-stu-id="a6e3e-136">0</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-137">Unknown</span><span class="sxs-lookup"><span data-stu-id="a6e3e-137">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-138">1</span><span class="sxs-lookup"><span data-stu-id="a6e3e-138">1</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-139">其他</span><span class="sxs-lookup"><span data-stu-id="a6e3e-139">Other</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-140">2</span><span class="sxs-lookup"><span data-stu-id="a6e3e-140">2</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-141">Male</span><span class="sxs-lookup"><span data-stu-id="a6e3e-141">Male</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-142">3</span><span class="sxs-lookup"><span data-stu-id="a6e3e-142">3</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-143">Female</span><span class="sxs-lookup"><span data-stu-id="a6e3e-143">Female</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-144">4</span><span class="sxs-lookup"><span data-stu-id="a6e3e-144">4</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-145">受防護</span><span class="sxs-lookup"><span data-stu-id="a6e3e-145">Shielded</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-146">5</span><span class="sxs-lookup"><span data-stu-id="a6e3e-146">5</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-147">受防護</span><span class="sxs-lookup"><span data-stu-id="a6e3e-147">Unshielded</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-148">6</span><span class="sxs-lookup"><span data-stu-id="a6e3e-148">6</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-149">SCSI () 高密度 (50 針腳) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-149">SCSI (A) High-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-150">7</span><span class="sxs-lookup"><span data-stu-id="a6e3e-150">7</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-151">SCSI () 低密度 (50 針腳) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-151">SCSI (A) Low-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-152">8</span><span class="sxs-lookup"><span data-stu-id="a6e3e-152">8</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-153">SCSI (P) 高密度 (68 針腳) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-153">SCSI (P) High-density (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-154">9</span><span class="sxs-lookup"><span data-stu-id="a6e3e-154">9</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-155">SCSI SCA-I (80 釘選) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-155">SCSI SCA-I (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-156">10</span><span class="sxs-lookup"><span data-stu-id="a6e3e-156">10</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-157">SCSI SCA-II (80 針腳) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-157">SCSI SCA-II (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-158">11</span><span class="sxs-lookup"><span data-stu-id="a6e3e-158">11</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-159">SCSI 光纖通道 (DB-9、銅) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-159">SCSI Fibre Channel (DB-9, Copper)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-160">12</span><span class="sxs-lookup"><span data-stu-id="a6e3e-160">12</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-161"> (光纖) 的 SCSI 光纖通道</span><span class="sxs-lookup"><span data-stu-id="a6e3e-161">SCSI Fibre Channel (Fibre)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-162">13</span><span class="sxs-lookup"><span data-stu-id="a6e3e-162">13</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-163">SCSI 光纖通道 SCA-II (40 釘選) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-163">SCSI Fibre Channel SCA-II (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-164">14</span><span class="sxs-lookup"><span data-stu-id="a6e3e-164">14</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-165">SCSI 光纖通道 SCA-II (20 個 pin) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-165">SCSI Fibre Channel SCA-II (20 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-166">15</span><span class="sxs-lookup"><span data-stu-id="a6e3e-166">15</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-167">SCSI 光纖通道 BNC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-167">SCSI Fibre Channel BNC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-168">16</span><span class="sxs-lookup"><span data-stu-id="a6e3e-168">16</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-169">ATA 3-1/2 英寸 (40 針腳) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-169">ATA 3-1/2 Inch (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-170">17</span><span class="sxs-lookup"><span data-stu-id="a6e3e-170">17</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-171">ATA 2-1/2 英寸 (44 針腳) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-171">ATA 2-1/2 Inch (44 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-172">18</span><span class="sxs-lookup"><span data-stu-id="a6e3e-172">18</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-173">ATA-2</span><span class="sxs-lookup"><span data-stu-id="a6e3e-173">ATA-2</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-174">19</span><span class="sxs-lookup"><span data-stu-id="a6e3e-174">19</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-175">ATA-3</span><span class="sxs-lookup"><span data-stu-id="a6e3e-175">ATA-3</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-176">20</span><span class="sxs-lookup"><span data-stu-id="a6e3e-176">20</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-177">ATA/66</span><span class="sxs-lookup"><span data-stu-id="a6e3e-177">ATA/66</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-178">21</span><span class="sxs-lookup"><span data-stu-id="a6e3e-178">21</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-179">DB-9</span><span class="sxs-lookup"><span data-stu-id="a6e3e-179">DB-9</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-180">22</span><span class="sxs-lookup"><span data-stu-id="a6e3e-180">22</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-181">DB-15</span><span class="sxs-lookup"><span data-stu-id="a6e3e-181">DB-15</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-182">23</span><span class="sxs-lookup"><span data-stu-id="a6e3e-182">23</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-183">DB-25</span><span class="sxs-lookup"><span data-stu-id="a6e3e-183">DB-25</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-184">24</span><span class="sxs-lookup"><span data-stu-id="a6e3e-184">24</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-185">DB-36</span><span class="sxs-lookup"><span data-stu-id="a6e3e-185">DB-36</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-186">25</span><span class="sxs-lookup"><span data-stu-id="a6e3e-186">25</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-187">RS-232C</span><span class="sxs-lookup"><span data-stu-id="a6e3e-187">RS-232C</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-188">26</span><span class="sxs-lookup"><span data-stu-id="a6e3e-188">26</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-189">RS-422</span><span class="sxs-lookup"><span data-stu-id="a6e3e-189">RS-422</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-190">27</span><span class="sxs-lookup"><span data-stu-id="a6e3e-190">27</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-191">RS-423</span><span class="sxs-lookup"><span data-stu-id="a6e3e-191">RS-423</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-192">28</span><span class="sxs-lookup"><span data-stu-id="a6e3e-192">28</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-193">RS-485</span><span class="sxs-lookup"><span data-stu-id="a6e3e-193">RS-485</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-194">29</span><span class="sxs-lookup"><span data-stu-id="a6e3e-194">29</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-195">RS-449</span><span class="sxs-lookup"><span data-stu-id="a6e3e-195">RS-449</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-196">30</span><span class="sxs-lookup"><span data-stu-id="a6e3e-196">30</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-197">V. 35</span><span class="sxs-lookup"><span data-stu-id="a6e3e-197">V.35</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-198">31</span><span class="sxs-lookup"><span data-stu-id="a6e3e-198">31</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-199">X. 21</span><span class="sxs-lookup"><span data-stu-id="a6e3e-199">X.21</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-200">32</span><span class="sxs-lookup"><span data-stu-id="a6e3e-200">32</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-201">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="a6e3e-201">IEEE-488</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-202">33</span><span class="sxs-lookup"><span data-stu-id="a6e3e-202">33</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-203">AUI</span><span class="sxs-lookup"><span data-stu-id="a6e3e-203">AUI</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-204">34</span><span class="sxs-lookup"><span data-stu-id="a6e3e-204">34</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-205">UTP 類別3</span><span class="sxs-lookup"><span data-stu-id="a6e3e-205">UTP Category 3</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-206">35</span><span class="sxs-lookup"><span data-stu-id="a6e3e-206">35</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-207">UTP 類別4</span><span class="sxs-lookup"><span data-stu-id="a6e3e-207">UTP Category 4</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-208">36</span><span class="sxs-lookup"><span data-stu-id="a6e3e-208">36</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-209">UTP 類別5</span><span class="sxs-lookup"><span data-stu-id="a6e3e-209">UTP Category 5</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-210">37</span><span class="sxs-lookup"><span data-stu-id="a6e3e-210">37</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-211">BNC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-211">BNC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-212">38</span><span class="sxs-lookup"><span data-stu-id="a6e3e-212">38</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-213">RJ11</span><span class="sxs-lookup"><span data-stu-id="a6e3e-213">RJ11</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-214">39</span><span class="sxs-lookup"><span data-stu-id="a6e3e-214">39</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-215">根</span><span class="sxs-lookup"><span data-stu-id="a6e3e-215">RJ45</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-216">40</span><span class="sxs-lookup"><span data-stu-id="a6e3e-216">40</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-217">光纖 MIC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-217">Fiber MIC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-218">41</span><span class="sxs-lookup"><span data-stu-id="a6e3e-218">41</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-219">Apple AUI</span><span class="sxs-lookup"><span data-stu-id="a6e3e-219">Apple AUI</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-220">42</span><span class="sxs-lookup"><span data-stu-id="a6e3e-220">42</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-221">Apple GeoPort</span><span class="sxs-lookup"><span data-stu-id="a6e3e-221">Apple GeoPort</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-222">43</span><span class="sxs-lookup"><span data-stu-id="a6e3e-222">43</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-223">PCI</span><span class="sxs-lookup"><span data-stu-id="a6e3e-223">PCI</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-224">44</span><span class="sxs-lookup"><span data-stu-id="a6e3e-224">44</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-225">ISA</span><span class="sxs-lookup"><span data-stu-id="a6e3e-225">ISA</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-226">45</span><span class="sxs-lookup"><span data-stu-id="a6e3e-226">45</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-227">EISA</span><span class="sxs-lookup"><span data-stu-id="a6e3e-227">EISA</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-228">46</span><span class="sxs-lookup"><span data-stu-id="a6e3e-228">46</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-229">VESA</span><span class="sxs-lookup"><span data-stu-id="a6e3e-229">VESA</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-230">47</span><span class="sxs-lookup"><span data-stu-id="a6e3e-230">47</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-231">Pcmcia</span><span class="sxs-lookup"><span data-stu-id="a6e3e-231">PCMCIA</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-232">48</span><span class="sxs-lookup"><span data-stu-id="a6e3e-232">48</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-233">PCMCIA 類型 I</span><span class="sxs-lookup"><span data-stu-id="a6e3e-233">PCMCIA Type I</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-234">49</span><span class="sxs-lookup"><span data-stu-id="a6e3e-234">49</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-235">PCMCIA 類型 II</span><span class="sxs-lookup"><span data-stu-id="a6e3e-235">PCMCIA Type II</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-236">50</span><span class="sxs-lookup"><span data-stu-id="a6e3e-236">50</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-237">PCMCIA 類型 III</span><span class="sxs-lookup"><span data-stu-id="a6e3e-237">PCMCIA Type III</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-238">51</span><span class="sxs-lookup"><span data-stu-id="a6e3e-238">51</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-239">ZV 埠</span><span class="sxs-lookup"><span data-stu-id="a6e3e-239">ZV Port</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-240">52</span><span class="sxs-lookup"><span data-stu-id="a6e3e-240">52</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-241">CardBus</span><span class="sxs-lookup"><span data-stu-id="a6e3e-241">CardBus</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-242">53</span><span class="sxs-lookup"><span data-stu-id="a6e3e-242">53</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-243">USB</span><span class="sxs-lookup"><span data-stu-id="a6e3e-243">USB</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-244">54</span><span class="sxs-lookup"><span data-stu-id="a6e3e-244">54</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-245">IEEE 1394</span><span class="sxs-lookup"><span data-stu-id="a6e3e-245">IEEE 1394</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-246">55</span><span class="sxs-lookup"><span data-stu-id="a6e3e-246">55</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-247">HIPPI</span><span class="sxs-lookup"><span data-stu-id="a6e3e-247">HIPPI</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-248">56</span><span class="sxs-lookup"><span data-stu-id="a6e3e-248">56</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-249">HSSDC (6 個 pin) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-249">HSSDC (6 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-250">57</span><span class="sxs-lookup"><span data-stu-id="a6e3e-250">57</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-251">GBIC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-251">GBIC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-252">58</span><span class="sxs-lookup"><span data-stu-id="a6e3e-252">58</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-253">DIN</span><span class="sxs-lookup"><span data-stu-id="a6e3e-253">DIN</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-254">59</span><span class="sxs-lookup"><span data-stu-id="a6e3e-254">59</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-255">迷你</span><span class="sxs-lookup"><span data-stu-id="a6e3e-255">Mini-DIN</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-256">60</span><span class="sxs-lookup"><span data-stu-id="a6e3e-256">60</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-257">微型</span><span class="sxs-lookup"><span data-stu-id="a6e3e-257">Micro-DIN</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-258">61</span><span class="sxs-lookup"><span data-stu-id="a6e3e-258">61</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-259">PS/2</span><span class="sxs-lookup"><span data-stu-id="a6e3e-259">PS/2</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-260">62</span><span class="sxs-lookup"><span data-stu-id="a6e3e-260">62</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-261">紅外線</span><span class="sxs-lookup"><span data-stu-id="a6e3e-261">Infrared</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-262">63</span><span class="sxs-lookup"><span data-stu-id="a6e3e-262">63</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-263">HP-HIL</span><span class="sxs-lookup"><span data-stu-id="a6e3e-263">HP-HIL</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-264">64</span><span class="sxs-lookup"><span data-stu-id="a6e3e-264">64</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-265">存取。匯流排</span><span class="sxs-lookup"><span data-stu-id="a6e3e-265">Access.bus</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-266">65</span><span class="sxs-lookup"><span data-stu-id="a6e3e-266">65</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-267">NuBus</span><span class="sxs-lookup"><span data-stu-id="a6e3e-267">NuBus</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-268">66</span><span class="sxs-lookup"><span data-stu-id="a6e3e-268">66</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-269">Centronics</span><span class="sxs-lookup"><span data-stu-id="a6e3e-269">Centronics</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-270">67</span><span class="sxs-lookup"><span data-stu-id="a6e3e-270">67</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-271">Mini-Centronics</span><span class="sxs-lookup"><span data-stu-id="a6e3e-271">Mini-Centronics</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-272">68</span><span class="sxs-lookup"><span data-stu-id="a6e3e-272">68</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-273">Mini-Centronics 類型-14</span><span class="sxs-lookup"><span data-stu-id="a6e3e-273">Mini-Centronics Type-14</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-274">69</span><span class="sxs-lookup"><span data-stu-id="a6e3e-274">69</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-275">Mini-Centronics 類型-20</span><span class="sxs-lookup"><span data-stu-id="a6e3e-275">Mini-Centronics Type-20</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-276">70</span><span class="sxs-lookup"><span data-stu-id="a6e3e-276">70</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-277">Mini-Centronics 類型-26</span><span class="sxs-lookup"><span data-stu-id="a6e3e-277">Mini-Centronics Type-26</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-278">71</span><span class="sxs-lookup"><span data-stu-id="a6e3e-278">71</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-279">匯流排滑鼠</span><span class="sxs-lookup"><span data-stu-id="a6e3e-279">Bus Mouse</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-280">72</span><span class="sxs-lookup"><span data-stu-id="a6e3e-280">72</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-281">亞行</span><span class="sxs-lookup"><span data-stu-id="a6e3e-281">ADB</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-282">73</span><span class="sxs-lookup"><span data-stu-id="a6e3e-282">73</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-283">Agp</span><span class="sxs-lookup"><span data-stu-id="a6e3e-283">AGP</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-284">74</span><span class="sxs-lookup"><span data-stu-id="a6e3e-284">74</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-285">VM 匯流排</span><span class="sxs-lookup"><span data-stu-id="a6e3e-285">VME Bus</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-286">75</span><span class="sxs-lookup"><span data-stu-id="a6e3e-286">75</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-287">VME64</span><span class="sxs-lookup"><span data-stu-id="a6e3e-287">VME64</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-288">76</span><span class="sxs-lookup"><span data-stu-id="a6e3e-288">76</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-289">專屬</span><span class="sxs-lookup"><span data-stu-id="a6e3e-289">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-290">77</span><span class="sxs-lookup"><span data-stu-id="a6e3e-290">77</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-291">專屬處理器卡插槽</span><span class="sxs-lookup"><span data-stu-id="a6e3e-291">Proprietary Processor Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-292">78</span><span class="sxs-lookup"><span data-stu-id="a6e3e-292">78</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-293">專屬記憶卡插槽</span><span class="sxs-lookup"><span data-stu-id="a6e3e-293">Proprietary Memory Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-294">79</span><span class="sxs-lookup"><span data-stu-id="a6e3e-294">79</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-295">專屬的 i/o Riser 插槽</span><span class="sxs-lookup"><span data-stu-id="a6e3e-295">Proprietary I/O Riser Slot</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-296">80</span><span class="sxs-lookup"><span data-stu-id="a6e3e-296">80</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-297">PCI-66MHZ</span><span class="sxs-lookup"><span data-stu-id="a6e3e-297">PCI-66MHZ</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-298">81</span><span class="sxs-lookup"><span data-stu-id="a6e3e-298">81</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-299">AGP2X</span><span class="sxs-lookup"><span data-stu-id="a6e3e-299">AGP2X</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-300">82</span><span class="sxs-lookup"><span data-stu-id="a6e3e-300">82</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-301">AGP4X</span><span class="sxs-lookup"><span data-stu-id="a6e3e-301">AGP4X</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-302">83</span><span class="sxs-lookup"><span data-stu-id="a6e3e-302">83</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-303">電腦-98</span><span class="sxs-lookup"><span data-stu-id="a6e3e-303">PC-98</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-304">84</span><span class="sxs-lookup"><span data-stu-id="a6e3e-304">84</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-305">電腦-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="a6e3e-305">PC-98-Hireso</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-306">85</span><span class="sxs-lookup"><span data-stu-id="a6e3e-306">85</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-307">電腦-H98</span><span class="sxs-lookup"><span data-stu-id="a6e3e-307">PC-H98</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-308">86</span><span class="sxs-lookup"><span data-stu-id="a6e3e-308">86</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-309">電腦-98Note</span><span class="sxs-lookup"><span data-stu-id="a6e3e-309">PC-98Note</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-310">87</span><span class="sxs-lookup"><span data-stu-id="a6e3e-310">87</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-311">電腦-98Full</span><span class="sxs-lookup"><span data-stu-id="a6e3e-311">PC-98Full</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-312">88</span><span class="sxs-lookup"><span data-stu-id="a6e3e-312">88</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-313">SSA SCSI</span><span class="sxs-lookup"><span data-stu-id="a6e3e-313">SSA SCSI</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-314">89</span><span class="sxs-lookup"><span data-stu-id="a6e3e-314">89</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-315">圓形</span><span class="sxs-lookup"><span data-stu-id="a6e3e-315">Circular</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-316">90</span><span class="sxs-lookup"><span data-stu-id="a6e3e-316">90</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-317">面板 IDE 連接器</span><span class="sxs-lookup"><span data-stu-id="a6e3e-317">On Board IDE Connector</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-318">91</span><span class="sxs-lookup"><span data-stu-id="a6e3e-318">91</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-319">在面板上的軟碟連接器</span><span class="sxs-lookup"><span data-stu-id="a6e3e-319">On Board Floppy Connector</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-320">92</span><span class="sxs-lookup"><span data-stu-id="a6e3e-320">92</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-321">9個雙線插換行</span><span class="sxs-lookup"><span data-stu-id="a6e3e-321">9 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-322">93</span><span class="sxs-lookup"><span data-stu-id="a6e3e-322">93</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-323">25個雙內嵌的 Pin</span><span class="sxs-lookup"><span data-stu-id="a6e3e-323">25 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-324">94</span><span class="sxs-lookup"><span data-stu-id="a6e3e-324">94</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-325">50釘選雙重內嵌</span><span class="sxs-lookup"><span data-stu-id="a6e3e-325">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-326">95</span><span class="sxs-lookup"><span data-stu-id="a6e3e-326">95</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-327">68釘選雙重內嵌</span><span class="sxs-lookup"><span data-stu-id="a6e3e-327">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-328">96</span><span class="sxs-lookup"><span data-stu-id="a6e3e-328">96</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-329">面板音效連接器</span><span class="sxs-lookup"><span data-stu-id="a6e3e-329">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-330">97</span><span class="sxs-lookup"><span data-stu-id="a6e3e-330">97</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-331">迷你插口</span><span class="sxs-lookup"><span data-stu-id="a6e3e-331">Mini-jack</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-332">98</span><span class="sxs-lookup"><span data-stu-id="a6e3e-332">98</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-333">PCI X</span><span class="sxs-lookup"><span data-stu-id="a6e3e-333">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-334">99</span><span class="sxs-lookup"><span data-stu-id="a6e3e-334">99</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-335">S 匯流排 IEEE 1396-1993 32 位</span><span class="sxs-lookup"><span data-stu-id="a6e3e-335">Sbus IEEE 1396-1993 32 bit</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-336">100</span><span class="sxs-lookup"><span data-stu-id="a6e3e-336">100</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-337">S 匯流排 IEEE 1396-1993 64 位</span><span class="sxs-lookup"><span data-stu-id="a6e3e-337">Sbus IEEE 1396-1993 64 bit</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-338">101</span><span class="sxs-lookup"><span data-stu-id="a6e3e-338">101</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-339">MCA</span><span class="sxs-lookup"><span data-stu-id="a6e3e-339">MCA</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-340">102</span><span class="sxs-lookup"><span data-stu-id="a6e3e-340">102</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-341">喬</span><span class="sxs-lookup"><span data-stu-id="a6e3e-341">GIO</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-342">103</span><span class="sxs-lookup"><span data-stu-id="a6e3e-342">103</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-343">XIO</span><span class="sxs-lookup"><span data-stu-id="a6e3e-343">XIO</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-344">104</span><span class="sxs-lookup"><span data-stu-id="a6e3e-344">104</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-345">HIO</span><span class="sxs-lookup"><span data-stu-id="a6e3e-345">HIO</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-346">105</span><span class="sxs-lookup"><span data-stu-id="a6e3e-346">105</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-347">NGIO</span><span class="sxs-lookup"><span data-stu-id="a6e3e-347">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-348">106</span><span class="sxs-lookup"><span data-stu-id="a6e3e-348">106</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-349">PMC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-349">PMC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-350">107</span><span class="sxs-lookup"><span data-stu-id="a6e3e-350">107</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-351">MTRJ</span><span class="sxs-lookup"><span data-stu-id="a6e3e-351">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-352">108</span><span class="sxs-lookup"><span data-stu-id="a6e3e-352">108</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-353">VF-45</span><span class="sxs-lookup"><span data-stu-id="a6e3e-353">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-354">109</span><span class="sxs-lookup"><span data-stu-id="a6e3e-354">109</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-355">未來的 i/o</span><span class="sxs-lookup"><span data-stu-id="a6e3e-355">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-356">110</span><span class="sxs-lookup"><span data-stu-id="a6e3e-356">110</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-357">SC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-357">SC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-358">111</span><span class="sxs-lookup"><span data-stu-id="a6e3e-358">111</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-359">SG</span><span class="sxs-lookup"><span data-stu-id="a6e3e-359">SG</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-360">112</span><span class="sxs-lookup"><span data-stu-id="a6e3e-360">112</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-361">電子</span><span class="sxs-lookup"><span data-stu-id="a6e3e-361">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-362">113</span><span class="sxs-lookup"><span data-stu-id="a6e3e-362">113</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-363">光學</span><span class="sxs-lookup"><span data-stu-id="a6e3e-363">Optical</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-364">114</span><span class="sxs-lookup"><span data-stu-id="a6e3e-364">114</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-365">功能區</span><span class="sxs-lookup"><span data-stu-id="a6e3e-365">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-366">115</span><span class="sxs-lookup"><span data-stu-id="a6e3e-366">115</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-367">GLM</span><span class="sxs-lookup"><span data-stu-id="a6e3e-367">GLM</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-368">116</span><span class="sxs-lookup"><span data-stu-id="a6e3e-368">116</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-369">1x9</span><span class="sxs-lookup"><span data-stu-id="a6e3e-369">1x9</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-370">117</span><span class="sxs-lookup"><span data-stu-id="a6e3e-370">117</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-371">小 SG</span><span class="sxs-lookup"><span data-stu-id="a6e3e-371">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-372">118</span><span class="sxs-lookup"><span data-stu-id="a6e3e-372">118</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-373">LC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-373">LC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-374">119</span><span class="sxs-lookup"><span data-stu-id="a6e3e-374">119</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-375">HSSC</span><span class="sxs-lookup"><span data-stu-id="a6e3e-375">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-376">120</span><span class="sxs-lookup"><span data-stu-id="a6e3e-376">120</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-377">VHDCI 防護 (68 pin) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-377">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-378">121</span><span class="sxs-lookup"><span data-stu-id="a6e3e-378">121</span></span>
</dt> <dd>

<span data-ttu-id="a6e3e-379">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="a6e3e-379">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a6e3e-380">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-380">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-383">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-383">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-384">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-384">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a6e3e-385">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-385">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a6e3e-386">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-386">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-387">**說明**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-387">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-390">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-390">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-391">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-391">Textual description of the object.</span></span>

<span data-ttu-id="a6e3e-392">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-393">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-393">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-394">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-394">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-396">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-397">可插入至插槽的介面卡卡片最大高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-397">Maximum height, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-398">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-398">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-399">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-401">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-402">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-402">Date and time the object was installed.</span></span> <span data-ttu-id="a6e3e-403">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-403">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a6e3e-404">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-405">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-405">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-406">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-406">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-408">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-408">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-409">可以插入至插槽的介面卡卡片最大長度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-409">Maximum length, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-410">**製造商**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-410">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-411">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-413">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-413">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-414">產生實體元素的組織。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-414">Organization that produced the physical element.</span></span> <span data-ttu-id="a6e3e-415">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-415">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="a6e3e-416">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-416">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-417">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-417">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-418">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-420">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.3 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 位 ") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-421">可以插入至插槽的介面卡的最大匯流排寬度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-421">Maximum bus width, in bits, of adapter cards that can be inserted into the slot.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="a6e3e-422">**8** (0) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-422">**8** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="a6e3e-423">**16** (1) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-423">**16** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="a6e3e-424">**32** (2) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-424">**32** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="64"></span>

<span data-ttu-id="a6e3e-425">**64** (3) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-425">**64** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="128"></span>

<span data-ttu-id="a6e3e-426">**128** (4) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-426">**128** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6e3e-427">**型號**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-427">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-428">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-430">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-431">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-431">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="a6e3e-432">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-432">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-433">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-433">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-436">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-436">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-437">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-437">Label by which the object is known.</span></span> <span data-ttu-id="a6e3e-438">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-438">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a6e3e-439">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-440">**Number**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-440">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-441">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-443">實體位置編號，可用來做為系統位置資料表的索引，以判斷位置是否實際被佔用。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-443">Physical slot number, which can be used as an index into a system slot table, to determine whether the slot is physically occupied.</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-444">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-444">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-447">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-447">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="a6e3e-448">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-448">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="a6e3e-449">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-449">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="a6e3e-450">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-450">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-451">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-451">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-452">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-454">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-454">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-455">由產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-455">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="a6e3e-456">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-456">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-457">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-457">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-458">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-460">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-460">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="a6e3e-461">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-461">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-462">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-462">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-464">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-465">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_** 位置」。**SpecialPurpose**") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-465">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-466">描述此位置實際是唯一的，且可能保存特殊硬體類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-466">Free-form string that describes how this slot is physically unique and that it may hold special types of hardware.</span></span> <span data-ttu-id="a6e3e-467">只有當對應的布林 **SpecialPurpose** 屬性設定為 **TRUE** 時，這個屬性才有意義。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-467">This property only has meaning when the corresponding Boolean **SpecialPurpose** property is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-468">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-468">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-471">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-471">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-472">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-472">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="a6e3e-473">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-473">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-474">**SKU**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-474">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-476">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-477">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-478">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-478">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="a6e3e-479">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-479">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-480">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-480">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-481">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-481">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-483">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_** 位置」。**PurposeDescription**") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-483">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-484">若 **為 TRUE**，則位置實際上是唯一的，而且可能保存特殊類型的硬體， (例如，圖形處理器插槽) 。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-484">If **TRUE**, the slot is physically unique and may hold special types of hardware, (for example, a graphics processor slot).</span></span> <span data-ttu-id="a6e3e-485">若 **為 TRUE**， **PurposeDescription** 屬性應該指定位置是唯一的，還是位置的用途。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-485">If **TRUE**, the **PurposeDescription** property should specify how the slot is unique or the slot's purpose.</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-486">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-486">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-489">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-489">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-490">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-490">Current status of the object.</span></span> <span data-ttu-id="a6e3e-491">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-491">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a6e3e-492">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="a6e3e-492">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a6e3e-493">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-493">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a6e3e-494">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-494">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a6e3e-495">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-495">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6e3e-496">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-496">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a6e3e-497">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-497">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a6e3e-498">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-498">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a6e3e-499">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-499">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a6e3e-500">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-500">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a6e3e-501">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-501">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a6e3e-502">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-502">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a6e3e-503">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-503">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a6e3e-504">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-504">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6e3e-505">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-505">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-506">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-506">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-508">若 **為 TRUE**，則位置支援介面卡的熱插即用。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-508">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-509">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-509">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-510">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-511">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-512">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-512">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-513">可唯一識別實體元素並作為專案索引鍵的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-513">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="a6e3e-514">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-514">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="a6e3e-515">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中非常高的位置，以獨立識別硬體/實體，無論 (或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-515">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="a6e3e-516">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-516">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="a6e3e-517">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-517">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="a6e3e-518">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-518">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="a6e3e-519">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-519">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-520">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-520">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-521">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-522">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-523">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫瓦 ") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-524">插槽的最高散熱量（以毫瓦）。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-524">Maximum thermal dissipation of the slot, in milliwatts.</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-525">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-525">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-526">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a6e3e-526">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-527">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-528">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.9 ") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-528">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-529">插槽所支援的 Vcc 電壓。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-529">Vcc voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6e3e-530">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-530">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a6e3e-531">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-531">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="a6e3e-532">**3.3 v** (2) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-532">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="a6e3e-533">**5v** (3) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-533">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6e3e-534">**版本**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-534">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-536">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-537">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-537">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-538">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-538">Version of the physical element.</span></span>

<span data-ttu-id="a6e3e-539">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-539">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e3e-540">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-540">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e3e-541">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a6e3e-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-542">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a6e3e-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e3e-543">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.10 ") </span><span class="sxs-lookup"><span data-stu-id="a6e3e-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="a6e3e-544">插槽所支援的 Vpp 電壓。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-544">Vpp voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6e3e-545">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-545">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a6e3e-546">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-546">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="a6e3e-547">**3.3 v** (2) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-547">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="a6e3e-548">**5v** (3) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-548">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="a6e3e-549">**12v** (4) </span><span class="sxs-lookup"><span data-stu-id="a6e3e-549">**12V** (4)</span></span>


<span data-ttu-id="a6e3e-550"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a6e3e-550"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a6e3e-551">備註</span><span class="sxs-lookup"><span data-stu-id="a6e3e-551">Remarks</span></span>

<span data-ttu-id="a6e3e-552">**Cim \_ 插槽** 類別衍生自 [**cim \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-552">The **CIM\_Slot** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="a6e3e-553">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-553">WMI does not implement this class.</span></span> <span data-ttu-id="a6e3e-554">針對衍生自 CIM 位置 **的 \_ WMI 類別**，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-554">For WMI classes derived from **CIM\_Slot**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a6e3e-555">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a6e3e-556">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a6e3e-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e3e-557">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6e3e-557">Requirements</span></span>



| <span data-ttu-id="a6e3e-558">需求</span><span class="sxs-lookup"><span data-stu-id="a6e3e-558">Requirement</span></span> | <span data-ttu-id="a6e3e-559">值</span><span class="sxs-lookup"><span data-stu-id="a6e3e-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e3e-560">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6e3e-560">Minimum supported client</span></span><br/> | <span data-ttu-id="a6e3e-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6e3e-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6e3e-562">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6e3e-562">Minimum supported server</span></span><br/> | <span data-ttu-id="a6e3e-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6e3e-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6e3e-564">命名空間</span><span class="sxs-lookup"><span data-stu-id="a6e3e-564">Namespace</span></span><br/>                | <span data-ttu-id="a6e3e-565">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a6e3e-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a6e3e-566">MOF</span><span class="sxs-lookup"><span data-stu-id="a6e3e-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6e3e-567"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6e3e-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6e3e-568">DLL</span><span class="sxs-lookup"><span data-stu-id="a6e3e-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6e3e-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6e3e-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6e3e-570">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6e3e-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6e3e-571">**CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="a6e3e-571">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> </dl>

 


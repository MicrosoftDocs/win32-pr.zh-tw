---
description: CIM \_ PhysicalConnector 類別代表用來連接到其他元素的任何實體元素。 任何可以連接及傳輸兩個或多個實體元素之間的信號或電源的物件，都是此類別的子系 (或成員) 。
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: CIM_PhysicalConnector 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 106b8ab30296b77be550809771db3b0208485872
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972779"
---
# <a name="cim_physicalconnector-class"></a><span data-ttu-id="bab27-104">CIM \_ PhysicalConnector 類別</span><span class="sxs-lookup"><span data-stu-id="bab27-104">CIM\_PhysicalConnector class</span></span>

<span data-ttu-id="bab27-105">**CIM \_ PhysicalConnector** 類別代表用來連接到其他元素的任何實體元素。</span><span class="sxs-lookup"><span data-stu-id="bab27-105">The **CIM\_PhysicalConnector** class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="bab27-106">任何可以連接及傳輸兩個或多個實體元素之間的信號或電源的物件，都是此類別的子系 (或成員) 。</span><span class="sxs-lookup"><span data-stu-id="bab27-106">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span> <span data-ttu-id="bab27-107">例如，插槽和 D shell 連接器是實體連接器的類型。</span><span class="sxs-lookup"><span data-stu-id="bab27-107">For example, slots and D-shell connectors are types of physical connectors.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bab27-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="bab27-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bab27-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="bab27-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bab27-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bab27-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bab27-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bab27-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab27-112">語法</span><span class="sxs-lookup"><span data-stu-id="bab27-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
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
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a><span data-ttu-id="bab27-113">成員</span><span class="sxs-lookup"><span data-stu-id="bab27-113">Members</span></span>

<span data-ttu-id="bab27-114">**CIM \_ PhysicalConnector** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bab27-114">The **CIM\_PhysicalConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="bab27-115">屬性</span><span class="sxs-lookup"><span data-stu-id="bab27-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bab27-116">屬性</span><span class="sxs-lookup"><span data-stu-id="bab27-116">Properties</span></span>

<span data-ttu-id="bab27-117">**CIM \_ PhysicalConnector** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bab27-117">The **CIM\_PhysicalConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bab27-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="bab27-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="bab27-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bab27-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="bab27-122">A short textual description of the object.</span></span>

<span data-ttu-id="bab27-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-124">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="bab27-124">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab27-127">描述 pin 設定的自由格式字串，以及實體連接器的使用信號。</span><span class="sxs-lookup"><span data-stu-id="bab27-127">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

</dd> <dt>

<span data-ttu-id="bab27-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="bab27-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-129">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bab27-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bab27-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab27-131">實體連接器的類型。</span><span class="sxs-lookup"><span data-stu-id="bab27-131">Type of physical connector.</span></span> <span data-ttu-id="bab27-132">指定陣列以允許連接器資訊組合的描述。</span><span class="sxs-lookup"><span data-stu-id="bab27-132">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="bab27-133">例如，一個陣列專案可以指定 RS-232、另一個資料庫-25 和第三個專案可以將連接器定義為「男性」。</span><span class="sxs-lookup"><span data-stu-id="bab27-133">For example, one array entry could specify RS-232, another DB-25, and a third entry could define the connector as "male".</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bab27-134">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="bab27-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bab27-135">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="bab27-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="bab27-136">**男性** (2) </span><span class="sxs-lookup"><span data-stu-id="bab27-136">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="bab27-137">**女性** (3) </span><span class="sxs-lookup"><span data-stu-id="bab27-137">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="bab27-138">**受防護** 的 (4) </span><span class="sxs-lookup"><span data-stu-id="bab27-138">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="bab27-139">非 **遮罩** (5) </span><span class="sxs-lookup"><span data-stu-id="bab27-139">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="bab27-140">**SCSI () High-Density (50 針腳)** (6) </span><span class="sxs-lookup"><span data-stu-id="bab27-140">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="bab27-141">**SCSI () Low-Density (50 針腳)** (7) </span><span class="sxs-lookup"><span data-stu-id="bab27-141">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="bab27-142">**SCSI (P) High-Density (68 針腳)** (8) </span><span class="sxs-lookup"><span data-stu-id="bab27-142">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="bab27-143">**SCSI SCA-I (80 針腳)** (9) </span><span class="sxs-lookup"><span data-stu-id="bab27-143">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="bab27-144">**SCSI SCA-II (80 針腳)** (10) </span><span class="sxs-lookup"><span data-stu-id="bab27-144">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="bab27-145">**SCSI 光纖通道 (DB-9、銅)** (11) </span><span class="sxs-lookup"><span data-stu-id="bab27-145">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="bab27-146">**SCSI 光纖通道 (光纖)** (12) </span><span class="sxs-lookup"><span data-stu-id="bab27-146">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="bab27-147">**SCSI 光纖通道 SCA-II (40 針腳)** (13) </span><span class="sxs-lookup"><span data-stu-id="bab27-147">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="bab27-148">**SCSI 光纖通道 SCA-II (20 部 pin)** (14) </span><span class="sxs-lookup"><span data-stu-id="bab27-148">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="bab27-149">**SCSI 光纖通道 BNC** (15) </span><span class="sxs-lookup"><span data-stu-id="bab27-149">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="bab27-150">**ATA 3-1/2 英寸 (40 針腳)** (16) </span><span class="sxs-lookup"><span data-stu-id="bab27-150">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="bab27-151">**ATA 2-1/2 英寸 (44 針腳)** (17) </span><span class="sxs-lookup"><span data-stu-id="bab27-151">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="bab27-152">**ATA-2** (18) </span><span class="sxs-lookup"><span data-stu-id="bab27-152">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="bab27-153">**ATA-3** (19) </span><span class="sxs-lookup"><span data-stu-id="bab27-153">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="bab27-154">**ATA/66** (20) </span><span class="sxs-lookup"><span data-stu-id="bab27-154">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="bab27-155">**Db-library** (21) </span><span class="sxs-lookup"><span data-stu-id="bab27-155">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="bab27-156">**DB-15** (22) </span><span class="sxs-lookup"><span data-stu-id="bab27-156">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="bab27-157">**DB-25** (23) </span><span class="sxs-lookup"><span data-stu-id="bab27-157">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="bab27-158">**DB-36** (24) </span><span class="sxs-lookup"><span data-stu-id="bab27-158">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="bab27-159">**Rs-232c** (25) </span><span class="sxs-lookup"><span data-stu-id="bab27-159">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="bab27-160">**RS-422** (26) </span><span class="sxs-lookup"><span data-stu-id="bab27-160">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="bab27-161">**RS-423** (27) </span><span class="sxs-lookup"><span data-stu-id="bab27-161">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="bab27-162">**RS-485** (28) </span><span class="sxs-lookup"><span data-stu-id="bab27-162">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="bab27-163">**RS-449** (29) </span><span class="sxs-lookup"><span data-stu-id="bab27-163">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="bab27-164">**V. 35** (30) </span><span class="sxs-lookup"><span data-stu-id="bab27-164">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="bab27-165">**X. 21** (31) </span><span class="sxs-lookup"><span data-stu-id="bab27-165">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="bab27-166">**IEEE-488** (32) </span><span class="sxs-lookup"><span data-stu-id="bab27-166">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="bab27-167">**AUI** (33) </span><span class="sxs-lookup"><span data-stu-id="bab27-167">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="bab27-168">**UTP 類別 3** (34) </span><span class="sxs-lookup"><span data-stu-id="bab27-168">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="bab27-169">**UTP 類別 4** (35) </span><span class="sxs-lookup"><span data-stu-id="bab27-169">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="bab27-170">**UTP 類別 5** (36) </span><span class="sxs-lookup"><span data-stu-id="bab27-170">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="bab27-171">**BNC** (37) </span><span class="sxs-lookup"><span data-stu-id="bab27-171">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="bab27-172">**RJ11** (38) </span><span class="sxs-lookup"><span data-stu-id="bab27-172">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="bab27-173">**RJ45** (39) </span><span class="sxs-lookup"><span data-stu-id="bab27-173">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="bab27-174">**光纖 MIC** (40) </span><span class="sxs-lookup"><span data-stu-id="bab27-174">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="bab27-175">**APPLE AUI** (41) </span><span class="sxs-lookup"><span data-stu-id="bab27-175">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="bab27-176">**Apple GeoPort** (42) </span><span class="sxs-lookup"><span data-stu-id="bab27-176">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="bab27-177">**PCI** (43) </span><span class="sxs-lookup"><span data-stu-id="bab27-177">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="bab27-178">**ISA** (44) </span><span class="sxs-lookup"><span data-stu-id="bab27-178">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="bab27-179">**EISA** (45) </span><span class="sxs-lookup"><span data-stu-id="bab27-179">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="bab27-180">**VESA** (46) </span><span class="sxs-lookup"><span data-stu-id="bab27-180">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="bab27-181">**PCMCIA** (47) </span><span class="sxs-lookup"><span data-stu-id="bab27-181">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="bab27-182">**PCMCIA 類型 I** (48) </span><span class="sxs-lookup"><span data-stu-id="bab27-182">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="bab27-183">**PCMCIA 類型 II** (49) </span><span class="sxs-lookup"><span data-stu-id="bab27-183">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="bab27-184">**PCMCIA 類型 III** (50) </span><span class="sxs-lookup"><span data-stu-id="bab27-184">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="bab27-185">**ZV 埠** (51) </span><span class="sxs-lookup"><span data-stu-id="bab27-185">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="bab27-186">**CardBus** (52) </span><span class="sxs-lookup"><span data-stu-id="bab27-186">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="bab27-187">**USB** (53) </span><span class="sxs-lookup"><span data-stu-id="bab27-187">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="bab27-188">**IEEE 1394** (54) </span><span class="sxs-lookup"><span data-stu-id="bab27-188">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="bab27-189">**HIPPI** (55) </span><span class="sxs-lookup"><span data-stu-id="bab27-189">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="bab27-190">**HSSDC (6 針腳)** (56) </span><span class="sxs-lookup"><span data-stu-id="bab27-190">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="bab27-191">**GBIC** (57) </span><span class="sxs-lookup"><span data-stu-id="bab27-191">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="bab27-192">**(58**) </span><span class="sxs-lookup"><span data-stu-id="bab27-192">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="bab27-193">**迷你** 等 (59) </span><span class="sxs-lookup"><span data-stu-id="bab27-193">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="bab27-194">**微型** (60) </span><span class="sxs-lookup"><span data-stu-id="bab27-194">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="bab27-195">**PS/2** (61) </span><span class="sxs-lookup"><span data-stu-id="bab27-195">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="bab27-196">**紅外線** (62) </span><span class="sxs-lookup"><span data-stu-id="bab27-196">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="bab27-197">**HP HIL** (63) </span><span class="sxs-lookup"><span data-stu-id="bab27-197">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="bab27-198">**存取. bus** (64) </span><span class="sxs-lookup"><span data-stu-id="bab27-198">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="bab27-199">**NuBus** (65) </span><span class="sxs-lookup"><span data-stu-id="bab27-199">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="bab27-200">**Centronics** (66) </span><span class="sxs-lookup"><span data-stu-id="bab27-200">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="bab27-201">**迷你 Centronics** (67) </span><span class="sxs-lookup"><span data-stu-id="bab27-201">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="bab27-202">**迷你 Centronics 類型-14** (68) </span><span class="sxs-lookup"><span data-stu-id="bab27-202">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="bab27-203">**迷你 Centronics 類型-20** (69) </span><span class="sxs-lookup"><span data-stu-id="bab27-203">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="bab27-204">**迷你 Centronics 類型-26** (70) </span><span class="sxs-lookup"><span data-stu-id="bab27-204">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="bab27-205">**匯流排滑鼠** (71) </span><span class="sxs-lookup"><span data-stu-id="bab27-205">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="bab27-206">**ADB** (72) </span><span class="sxs-lookup"><span data-stu-id="bab27-206">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="bab27-207">**AGP** (73) </span><span class="sxs-lookup"><span data-stu-id="bab27-207">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="bab27-208">**Vm 匯流排** (74) </span><span class="sxs-lookup"><span data-stu-id="bab27-208">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="bab27-209">**VME64** (75) </span><span class="sxs-lookup"><span data-stu-id="bab27-209">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="bab27-210">**專屬** (76) </span><span class="sxs-lookup"><span data-stu-id="bab27-210">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="bab27-211">**專屬處理器卡插槽** (77) </span><span class="sxs-lookup"><span data-stu-id="bab27-211">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="bab27-212">**專屬記憶卡插槽** (78) </span><span class="sxs-lookup"><span data-stu-id="bab27-212">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="bab27-213">**專屬 I/o Riser 卡插槽** (79) </span><span class="sxs-lookup"><span data-stu-id="bab27-213">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="bab27-214">**PCI-66MHZ** (80) </span><span class="sxs-lookup"><span data-stu-id="bab27-214">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="bab27-215">**AGP2X** (81) </span><span class="sxs-lookup"><span data-stu-id="bab27-215">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="bab27-216">**AGP4X** (82) </span><span class="sxs-lookup"><span data-stu-id="bab27-216">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="bab27-217">**PC-98** (83) </span><span class="sxs-lookup"><span data-stu-id="bab27-217">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="bab27-218">**PC-98-Hireso** (84) </span><span class="sxs-lookup"><span data-stu-id="bab27-218">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="bab27-219">**PC-H98** (85) </span><span class="sxs-lookup"><span data-stu-id="bab27-219">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="bab27-220">**PC-98Note** (86) </span><span class="sxs-lookup"><span data-stu-id="bab27-220">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="bab27-221">**PC-98Full** (87) </span><span class="sxs-lookup"><span data-stu-id="bab27-221">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="bab27-222">**SSA SCSI** (88) </span><span class="sxs-lookup"><span data-stu-id="bab27-222">**SSA SCSI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

<span data-ttu-id="bab27-223">**迴圈** (89) </span><span class="sxs-lookup"><span data-stu-id="bab27-223">**Circular** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

<span data-ttu-id="bab27-224">**On 面板 IDE 連接器** (90) </span><span class="sxs-lookup"><span data-stu-id="bab27-224">**On Board IDE Connector** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

<span data-ttu-id="bab27-225">**在主機板軟盤機上** (91) </span><span class="sxs-lookup"><span data-stu-id="bab27-225">**On Board Floppy Connector** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bab27-226">**9 釘選雙重內嵌** (92) </span><span class="sxs-lookup"><span data-stu-id="bab27-226">**9 Pin Dual Inline** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bab27-227">**25 個 Pin 雙內嵌** (93) </span><span class="sxs-lookup"><span data-stu-id="bab27-227">**25 Pin Dual Inline** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bab27-228">**50 釘選雙重內嵌** (94) </span><span class="sxs-lookup"><span data-stu-id="bab27-228">**50 Pin Dual Inline** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bab27-229">**68 釘選雙重內嵌** (95) </span><span class="sxs-lookup"><span data-stu-id="bab27-229">**68 Pin Dual Inline** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

<span data-ttu-id="bab27-230">**面板音效連接器** (96) </span><span class="sxs-lookup"><span data-stu-id="bab27-230">**On Board Sound Connector** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="bab27-231">**迷你插座** (97) </span><span class="sxs-lookup"><span data-stu-id="bab27-231">**Mini-jack** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="bab27-232">**PCI-X** (98) </span><span class="sxs-lookup"><span data-stu-id="bab27-232">**PCI-X** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="bab27-233">**S 匯流排 IEEE 1396-1993 32 位** (99) </span><span class="sxs-lookup"><span data-stu-id="bab27-233">**Sbus IEEE 1396-1993 32 bit** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="bab27-234">**S 匯流排 IEEE 1396-1993 64 位** (100) </span><span class="sxs-lookup"><span data-stu-id="bab27-234">**Sbus IEEE 1396-1993 64 bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="bab27-235">**MCA** (101) </span><span class="sxs-lookup"><span data-stu-id="bab27-235">**MCA** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="bab27-236">**GIO** (102) </span><span class="sxs-lookup"><span data-stu-id="bab27-236">**GIO** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="bab27-237">**XIO** (103) </span><span class="sxs-lookup"><span data-stu-id="bab27-237">**XIO** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="bab27-238">**HIO** (104) </span><span class="sxs-lookup"><span data-stu-id="bab27-238">**HIO** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="bab27-239">**NGIO** (105) </span><span class="sxs-lookup"><span data-stu-id="bab27-239">**NGIO** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="bab27-240">**PMC** (106) </span><span class="sxs-lookup"><span data-stu-id="bab27-240">**PMC** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

<span data-ttu-id="bab27-241">**MTRJ** (107) </span><span class="sxs-lookup"><span data-stu-id="bab27-241">**MTRJ** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

<span data-ttu-id="bab27-242">**VF-45** (108) </span><span class="sxs-lookup"><span data-stu-id="bab27-242">**VF-45** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="bab27-243">**未來的 i/o** (109) </span><span class="sxs-lookup"><span data-stu-id="bab27-243">**Future I/O** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

<span data-ttu-id="bab27-244">**SC** (110) </span><span class="sxs-lookup"><span data-stu-id="bab27-244">**SC** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

<span data-ttu-id="bab27-245">**SG** (111) </span><span class="sxs-lookup"><span data-stu-id="bab27-245">**SG** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

<span data-ttu-id="bab27-246">**電** (112) </span><span class="sxs-lookup"><span data-stu-id="bab27-246">**Electrical** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

<span data-ttu-id="bab27-247">**光學** (113) </span><span class="sxs-lookup"><span data-stu-id="bab27-247">**Optical** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

<span data-ttu-id="bab27-248">**功能區** (114) </span><span class="sxs-lookup"><span data-stu-id="bab27-248">**Ribbon** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

<span data-ttu-id="bab27-249">**GLM** (115) </span><span class="sxs-lookup"><span data-stu-id="bab27-249">**GLM** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

<span data-ttu-id="bab27-250">**1x9** (116) </span><span class="sxs-lookup"><span data-stu-id="bab27-250">**1x9** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

<span data-ttu-id="bab27-251"> (117) 的 **最小 SG**</span><span class="sxs-lookup"><span data-stu-id="bab27-251">**Mini SG** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

<span data-ttu-id="bab27-252">**LC** (118) </span><span class="sxs-lookup"><span data-stu-id="bab27-252">**LC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

<span data-ttu-id="bab27-253">**HSSC** (119) </span><span class="sxs-lookup"><span data-stu-id="bab27-253">**HSSC** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

<span data-ttu-id="bab27-254">**VHDCI 防護 (68 pin)** (120) </span><span class="sxs-lookup"><span data-stu-id="bab27-254">**VHDCI Shielded (68 pins)** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="bab27-255">**(121**) 的不限</span><span class="sxs-lookup"><span data-stu-id="bab27-255">**InfiniBand** (121)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bab27-256">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bab27-256">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-259">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="bab27-259">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-260">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="bab27-260">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bab27-261">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="bab27-261">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bab27-262">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-263">**說明**</span><span class="sxs-lookup"><span data-stu-id="bab27-263">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-266">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="bab27-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bab27-267">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="bab27-267">A textual description of the object.</span></span>

<span data-ttu-id="bab27-268">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-268">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-269">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bab27-269">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-270">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="bab27-270">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-272">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="bab27-272">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bab27-273">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="bab27-273">Indicates when the object was installed.</span></span> <span data-ttu-id="bab27-274">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="bab27-274">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bab27-275">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-276">**製造商**</span><span class="sxs-lookup"><span data-stu-id="bab27-276">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-277">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-279">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="bab27-279">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-280">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="bab27-280">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="bab27-281">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bab27-281">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="bab27-282">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-283">**型號**</span><span class="sxs-lookup"><span data-stu-id="bab27-283">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-286">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="bab27-286">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-287">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="bab27-287">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="bab27-288">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-288">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-289">**名稱**</span><span class="sxs-lookup"><span data-stu-id="bab27-289">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-290">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-292">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="bab27-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bab27-293">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="bab27-293">Label by which the object is known.</span></span> <span data-ttu-id="bab27-294">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="bab27-294">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="bab27-295">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-296">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="bab27-296">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab27-299">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="bab27-299">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="bab27-300">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="bab27-300">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="bab27-301">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="bab27-301">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="bab27-302">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-303">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="bab27-303">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-306">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="bab27-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-307">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="bab27-307">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="bab27-308">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-308">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-309">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="bab27-309">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-310">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bab27-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab27-312">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="bab27-312">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="bab27-313">否則，它目前為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="bab27-313">Otherwise, it is currently off.</span></span>

<span data-ttu-id="bab27-314">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-315">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="bab27-315">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-318">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="bab27-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-319">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="bab27-319">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="bab27-320">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-321">**SKU**</span><span class="sxs-lookup"><span data-stu-id="bab27-321">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-324">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="bab27-324">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-325">此實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="bab27-325">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="bab27-326">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-327">**狀態**</span><span class="sxs-lookup"><span data-stu-id="bab27-327">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-330">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="bab27-330">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bab27-331">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="bab27-331">String that indicates the current status of the object.</span></span> <span data-ttu-id="bab27-332">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="bab27-332">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="bab27-333">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="bab27-333">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="bab27-334">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="bab27-334">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="bab27-335">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="bab27-335">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bab27-336">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="bab27-336">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bab27-337">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="bab27-337">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bab27-338">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bab27-339">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="bab27-339">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bab27-340">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="bab27-340">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bab27-341">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-341">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bab27-342">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-342">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bab27-343">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-343">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bab27-344">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-344">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bab27-345">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-345">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bab27-346">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-346">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bab27-347">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-347">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bab27-348">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-348">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bab27-349">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="bab27-349">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bab27-350">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-350">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bab27-351">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="bab27-351">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bab27-352">**Tag**</span><span class="sxs-lookup"><span data-stu-id="bab27-352">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-355">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="bab27-355">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-356">可唯一識別實體元素，並作為專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="bab27-356">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="bab27-357">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="bab27-357">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="bab27-358">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="bab27-358">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="bab27-359">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="bab27-359">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="bab27-360">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="bab27-360">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="bab27-361">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="bab27-361">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="bab27-362">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-362">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab27-363">**版本**</span><span class="sxs-lookup"><span data-stu-id="bab27-363">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab27-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bab27-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab27-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bab27-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab27-366">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="bab27-366">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bab27-367">指出實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="bab27-367">Indicates the version of the physical element.</span></span>

<span data-ttu-id="bab27-368">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-368">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bab27-369">備註</span><span class="sxs-lookup"><span data-stu-id="bab27-369">Remarks</span></span>

<span data-ttu-id="bab27-370">**Cim \_ PhysicalConnector** 類別衍生自 [**cim \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-370">The **CIM\_PhysicalConnector** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="bab27-371">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="bab27-371">WMI does not implement this class.</span></span> <span data-ttu-id="bab27-372">針對衍生自 **CIM \_ PHYSICALCONNECTOR** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="bab27-372">For WMI classes that are derived from **CIM\_PhysicalConnector**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bab27-373">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="bab27-373">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bab27-374">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bab27-374">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bab27-375">規格需求</span><span class="sxs-lookup"><span data-stu-id="bab27-375">Requirements</span></span>



| <span data-ttu-id="bab27-376">需求</span><span class="sxs-lookup"><span data-stu-id="bab27-376">Requirement</span></span> | <span data-ttu-id="bab27-377">值</span><span class="sxs-lookup"><span data-stu-id="bab27-377">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bab27-378">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bab27-378">Minimum supported client</span></span><br/> | <span data-ttu-id="bab27-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bab27-379">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bab27-380">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bab27-380">Minimum supported server</span></span><br/> | <span data-ttu-id="bab27-381">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bab27-381">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bab27-382">命名空間</span><span class="sxs-lookup"><span data-stu-id="bab27-382">Namespace</span></span><br/>                | <span data-ttu-id="bab27-383">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bab27-383">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bab27-384">MOF</span><span class="sxs-lookup"><span data-stu-id="bab27-384">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bab27-385"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bab27-385"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bab27-386">DLL</span><span class="sxs-lookup"><span data-stu-id="bab27-386">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bab27-387"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab27-387"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab27-388">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bab27-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab27-389">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="bab27-389">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 


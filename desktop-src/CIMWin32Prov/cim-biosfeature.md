---
description: 代表用來啟動及設定電腦系統的低層級軟體的功能。
ms.assetid: 54d03539-d908-4571-b8fd-934b972e8d84
ms.tgt_platform: multiple
title: CIM_BIOSFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeature
- CIM_BIOSFeature.Caption
- CIM_BIOSFeature.Description
- CIM_BIOSFeature.InstallDate
- CIM_BIOSFeature.Status
- CIM_BIOSFeature.IdentifyingNumber
- CIM_BIOSFeature.ProductName
- CIM_BIOSFeature.Vendor
- CIM_BIOSFeature.Version
- CIM_BIOSFeature.Name
- CIM_BIOSFeature.CharacteristicDescriptions
- CIM_BIOSFeature.Characteristics
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 538dc9e4c18d976901519ae0e2d6f5249fd25c35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847440"
---
# <a name="cim_biosfeature-class"></a><span data-ttu-id="aedeb-103">CIM \_ BIOSFeature 類別</span><span class="sxs-lookup"><span data-stu-id="aedeb-103">CIM\_BIOSFeature class</span></span>

<span data-ttu-id="aedeb-104">**CIM \_ BIOSFeature** 類別代表用來啟動及設定電腦系統的低層級軟體的功能。</span><span class="sxs-lookup"><span data-stu-id="aedeb-104">The **CIM\_BIOSFeature** class represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aedeb-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="aedeb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aedeb-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aedeb-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aedeb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aedeb-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="aedeb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aedeb-109">語法</span><span class="sxs-lookup"><span data-stu-id="aedeb-109">Syntax</span></span>

``` syntax
[UUID("{7D33100E-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   IdentifyingNumber;
  string   ProductName;
  string   Vendor;
  string   Version;
  string   Name;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="aedeb-110">成員</span><span class="sxs-lookup"><span data-stu-id="aedeb-110">Members</span></span>

<span data-ttu-id="aedeb-111">**CIM \_ BIOSFeature** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aedeb-111">The **CIM\_BIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="aedeb-112">屬性</span><span class="sxs-lookup"><span data-stu-id="aedeb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aedeb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="aedeb-113">Properties</span></span>

<span data-ttu-id="aedeb-114">**CIM \_ BIOSFeature** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aedeb-114">The **CIM\_BIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aedeb-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="aedeb-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="aedeb-119">A short textual description of the object.</span></span>

<span data-ttu-id="aedeb-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aedeb-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="aedeb-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-122">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="aedeb-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-124">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| BIOS 特性 \| 003.4 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**。**特性**") </span><span class="sxs-lookup"><span data-stu-id="aedeb-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-125">自由格式字串的陣列，提供 **特性** 陣列中所指出之 BIOS 功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="aedeb-125">Array of free-form strings that provides detailed explanations of the BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="aedeb-126">此陣列中的每個專案都與 **特性** 陣列中的專案相關，該專案位於相同的索引。</span><span class="sxs-lookup"><span data-stu-id="aedeb-126">Each entry in this array is related to the entry in the **Characteristics** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="aedeb-127">**特性**</span><span class="sxs-lookup"><span data-stu-id="aedeb-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-128">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="aedeb-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-130">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| BIOS 特性 \| 003.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**。**CharacteristicDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="aedeb-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-131">整數的陣列，指定 BIOS 所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="aedeb-131">Array of integers that specifies the features supported by the BIOS.</span></span> <span data-ttu-id="aedeb-132">在 CIM 架構中，值3是不正確，因為它代表 DMI 中不支援任何 BIOS 功能。</span><span class="sxs-lookup"><span data-stu-id="aedeb-132">The value 3 is not valid in the CIM schema because it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="aedeb-133">在這種情況下，這個物件不應該具現化。</span><span class="sxs-lookup"><span data-stu-id="aedeb-133">In which case, this object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aedeb-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="aedeb-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-135">其他。</span><span class="sxs-lookup"><span data-stu-id="aedeb-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aedeb-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="aedeb-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-137">不明。</span><span class="sxs-lookup"><span data-stu-id="aedeb-137">Unknown.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="aedeb-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** (3) </span><span class="sxs-lookup"><span data-stu-id="aedeb-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-139">未定義。</span><span class="sxs-lookup"><span data-stu-id="aedeb-139">Undefined.</span></span>

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span data-ttu-id="aedeb-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA 支援** (4) </span><span class="sxs-lookup"><span data-stu-id="aedeb-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA Support** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-141">ISA 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-141">ISA support.</span></span>

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span data-ttu-id="aedeb-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA 支援** (5) </span><span class="sxs-lookup"><span data-stu-id="aedeb-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA Support** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-143">MCA 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-143">MCA support.</span></span>

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span data-ttu-id="aedeb-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA 支援** (6) </span><span class="sxs-lookup"><span data-stu-id="aedeb-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA Support** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-145">EISA 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-145">EISA support.</span></span>

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span data-ttu-id="aedeb-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI 支援** (7) </span><span class="sxs-lookup"><span data-stu-id="aedeb-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI Support** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-147">PCI 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-147">PCI support.</span></span>

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span data-ttu-id="aedeb-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span> (8) 的 **PCMCIA 支援**</span><span class="sxs-lookup"><span data-stu-id="aedeb-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA Support** (8)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-149">PCMCIA 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-149">PCMCIA support.</span></span>

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span data-ttu-id="aedeb-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP 支援** (9) </span><span class="sxs-lookup"><span data-stu-id="aedeb-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP Support** (9)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-151">PnP 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-151">PnP support.</span></span>

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span data-ttu-id="aedeb-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM 支援** (10) </span><span class="sxs-lookup"><span data-stu-id="aedeb-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM Support** (10)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-153">APM 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-153">APM support.</span></span>

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span data-ttu-id="aedeb-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>可 **升級的 BIOS** (11) </span><span class="sxs-lookup"><span data-stu-id="aedeb-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradeable BIOS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-155">可升級的 BIOS。</span><span class="sxs-lookup"><span data-stu-id="aedeb-155">Upgradeable BIOS.</span></span>

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="aedeb-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>允許 (12) 的 **BIOS 遮蔽**</span><span class="sxs-lookup"><span data-stu-id="aedeb-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing Allowed** (12)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-157">允許 BIOS 遮蔽。</span><span class="sxs-lookup"><span data-stu-id="aedeb-157">BIOS shadowing allowed.</span></span>

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span data-ttu-id="aedeb-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA 支援** (13) </span><span class="sxs-lookup"><span data-stu-id="aedeb-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA Support** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-159">VL VESA 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-159">VL VESA support.</span></span>

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span data-ttu-id="aedeb-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD 支援** (14) </span><span class="sxs-lookup"><span data-stu-id="aedeb-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD Support** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-161">ESCD 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-161">ESCD support.</span></span>

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span data-ttu-id="aedeb-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 支援** (15) </span><span class="sxs-lookup"><span data-stu-id="aedeb-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 Support** (15)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-163">LS-120 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-163">LS-120 support.</span></span>

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span data-ttu-id="aedeb-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI 支援** (16) </span><span class="sxs-lookup"><span data-stu-id="aedeb-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI Support** (16)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-165">ACPI 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-165">ACPI support.</span></span>

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span data-ttu-id="aedeb-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O 開機支援** (17) </span><span class="sxs-lookup"><span data-stu-id="aedeb-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O Boot Support** (17)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-167">I2O 開機支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-167">I2O boot support.</span></span>

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span data-ttu-id="aedeb-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB 舊版支援** (18) </span><span class="sxs-lookup"><span data-stu-id="aedeb-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy Support** (18)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-169">USB 舊版支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-169">USB legacy support.</span></span>

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span data-ttu-id="aedeb-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP 支援** (19) </span><span class="sxs-lookup"><span data-stu-id="aedeb-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP Support** (19)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-171">AGP 支援。</span><span class="sxs-lookup"><span data-stu-id="aedeb-171">AGP support.</span></span>

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span data-ttu-id="aedeb-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC 卡** (20) </span><span class="sxs-lookup"><span data-stu-id="aedeb-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-173">電腦卡。</span><span class="sxs-lookup"><span data-stu-id="aedeb-173">PC card.</span></span>

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span data-ttu-id="aedeb-174"><span id="IR"></span><span id="ir"></span>**IR** (21) </span><span class="sxs-lookup"><span data-stu-id="aedeb-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-175">紅外。</span><span class="sxs-lookup"><span data-stu-id="aedeb-175">IR.</span></span>

</dd> <dt>

<span id="1394"></span>

<span data-ttu-id="aedeb-176"><span id="1394"></span>**1394** (22) </span><span class="sxs-lookup"><span data-stu-id="aedeb-176"><span id="1394"></span>**1394** (22)</span></span>


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="aedeb-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23) </span><span class="sxs-lookup"><span data-stu-id="aedeb-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-178">I2c。</span><span class="sxs-lookup"><span data-stu-id="aedeb-178">I2C.</span></span>

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span data-ttu-id="aedeb-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**智慧型電池** (24) </span><span class="sxs-lookup"><span data-stu-id="aedeb-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-180">智慧型電池。</span><span class="sxs-lookup"><span data-stu-id="aedeb-180">Smart battery.</span></span>

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="aedeb-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160) </span><span class="sxs-lookup"><span data-stu-id="aedeb-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>


</dt> <dd>

<span data-ttu-id="aedeb-182">電腦-98。</span><span class="sxs-lookup"><span data-stu-id="aedeb-182">PC-98.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aedeb-183">**說明**</span><span class="sxs-lookup"><span data-stu-id="aedeb-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-186">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-187">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="aedeb-187">A textual description of the object.</span></span>

<span data-ttu-id="aedeb-188">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aedeb-189">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="aedeb-189">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-192">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**IdentifyingNumber**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="aedeb-192">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-193">產品識別，例如軟體上的序號或硬體晶片上的骰子編號。</span><span class="sxs-lookup"><span data-stu-id="aedeb-193">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

<span data-ttu-id="aedeb-194">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-194">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="aedeb-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aedeb-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-196">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="aedeb-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-198">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="aedeb-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-199">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="aedeb-199">Indicates when the object was installed.</span></span> <span data-ttu-id="aedeb-200">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="aedeb-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="aedeb-201">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aedeb-202">**名稱**</span><span class="sxs-lookup"><span data-stu-id="aedeb-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-205">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="aedeb-205">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-206">Name 屬性會定義物件在資料處理系統外部已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="aedeb-206">The Name property defines the label by which the object is known to the world outside the data processing system.</span></span> <span data-ttu-id="aedeb-207">這個標籤是人類看得懂的名稱，可唯一識別元素命名空間內容中的元素。</span><span class="sxs-lookup"><span data-stu-id="aedeb-207">This label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="aedeb-208">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-208">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="aedeb-209">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="aedeb-209">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-212">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Name**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="aedeb-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-213">常用的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="aedeb-213">Commonly used product name.</span></span>

<span data-ttu-id="aedeb-214">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-214">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="aedeb-215">**狀態**</span><span class="sxs-lookup"><span data-stu-id="aedeb-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-218">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-218">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-219">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="aedeb-219">String that indicates the current status of the object.</span></span> <span data-ttu-id="aedeb-220">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="aedeb-220">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="aedeb-221">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="aedeb-221">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="aedeb-222">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="aedeb-222">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="aedeb-223">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="aedeb-223">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aedeb-224">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="aedeb-224">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aedeb-225">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="aedeb-225">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aedeb-226">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-226">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aedeb-227">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="aedeb-227">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aedeb-228">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-228">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aedeb-229">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-229">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aedeb-230">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-230">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aedeb-231">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-231">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aedeb-232">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-232">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aedeb-233">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-233">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aedeb-234">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-234">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aedeb-235">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-235">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aedeb-236">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-236">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aedeb-237">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-237">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aedeb-238">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-238">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aedeb-239">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="aedeb-239">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aedeb-240">**廠商**</span><span class="sxs-lookup"><span data-stu-id="aedeb-240">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-243">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**廠商**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="aedeb-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-244">產品供應商的名稱，其對應至「DMTF 解決方案交換標準」產品物件中的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aedeb-244">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="aedeb-245">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-245">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="aedeb-246">**版本**</span><span class="sxs-lookup"><span data-stu-id="aedeb-246">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aedeb-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aedeb-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aedeb-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aedeb-249">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Version**") 、 [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="aedeb-249">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="aedeb-250">產品版本資訊，對應至 [DMTF 解決方案交換標準] 產品物件中的 [ **版本** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="aedeb-250">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="aedeb-251">這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-251">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aedeb-252">備註</span><span class="sxs-lookup"><span data-stu-id="aedeb-252">Remarks</span></span>

<span data-ttu-id="aedeb-253">**Cim \_ BIOSFeature** 類別衍生自 [**cim \_ SoftwareFeature**](cim-softwarefeature.md)。</span><span class="sxs-lookup"><span data-stu-id="aedeb-253">The **CIM\_BIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="aedeb-254">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="aedeb-254">WMI does not implement this class.</span></span>

<span data-ttu-id="aedeb-255">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="aedeb-255">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aedeb-256">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="aedeb-256">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aedeb-257">規格需求</span><span class="sxs-lookup"><span data-stu-id="aedeb-257">Requirements</span></span>



| <span data-ttu-id="aedeb-258">需求</span><span class="sxs-lookup"><span data-stu-id="aedeb-258">Requirement</span></span> | <span data-ttu-id="aedeb-259">值</span><span class="sxs-lookup"><span data-stu-id="aedeb-259">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aedeb-260">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aedeb-260">Minimum supported client</span></span><br/> | <span data-ttu-id="aedeb-261">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aedeb-261">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aedeb-262">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aedeb-262">Minimum supported server</span></span><br/> | <span data-ttu-id="aedeb-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aedeb-263">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aedeb-264">命名空間</span><span class="sxs-lookup"><span data-stu-id="aedeb-264">Namespace</span></span><br/>                | <span data-ttu-id="aedeb-265">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aedeb-265">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aedeb-266">MOF</span><span class="sxs-lookup"><span data-stu-id="aedeb-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aedeb-267"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="aedeb-267"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aedeb-268">DLL</span><span class="sxs-lookup"><span data-stu-id="aedeb-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aedeb-269"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aedeb-269"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aedeb-270">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aedeb-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aedeb-271">**CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="aedeb-271">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 


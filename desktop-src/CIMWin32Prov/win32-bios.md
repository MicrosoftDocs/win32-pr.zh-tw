---
description: 代表電腦上所安裝之電腦系統的基本輸入/輸出服務 (BIOS) 的屬性。
ms.assetid: e4a5aaf0-0432-4517-97b7-ac05ffd10b5b
ms.tgt_platform: multiple
title: Win32_BIOS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BIOS
- Win32_BIOS.BiosCharacteristics
- Win32_BIOS.BIOSVersion
- Win32_BIOS.BuildNumber
- Win32_BIOS.Caption
- Win32_BIOS.CodeSet
- Win32_BIOS.CurrentLanguage
- Win32_BIOS.Description
- Win32_BIOS.EmbeddedControllerMajorVersion
- Win32_BIOS.EmbeddedControllerMinorVersion
- Win32_BIOS.IdentificationCode
- Win32_BIOS.InstallableLanguages
- Win32_BIOS.InstallDate
- Win32_BIOS.LanguageEdition
- Win32_BIOS.ListOfLanguages
- Win32_BIOS.Manufacturer
- Win32_BIOS.Name
- Win32_BIOS.OtherTargetOS
- Win32_BIOS.PrimaryBIOS
- Win32_BIOS.ReleaseDate
- Win32_BIOS.SerialNumber
- Win32_BIOS.SMBIOSBIOSVersion
- Win32_BIOS.SMBIOSMajorVersion
- Win32_BIOS.SMBIOSMinorVersion
- Win32_BIOS.SMBIOSPresent
- Win32_BIOS.SoftwareElementID
- Win32_BIOS.SoftwareElementState
- Win32_BIOS.Status
- Win32_BIOS.SystemBiosMajorVersion
- Win32_BIOS.SystemBiosMinorVersion
- Win32_BIOS.TargetOperatingSystem
- Win32_BIOS.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c1e953c9c1348a133cf4755ab04f6024c42034
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510689"
---
# <a name="win32_bios-class"></a><span data-ttu-id="152a0-103">Win32 \_ BIOS 類別</span><span class="sxs-lookup"><span data-stu-id="152a0-103">Win32\_BIOS class</span></span>

<span data-ttu-id="152a0-104">**Win32 \_ BIOS** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表電腦系統的基本輸入/輸出服務 (BIOS) 安裝在電腦上的屬性。</span><span class="sxs-lookup"><span data-stu-id="152a0-104">The **Win32\_BIOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the attributes of the computer system's basic input/output services (BIOS) that are installed on a computer.</span></span>

<span data-ttu-id="152a0-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="152a0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="152a0-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="152a0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="152a0-107">語法</span><span class="sxs-lookup"><span data-stu-id="152a0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BIOS : CIM_BIOSElement
{
  uint16   BiosCharacteristics[];
  string   BIOSVersion[];
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   CurrentLanguage;
  string   Description;
  uint8    EmbeddedControllerMajorVersion;
  uint8    EmbeddedControllerMinorVersion;
  string   IdentificationCode;
  uint16   InstallableLanguages;
  datetime InstallDate;
  string   LanguageEdition;
  String   ListOfLanguages[];
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  boolean  PrimaryBIOS;
  datetime ReleaseDate;
  string   SerialNumber;
  string   SMBIOSBIOSVersion;
  uint16   SMBIOSMajorVersion;
  uint16   SMBIOSMinorVersion;
  boolean  SMBIOSPresent;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint8    SystemBiosMajorVersion;
  uint8    SystemBiosMinorVersion;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="152a0-108">成員</span><span class="sxs-lookup"><span data-stu-id="152a0-108">Members</span></span>

<span data-ttu-id="152a0-109">**Win32 \_ BIOS** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="152a0-109">The **Win32\_BIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="152a0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="152a0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="152a0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="152a0-111">Properties</span></span>

<span data-ttu-id="152a0-112">**Win32 \_ BIOS** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="152a0-112">The **Win32\_BIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="152a0-113">**BiosCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="152a0-113">**BiosCharacteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-114">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="152a0-114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="152a0-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-116">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 0 \| BIOS 特性" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Characteristics")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-117">系統管理 BIOS 參考規格所定義之系統所支援的 BIOS 特性陣列。</span><span class="sxs-lookup"><span data-stu-id="152a0-117">Array of BIOS characteristics supported by the system as defined by the System Management BIOS Reference Specification.</span></span>

<span data-ttu-id="152a0-118">此值來自于 SMBIOS 資訊中 **Bios 資訊** 結構的 **bios 特性** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-118">This value comes from the **BIOS Characteristics** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="152a0-119">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="152a0-119">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="152a0-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="152a0-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="152a0-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="152a0-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="152a0-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="152a0-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span data-ttu-id="152a0-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**不支援的 BIOS 特性** (3) </span><span class="sxs-lookup"><span data-stu-id="152a0-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**BIOS Characteristics Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span> (4) **支援 ISA**</span><span class="sxs-lookup"><span data-stu-id="152a0-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span> (為 5) **支援 MCA**</span><span class="sxs-lookup"><span data-stu-id="152a0-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span> (6) **支援 EISA**</span><span class="sxs-lookup"><span data-stu-id="152a0-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span> (7) **支援 PCI**</span><span class="sxs-lookup"><span data-stu-id="152a0-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="152a0-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**支援 (PCMCIA) 的電腦配接器** (8) </span><span class="sxs-lookup"><span data-stu-id="152a0-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC Card (PCMCIA) is supported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**隨插即用支援** (9) </span><span class="sxs-lookup"><span data-stu-id="152a0-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play is supported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span> (10) **支援 APM**</span><span class="sxs-lookup"><span data-stu-id="152a0-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM is supported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span data-ttu-id="152a0-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS 可升級 (Flash)** (11) </span><span class="sxs-lookup"><span data-stu-id="152a0-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS is Upgradeable (Flash)** (11)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-132">BIOS 可升級 (Flash) </span><span class="sxs-lookup"><span data-stu-id="152a0-132">BIOS is Upgradable (Flash)</span></span>

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span data-ttu-id="152a0-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**允許 BIOS 遮蔽** (12) </span><span class="sxs-lookup"><span data-stu-id="152a0-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**BIOS shadowing is allowed** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span> (13) **支援 VL-VESA**</span><span class="sxs-lookup"><span data-stu-id="152a0-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA is supported** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span data-ttu-id="152a0-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span> (14) **提供 ESCD 支援**</span><span class="sxs-lookup"><span data-stu-id="152a0-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**ESCD support is available** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span> (15) **支援從 CD 開機**</span><span class="sxs-lookup"><span data-stu-id="152a0-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Boot from CD is supported** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span> (16) **支援可選取的開機**</span><span class="sxs-lookup"><span data-stu-id="152a0-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Selectable Boot is supported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span data-ttu-id="152a0-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM socketed** (17) </span><span class="sxs-lookup"><span data-stu-id="152a0-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM is socketed** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="152a0-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span> (18 **(PCMCIA) 支援從電腦卡開機**) </span><span class="sxs-lookup"><span data-stu-id="152a0-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Boot From PC Card (PCMCIA) is supported** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**支援 EDD (增強的磁片磁碟機) 規格** (19) </span><span class="sxs-lookup"><span data-stu-id="152a0-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**EDD (Enhanced Disk Drive) Specification is supported** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="152a0-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h-適用于 NEC 9800 1.2 mb 的日文磁片 (3.5」、1千 \\ 位元組/磁區、360 RPM) 支援** (20) </span><span class="sxs-lookup"><span data-stu-id="152a0-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5\\", 1k Bytes/Sector, 360 RPM) is supported** (20)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-142">Int 13h-支援 NEC 9800 1.2 mb 的日文磁片 (3.5、1千位元組/磁區、360 RPM) </span><span class="sxs-lookup"><span data-stu-id="152a0-142">Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="152a0-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h-日文 Toshiba 1.2 mb (3.5」 \\ 、360 RPM) 支援** (21) </span><span class="sxs-lookup"><span data-stu-id="152a0-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5\\", 360 RPM) is supported** (21)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-144">Int 13h-日文 Toshiba 1.2 mb (3.5、360 RPM) 支援</span><span class="sxs-lookup"><span data-stu-id="152a0-144">Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="152a0-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**支援 Int 13h-5.25 \\ "/360 KB 的軟碟服務** (22) </span><span class="sxs-lookup"><span data-stu-id="152a0-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" / 360 KB Floppy Services are supported** (22)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-146">支援 Int 13h-5.25/360 KB 的軟碟服務</span><span class="sxs-lookup"><span data-stu-id="152a0-146">Int 13h - 5.25 / 360 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="152a0-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span> (23) **支援 Int 13h-5.25 \\ "/1.2MB 的軟碟服務**</span><span class="sxs-lookup"><span data-stu-id="152a0-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" /1.2MB Floppy Services are supported** (23)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-148">支援 Int 13h-5.25/1.2MB 軟碟服務</span><span class="sxs-lookup"><span data-stu-id="152a0-148">Int 13h - 5.25 /1.2MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span data-ttu-id="152a0-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span> (24) **支援 Int 13h-3.5 \\ "/720 KB 的軟碟服務**</span><span class="sxs-lookup"><span data-stu-id="152a0-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h - 3.5\\" / 720 KB Floppy Services are supported** (24)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-150">支援 Int 13h-3.5/720 KB 的軟碟服務</span><span class="sxs-lookup"><span data-stu-id="152a0-150">Int 13h - 3.5 / 720 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="152a0-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span> (25) **支援 Int 13h-3.5 \\ "/2.88 MB 的軟碟服務**</span><span class="sxs-lookup"><span data-stu-id="152a0-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 3.5\\" / 2.88 MB Floppy Services are supported** (25)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-152">支援 Int 13h-3.5/2.88 MB 的軟碟服務</span><span class="sxs-lookup"><span data-stu-id="152a0-152">Int 13h - 3.5 / 2.88 MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**整數5h，支援列印畫面服務** (26) </span><span class="sxs-lookup"><span data-stu-id="152a0-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, Print Screen Service is supported** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="152a0-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span> (27) **支援 Int 9h、8042鍵盤服務**</span><span class="sxs-lookup"><span data-stu-id="152a0-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 Keyboard services are supported** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="152a0-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h， (28) 支援序列服務**</span><span class="sxs-lookup"><span data-stu-id="152a0-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, Serial Services are supported** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="152a0-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**整數17h，支援印表機服務** (29) </span><span class="sxs-lookup"><span data-stu-id="152a0-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, printer services are supported** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="152a0-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span> (30) **支援 Int 10h、CGA/Mono 影片服務**</span><span class="sxs-lookup"><span data-stu-id="152a0-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, CGA/Mono Video Services are supported** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span data-ttu-id="152a0-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31) </span><span class="sxs-lookup"><span data-stu-id="152a0-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span data-ttu-id="152a0-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI 支援** (32) </span><span class="sxs-lookup"><span data-stu-id="152a0-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI supported** (32)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-160">支援 ACPI</span><span class="sxs-lookup"><span data-stu-id="152a0-160">ACPI is supported</span></span>

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span> (33) **支援 USB 舊版**</span><span class="sxs-lookup"><span data-stu-id="152a0-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**USB Legacy is supported** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span> (34) **支援 AGP**</span><span class="sxs-lookup"><span data-stu-id="152a0-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP is supported** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**支援 I2O 開機** (35) </span><span class="sxs-lookup"><span data-stu-id="152a0-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**I2O boot is supported** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 開機支援** (36) </span><span class="sxs-lookup"><span data-stu-id="152a0-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 boot is supported** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span> (37) **支援 ATAPI ZIP 磁片磁碟機開機**</span><span class="sxs-lookup"><span data-stu-id="152a0-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**ATAPI ZIP Drive boot is supported** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="152a0-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 (支援開機** 38) </span><span class="sxs-lookup"><span data-stu-id="152a0-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 boot is supported** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span data-ttu-id="152a0-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>支援 (39) 的 **智慧型電池**</span><span class="sxs-lookup"><span data-stu-id="152a0-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Smart Battery supported** (39)</span></span>


</dt> <dd>

<span data-ttu-id="152a0-168">支援智慧電池</span><span class="sxs-lookup"><span data-stu-id="152a0-168">Smart Battery is supported</span></span>

</dd> <dt>

<span data-ttu-id="152a0-169">40 47</span><span class="sxs-lookup"><span data-stu-id="152a0-169">40 47</span></span>
</dt> <dd>

<span data-ttu-id="152a0-170">保留給 BIOS 廠商</span><span class="sxs-lookup"><span data-stu-id="152a0-170">Reserved for BIOS vendor</span></span>

</dd> <dt>

<span data-ttu-id="152a0-171">48 63</span><span class="sxs-lookup"><span data-stu-id="152a0-171">48 63</span></span>
</dt> <dd>

<span data-ttu-id="152a0-172">保留給系統廠商</span><span class="sxs-lookup"><span data-stu-id="152a0-172">Reserved for system vendor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="152a0-173">**BIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-173">**BIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-174">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="152a0-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="152a0-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152a0-176">完整系統 BIOS 資訊的陣列。</span><span class="sxs-lookup"><span data-stu-id="152a0-176">Array of the complete system BIOS information.</span></span> <span data-ttu-id="152a0-177">在許多電腦中，可能會有數個版本字串儲存在登錄中，並代表系統 BIOS 資訊。</span><span class="sxs-lookup"><span data-stu-id="152a0-177">In many computers there can be several version strings that are stored in the registry and represent the system BIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-178">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="152a0-178">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-181">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.4 ") </span><span class="sxs-lookup"><span data-stu-id="152a0-181">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-182">此軟體專案之編譯的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="152a0-182">Internal identifier for this compilation of this software element.</span></span>

<span data-ttu-id="152a0-183">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-183">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-184">**標題**</span><span class="sxs-lookup"><span data-stu-id="152a0-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-187">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-188">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="152a0-188">Short description of the object a one-line string.</span></span>

<span data-ttu-id="152a0-189">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-190">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="152a0-190">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-193">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="152a0-193">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="152a0-194">此軟體專案所使用的程式碼集。</span><span class="sxs-lookup"><span data-stu-id="152a0-194">Code set used by this software element.</span></span>

<span data-ttu-id="152a0-195">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-195">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-196">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="152a0-196">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-199">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 13 \| Current Language" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Current Language")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-200">目前 BIOS 語言的名稱。</span><span class="sxs-lookup"><span data-stu-id="152a0-200">Name of the current BIOS language.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-201">**說明**</span><span class="sxs-lookup"><span data-stu-id="152a0-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-204">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-204">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-205">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="152a0-205">Description of the object.</span></span>

<span data-ttu-id="152a0-206">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-207">**EmbeddedControllerMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-207">**EmbeddedControllerMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-208">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="152a0-208">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-210">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 0 \| Embedded Controller 固件主要版本" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-211">內嵌控制器固件的主要版本。</span><span class="sxs-lookup"><span data-stu-id="152a0-211">The major release of the embedded controller firmware.</span></span>

<span data-ttu-id="152a0-212">此值來自于 SMBIOS 資訊中 **BIOS 資訊** 結構的 **內嵌控制器固件主要版本** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-212">This value comes from the **Embedded Controller Firmware Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="152a0-213">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="152a0-213">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-214">**EmbeddedControllerMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-214">**EmbeddedControllerMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-215">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="152a0-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-217">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 0 \| Embedded Controller 固件次要版本" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-217">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-218">內嵌控制器固件的次要版本。</span><span class="sxs-lookup"><span data-stu-id="152a0-218">The minor release of the embedded controller firmware.</span></span>

<span data-ttu-id="152a0-219">此值來自于 SMBIOS 資訊中 **BIOS 資訊** 結構的 **內嵌控制器固件次要版次** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-219">This value comes from the **Embedded Controller Firmware Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="152a0-220">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="152a0-220">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-221">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="152a0-221">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-224">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.7 ") </span><span class="sxs-lookup"><span data-stu-id="152a0-224">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-225">此軟體元素的製造商識別碼。</span><span class="sxs-lookup"><span data-stu-id="152a0-225">Manufacturer's identifier for this software element.</span></span> <span data-ttu-id="152a0-226">通常這會是 (SKU) 或元件編號的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="152a0-226">Often this will be a stock keeping unit (SKU) or a part number.</span></span>

<span data-ttu-id="152a0-227">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-227">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-228">**InstallableLanguages**</span><span class="sxs-lookup"><span data-stu-id="152a0-228">**InstallableLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-229">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="152a0-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-231">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 13 可 \| 安裝的語言" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-231">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Installable Languages")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-232">可在此系統上安裝的語言數目。</span><span class="sxs-lookup"><span data-stu-id="152a0-232">Number of languages available for installation on this system.</span></span> <span data-ttu-id="152a0-233">語言可以決定屬性，例如 Unicode 和雙向文字的需求。</span><span class="sxs-lookup"><span data-stu-id="152a0-233">Language may determine properties such as the need for Unicode and bidirectional text.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="152a0-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-235">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="152a0-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-237">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="152a0-237">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-238">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="152a0-238">Date and time the object was installed.</span></span> <span data-ttu-id="152a0-239">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="152a0-239">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="152a0-240">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-241">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="152a0-241">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-244">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.6 ") </span><span class="sxs-lookup"><span data-stu-id="152a0-244">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-245">此軟體專案的語言版本。</span><span class="sxs-lookup"><span data-stu-id="152a0-245">Language edition of this software element.</span></span> <span data-ttu-id="152a0-246">應使用 ISO 639 中定義的語言代碼。</span><span class="sxs-lookup"><span data-stu-id="152a0-246">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="152a0-247">其中 software 專案代表多語系或國際版的產品，則應該使用「多語系」字串。</span><span class="sxs-lookup"><span data-stu-id="152a0-247">Where the software element represents a multilingual or international version of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="152a0-248">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-248">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-249">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="152a0-249">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-250">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="152a0-250">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="152a0-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-252">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 13 \| Language Strings" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Language Strings")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-253">可用的 BIOS 可安裝語言名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="152a0-253">Array of names of available BIOS-installable languages.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-254">**製造商**</span><span class="sxs-lookup"><span data-stu-id="152a0-254">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-257">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="152a0-257">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-258">此軟體元素的製造商。</span><span class="sxs-lookup"><span data-stu-id="152a0-258">Manufacturer of this software element.</span></span>

<span data-ttu-id="152a0-259">此值來自于 SMBIOS 資訊中 **BIOS 資訊** 結構的 **廠商** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-259">This value comes from the **Vendor** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="152a0-260">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-260">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-261">**名稱**</span><span class="sxs-lookup"><span data-stu-id="152a0-261">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-262">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-264">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="152a0-264">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="152a0-265">用來識別此軟體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="152a0-265">Name used to identify this software element.</span></span>

<span data-ttu-id="152a0-266">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-266">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-267">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="152a0-267">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-270">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OtherTypeDescription**") </span><span class="sxs-lookup"><span data-stu-id="152a0-270">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-271">當 **TargetOperatingSystem** 屬性的值為 1 (其他) 時，記錄軟體元素的製造商和作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="152a0-271">Records the manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 (Other).</span></span> <span data-ttu-id="152a0-272">當 **TargetOperatingSystem** 的值為1時， **OtherTargetOS** 必須具有非 null 值。</span><span class="sxs-lookup"><span data-stu-id="152a0-272">When **TargetOperatingSystem** has a value of 1, **OtherTargetOS** must have a nonnull value.</span></span> <span data-ttu-id="152a0-273">對於 **TargetOperatingSystem** 的所有其他值， **OtherTargetOS** 是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="152a0-273">For all other values of **TargetOperatingSystem**, **OtherTargetOS** is **NULL**.</span></span>

<span data-ttu-id="152a0-274">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-274">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-275">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="152a0-275">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-276">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="152a0-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-278">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="152a0-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-279">若 **為 TRUE**，則這是電腦系統的主要 BIOS。</span><span class="sxs-lookup"><span data-stu-id="152a0-279">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

<span data-ttu-id="152a0-280">這個屬性繼承自 [**CIM \_ BIOSElement**](cim-bioselement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-280">This property is inherited from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-281">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="152a0-281">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-282">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="152a0-282">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152a0-284">Windows BIOS 的發行日期（以國際標準時間 (UTC 格式）) YYYYMMDDHHMMSS.FFFFFF 的格式。MMMMMM (+-) OOO。</span><span class="sxs-lookup"><span data-stu-id="152a0-284">Release date of the Windows BIOS in the Coordinated Universal Time (UTC) format of YYYYMMDDHHMMSS.MMMMMM(+-)OOO.</span></span>

<span data-ttu-id="152a0-285">此值來自于 SMBIOS 資訊中 **Bios 資訊** 結構的 **bios 發行日期** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-285">This value comes from the **BIOS Release Date** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-286">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="152a0-286">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-287">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-289">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="152a0-289">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-290">軟體元素的已指派序號。</span><span class="sxs-lookup"><span data-stu-id="152a0-290">Assigned serial number of the software element.</span></span>

<span data-ttu-id="152a0-291">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-291">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-292">**SMBIOSBIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-292">**SMBIOSBIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-295">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 0 \| BIOS 版本" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Version")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-296">SMBIOS 所報告的 BIOS 版本。</span><span class="sxs-lookup"><span data-stu-id="152a0-296">BIOS version as reported by SMBIOS.</span></span>

<span data-ttu-id="152a0-297">此值來自于 SMBIOS 資訊中 **Bios 資訊** 結構的 **bios 版本** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-297">This value comes from the **BIOS Version** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-298">**SMBIOSMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-298">**SMBIOSMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-299">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="152a0-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-301">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| CSMBios \| GetVersion" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-302">主要 SMBIOS 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="152a0-302">Major SMBIOS version number.</span></span> <span data-ttu-id="152a0-303">如果找不到 SMBIOS，這個屬性會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="152a0-303">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-304">**SMBIOSMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-304">**SMBIOSMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-305">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="152a0-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-307">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| CSMBios \| GetVersion" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-308">次要 SMBIOS 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="152a0-308">Minor SMBIOS version number.</span></span> <span data-ttu-id="152a0-309">如果找不到 SMBIOS，這個屬性會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="152a0-309">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-310">**SMBIOSPresent**</span><span class="sxs-lookup"><span data-stu-id="152a0-310">**SMBIOSPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-311">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="152a0-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-313">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| CSMBios \| Init" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|Init")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-314">若 **為 true**，則表示 SMBIOS 可在此電腦系統上使用。</span><span class="sxs-lookup"><span data-stu-id="152a0-314">If **true**, the SMBIOS is available on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-315">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="152a0-315">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-318">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="152a0-318">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="152a0-319">此 software 元素的識別碼;設計用來與其他索引鍵搭配使用，以建立此實例的唯一標記法。</span><span class="sxs-lookup"><span data-stu-id="152a0-319">Identifier for this software element; designed to be used in conjunction with other keys to create a unique representation of this instance.</span></span>

<span data-ttu-id="152a0-320">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-320">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="152a0-321">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="152a0-321">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-322">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="152a0-322">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-324">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="152a0-324">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="152a0-325">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="152a0-325">State of a software element.</span></span>

<span data-ttu-id="152a0-326">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-326">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="152a0-327">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="152a0-327">The possible values are.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="152a0-328">可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="152a0-328">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="152a0-329">可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="152a0-329">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="152a0-330">**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="152a0-330">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="152a0-331">**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="152a0-331">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="152a0-332">**狀態**</span><span class="sxs-lookup"><span data-stu-id="152a0-332">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-335">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-335">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-336">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="152a0-336">Current status of the object.</span></span> <span data-ttu-id="152a0-337">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="152a0-337">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="152a0-338">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="152a0-338">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="152a0-339">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="152a0-339">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="152a0-340">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="152a0-340">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="152a0-341">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="152a0-341">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="152a0-342">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="152a0-343">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="152a0-343">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="152a0-344">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="152a0-344">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="152a0-345">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-345">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="152a0-346">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-346">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="152a0-347">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-347">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="152a0-348">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-348">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="152a0-349">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-349">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="152a0-350">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-350">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="152a0-351">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-351">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="152a0-352">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-352">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="152a0-353">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-353">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="152a0-354">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-354">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="152a0-355">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="152a0-355">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="152a0-356">**SystemBiosMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-356">**SystemBiosMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-357">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="152a0-357">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-359">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| TYPE 0 \| System BIOS 主要版本" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-360">系統 BIOS 的主要版本。</span><span class="sxs-lookup"><span data-stu-id="152a0-360">The major release of the System BIOS.</span></span>

<span data-ttu-id="152a0-361">此值來自于 SMBIOS 資訊中 **Bios 資訊** 結構的 **系統 bios 主要版本** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-361">This value comes from the **System BIOS Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="152a0-362">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="152a0-362">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-363">**SystemBiosMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="152a0-363">**SystemBiosMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-364">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="152a0-364">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-366">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| TYPE 0 \| System BIOS 次要版本" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-367">系統 BIOS 的次要版本。</span><span class="sxs-lookup"><span data-stu-id="152a0-367">The minor release of the System BIOS.</span></span>

<span data-ttu-id="152a0-368">此值來自于 SMBIOS 資訊中 **Bios 資訊** 結構的 **系統 Bios 次要版次** 成員。</span><span class="sxs-lookup"><span data-stu-id="152a0-368">This value comes from the **System BIOS Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="152a0-369">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="152a0-369">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="152a0-370">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="152a0-370">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-371">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="152a0-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-373">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Software Component Information \| 002.5 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OSType**") </span><span class="sxs-lookup"><span data-stu-id="152a0-373">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-374">擁有軟體元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="152a0-374">Target operating system of the owning software element.</span></span>

<span data-ttu-id="152a0-375">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-375">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="152a0-376">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="152a0-376">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="152a0-377">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="152a0-377">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="152a0-378">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="152a0-378">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="152a0-379">**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="152a0-379">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="152a0-380">**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="152a0-380">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="152a0-381">**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="152a0-381">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="152a0-382">**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="152a0-382">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="152a0-383">**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="152a0-383">**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="152a0-384">**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="152a0-384">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="152a0-385">**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="152a0-385">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="152a0-386">**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="152a0-386">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="152a0-387">**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="152a0-387">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="152a0-388">**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="152a0-388">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="152a0-389">**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="152a0-389">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="152a0-390">**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="152a0-390">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="152a0-391">**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="152a0-391">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="152a0-392">**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="152a0-392">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="152a0-393">**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="152a0-393">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="152a0-394">**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="152a0-394">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="152a0-395">**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="152a0-395">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="152a0-396">**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="152a0-396">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="152a0-397">**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="152a0-397">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="152a0-398">**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="152a0-398">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="152a0-399">**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="152a0-399">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="152a0-400">**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="152a0-400">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="152a0-401">相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="152a0-401">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="152a0-402">**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="152a0-402">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="152a0-403">**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="152a0-403">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="152a0-404">**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="152a0-404">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="152a0-405">**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="152a0-405">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="152a0-406">**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="152a0-406">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="152a0-407">**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="152a0-407">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="152a0-408">**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="152a0-408">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="152a0-409">**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="152a0-409">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="152a0-410">**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="152a0-410">**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="152a0-411">**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="152a0-411">**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="152a0-412">**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="152a0-412">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="152a0-413">**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="152a0-413">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="152a0-414">**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="152a0-414">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="152a0-415">**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="152a0-415">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="152a0-416">**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="152a0-416">**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="152a0-417">**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="152a0-417">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="152a0-418">**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="152a0-418">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="152a0-419">**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="152a0-419">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="152a0-420">**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="152a0-420">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="152a0-421">**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="152a0-421">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="152a0-422">**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="152a0-422">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="152a0-423">**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="152a0-423">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="152a0-424">**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="152a0-424">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="152a0-425">**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="152a0-425">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="152a0-426">**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="152a0-426">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="152a0-427">**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="152a0-427">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="152a0-428">**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="152a0-428">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="152a0-429">**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="152a0-429">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="152a0-430">**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="152a0-430">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="152a0-431">**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="152a0-431">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="152a0-432">**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="152a0-432">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="152a0-433">**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="152a0-433">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="152a0-434">**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="152a0-434">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="152a0-435">**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="152a0-435">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="152a0-436">**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="152a0-436">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="152a0-437">**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="152a0-437">**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="152a0-438">**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="152a0-438">**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="152a0-439">**版本**</span><span class="sxs-lookup"><span data-stu-id="152a0-439">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152a0-440">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="152a0-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152a0-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="152a0-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152a0-442">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Version" ) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 硬體 \\ \\ Description \\ \\ System \| SystemBiosVersion" ) </span><span class="sxs-lookup"><span data-stu-id="152a0-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HARDWARE\\\\Description\\\\System\|SystemBiosVersion")</span></span>
</dt> </dl>

<span data-ttu-id="152a0-443">BIOS 的版本。</span><span class="sxs-lookup"><span data-stu-id="152a0-443">Version of the BIOS.</span></span> <span data-ttu-id="152a0-444">這個字串是由 BIOS 製造商所建立。</span><span class="sxs-lookup"><span data-stu-id="152a0-444">This string is created by the BIOS manufacturer.</span></span>

<span data-ttu-id="152a0-445">這個屬性繼承自 [**CIM \_ SoftwareElement**](cim-softwareelement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-445">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="152a0-446">備註</span><span class="sxs-lookup"><span data-stu-id="152a0-446">Remarks</span></span>

<span data-ttu-id="152a0-447">**Win32 \_ BIOS** 類別衍生自 [**CIM \_ BIOSElement**](cim-bioselement.md)。</span><span class="sxs-lookup"><span data-stu-id="152a0-447">The **Win32\_BIOS** class is derived from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

<span data-ttu-id="152a0-448">**Win32 \_ bios** 類別中的屬性可能會針對具有相同 BIOS 的特定電腦系統變更，例如透過舊版 bios 模式開機，以及透過 UEFI BIOS 模式開機。</span><span class="sxs-lookup"><span data-stu-id="152a0-448">The properties in the **Win32\_BIOS** class may change for a specific computer system with the same BIOS, for example booting through a legacy BIOS mode vs. booting through UEFI BIOS mode.</span></span> <span data-ttu-id="152a0-449">不過，從 SMBIOS 結構取出的屬性應該維持不變。</span><span class="sxs-lookup"><span data-stu-id="152a0-449">However the properties retrieved from the SMBIOS structures should remain the same.</span></span>

## <a name="examples"></a><span data-ttu-id="152a0-450">範例</span><span class="sxs-lookup"><span data-stu-id="152a0-450">Examples</span></span>

<span data-ttu-id="152a0-451">[本機/遠端電腦上的 Get-computerinfo 查詢電腦資訊（ (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell 範例（英文）： TechNet 資源庫上的 PowerShell 範例會使用一些硬體和軟體的呼叫，包括 **Win32 \_ BIOS**，以顯示本機或遠端系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="152a0-451">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to display information about a local or remote system.</span></span>

<span data-ttu-id="152a0-452">TechNet 資源庫上的「 [產生系統資訊做為 XML](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) 階層的 VBScript 範例」會使用一些硬體和軟體的呼叫，包括 **Win32 \_ BIOS**，以使用手動 xml 輸出來產生系統的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="152a0-452">The [Generate system information as XML hierarchy](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) VBScript sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to generate an XML representation of a system using a manual XML output.</span></span>

<span data-ttu-id="152a0-453">下列 PowerShell 程式碼範例會使用 **Win32 \_ bios** 來傳回 BIOS 的特性</span><span class="sxs-lookup"><span data-stu-id="152a0-453">The following PowerShell code sample uses **Win32\_BIOS** to return characteristics of the BIOS</span></span>


```PowerShell
# wmi-win32_bios.ps1
# Demonstrates use of Win32_Bios WMI class
# Thomas Lee - tfl@psp.co.uk



# Helper function to return characterics of the BIOS
function get-WmiBiosCharacteristics {
param ([uint16] $char)

# parse and return values

If ($char -le 39) {

switch ($char) {
0   {"00-Reserved"}
1   {"01-Reserved"}
2   {"02-Unknown"}
3   {"03-BIOS Characteristics Not Supported"}
4   {"04-ISA is supported"}
5   {"05-MCA is supported"}
6   {"06-EISA is supported"}
7   {"07-PCI is supported"}
8   {"08-PC Card (PCMCIA) is supported"}
9   {"09-Plug and Play is supported"}
10  {"10-APM is supported"}
11  {"11-BIOS is Upgradable (Flash)"}
12  {"12-BIOS shadowing is allowed"}
13  {"13-VL-VESA is supported"}
14  {"14-ESCD support is available"}
15  {"15-Boot from CD is supported"}
16  {"16-Selectable Boot is supported"}
17  {"17-BIOS ROM is socketed"}
18  {"18-Boot From PC Card (PCMCIA) is supported"}
19  {"19-EDD (Enhanced Disk Drive) Specification is supported"}
20  {"20-Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported"}
21  {"21-Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported"}
22  {"22-Int 13h - 5.25 / 360 KB Floppy Services are supported"}
23  {"23-Int 13h - 5.25 /1.2MB Floppy Services are supported"}
24  {"24-Int 13h - 3.5 / 720 KB Floppy Services are supported"}
25  {"25-Int 13h - 3.5 / 2.88 MB Floppy Services are supported"}
26  {"26-Int 5h, Print Screen Service is supported"}
27  {"27-Int 9h, 8042 Keyboard services are supported"}
28  {"28-Int 14h, Serial Services are supported"}
29  {"29-Int 17h, printer services are supported"}
30  {"30-Int 10h, CGA/Mono Video Services are supported"}
31  {"31-NEC PC-98"}
32  {"32-ACPI supported"}
33  {"33-USB Legacy is supported"}
34  {"34-AGP is supported"}
35  {"35-I2O boot is supported"}
36  {"36-LS-120 boot is supported"}
37  {"37-ATAPI ZIP Drive boot is supported"}
38  {"38-1394 boot is supported"}
39  {"39-Smart Battery supported"}
}
Return
}

If ($char -ge 40 -and $char -le 45) {
          "{0}-Reserved for BIOS vendor" -f $char
return
}

If ($char -ge 48 -and $char -le 63) {
           "{0}-Reserved for system vendor" -f $char
return
}
"{0}-Unknown Value " -f $char
}

# Get BIOS information from WMI
$bios = Get-WMIObject Win32_Bios

# Display BIOS Details
"Win32_Bios WMI Information"
"Bios Characteristics"
foreach ($ch in $bios.BiosCharacteristics) {
"                      :  {0}" -f  (Get-WmiBiosCharacteristics($ch))
} 
"Bios Version          :  {0}" -f $bios.BiosVersion
"Codeset               :  {0}" -f $bios.Codeset
"CurrentLanguage       :  {0}" -f $bios.CurrentLanguage
"Description           :  {0}" -f $bios.Description
"IdentificatonCode     :  {0}" -f $bios.IdentificatonCode
"InstallableLanguages  :  {0}" -f $bios.InstallableLanguages
"InstallDate           :  {0}" -f $bios.InstallDate 
"LanguageEdition       :  {0}" -f $bios.LanguageEdition
"ListOfLanguages       :  {0}" -f $bios.ListOfLanguages
"Manufacturer          :  {0}" -f $bios.Manufacturer
"OtherTargetOS         :  {0}" -f $bios.OtherTargetOS
"PrimaryBIOS           :  {0}" -f $bios.PrimaryBIOS
"ReleaseDate           :  {0}" -f $bios.ReleaseDate
"SerialNumber          :  {0}" -f $bios.SerialNumber
"SMBIOSBIOSVersion     :  {0}" -f $bios.SMBIOSBIOSVersion
"SMBIOSMajorVersion    :  {0}" -f $bios.SMBIOSMajorVersion
"SMBIOSMinorVersion    :  {0}" -f $bios.SMBIOSMinorVersion
"SoftwareElementID     :  {0}" -f $bios.SoftwareElementID 
"SoftwareElementState  :  {0}" -f $bios.SoftwareElementState
"TargetOperatingSystem :  {0}" -f $bios.TargetOperatingSystem
"Version               :  {0}" -f $bios.Version 
```



<span data-ttu-id="152a0-454">先前的程式碼範例會傳回下列資訊：</span><span class="sxs-lookup"><span data-stu-id="152a0-454">The previous code sample returns the following information:</span></span>

``` syntax
Win32_Bios WMI Information
Bios Characteristics
                      :  04-ISA is supported
                      :  07-PCI is supported
                      :  08-PC Card (PCMCIA) is supported
                      :  09-Plug and Play is supported
                      :  11-BIOS is Upgradable (Flash)
                      :  12-BIOS shadowing is allowed
                      :  15-Boot from CD is supported
                      :  16-Selectable Boot is supported
                      :  24-Int 13h - 3.5 / 720 KB Floppy Services are supported
                      :  26-Int 5h, Print Screen Service is supported
                      :  27-Int 9h, 8042 Keyboard services are supported
                      :  28-Int 14h, Serial Services are supported
                      :  29-Int 17h, printer services are supported
                      :  30-Int 10h, CGA/Mono Video Services are supported
                      :  32-ACPI supported
                      :  33-USB Legacy is supported
                      :  34-AGP is supported
                      :  39-Smart Battery supported
                      :  40-Reserved for BIOS vendor
                      :  41-Reserved for BIOS vendor
                      :  42-Reserved for BIOS vendor
                      :  58-Reserved for system vendor
                      :  74-Unknown Value
Bios Version          :  DELL   - 27d60a0d
Codeset               :
CurrentLanguage       :  en|US|iso8859-1
Description           :  Phoenix ROM BIOS PLUS Version 1.10 A04
IdentificatonCode     :
InstallableLanguages  :  1
InstallDate           :
LanguageEdition       :
ListOfLanguages       :  en|US|iso8859-1
Manufacturer          :  Dell Inc.
OtherTargetOS         :
PrimaryBIOS           :  True
ReleaseDate           :  20061013000000.000000+000
SerialNumber          :  DDC2H2J
SMBIOSBIOSVersion     :  A04
SMBIOSMajorVersion    :  2
SMBIOSMinorVersion    :  4
SoftwareElementID     :  Phoenix ROM BIOS PLUS Version 1.10 A04
SoftwareElementState  :  3
TargetOperatingSystem :  0
Version               :  DELL   - 27d60a0d
```

## <a name="requirements"></a><span data-ttu-id="152a0-455">規格需求</span><span class="sxs-lookup"><span data-stu-id="152a0-455">Requirements</span></span>



| <span data-ttu-id="152a0-456">需求</span><span class="sxs-lookup"><span data-stu-id="152a0-456">Requirement</span></span> | <span data-ttu-id="152a0-457">值</span><span class="sxs-lookup"><span data-stu-id="152a0-457">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="152a0-458">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="152a0-458">Minimum supported client</span></span><br/> | <span data-ttu-id="152a0-459">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="152a0-459">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="152a0-460">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="152a0-460">Minimum supported server</span></span><br/> | <span data-ttu-id="152a0-461">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="152a0-461">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="152a0-462">命名空間</span><span class="sxs-lookup"><span data-stu-id="152a0-462">Namespace</span></span><br/>                | <span data-ttu-id="152a0-463">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="152a0-463">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="152a0-464">MOF</span><span class="sxs-lookup"><span data-stu-id="152a0-464">MOF</span></span><br/>                      | <dl> <span data-ttu-id="152a0-465"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="152a0-465"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="152a0-466">DLL</span><span class="sxs-lookup"><span data-stu-id="152a0-466">DLL</span></span><br/>                      | <dl> <span data-ttu-id="152a0-467"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="152a0-467"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152a0-468">另請參閱</span><span class="sxs-lookup"><span data-stu-id="152a0-468">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152a0-469">**CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="152a0-469">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="152a0-470">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="152a0-470">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


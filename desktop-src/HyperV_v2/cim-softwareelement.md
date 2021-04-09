---
description: 代表 CIM SoftwareFeature 可個別管理或可部署的部分 \_ 。
ms.assetid: 96affc55-b001-4122-b883-3610bf95a786
title: 'CIM_SoftwareElement 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.Version
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.LanguageEdition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1d11b428e9a17819f850ce210e6854e4f1d17e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694255"
---
# <a name="cim_softwareelement-class-hyper-v-management"></a>CIM_SoftwareElement 類別 (Hyper-v 管理) 

代表 **CIM \_ SoftwareFeature** 可個別管理或可部署的部分。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Application::DeploymentModel"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string Name;
  string Version;
  uint16 SoftwareElementState;
  string SoftwareElementID;
  uint16 TargetOperatingSystem;
  string OtherTargetOS;
  string Manufacturer;
  string BuildNumber;
  string SerialNumber;
  string CodeSet;
  string IdentificationCode;
  string LanguageEdition;
};
```

## <a name="members"></a>成員

**CIM \_ SoftwareElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ SoftwareElement** 類別具有這些屬性。

<dl> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| Software Component Information \| 002.4 ") 
</dt> </dl>

軟體元素編譯的內部識別碼。

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

Software 元素所使用的字元編碼，例如 UTF-8 和 ISO8859-1。

</dd> <dt>

**IdentificationCode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 子元件軟體 \| 001.6 ") 
</dt> </dl>

Software 元素的製造商識別碼。 這通常是庫存單位 (SKU) 或元件編號。

</dd> <dt>

**LanguageEdition**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 子元件軟體 \| 001.7 ") 
</dt> </dl>

軟體元素的語言版本。 應使用 ISO 639 標準中所定義的語言代碼。 如果專案代表多語言或國際版本，則應該使用「多語系」字串。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 子元件軟體 \| 001.3 ") 
</dt> </dl>

軟體元素的製造商。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

用來識別軟體元素的名稱。

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ 作業系統**](/windows/desktop/CIMWin32Prov/cim-operatingsystem)。**OtherTypeDescription**") 
</dt> </dl>

當 [ **TargetOperatingSystem** ] 屬性設定為 [ **其他** ( "1" ) 時，製造商和作業系統類型。

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.4 ") 
</dt> </dl>

軟體元素的指派序號。

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

要與其他金鑰搭配使用，以建立唯一識別專案的 software 專案識別碼。

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

軟體專案的生命週期狀態。

\- 可部署狀態的 SoftwareElement 會描述成功散發它所需的詳細資料，以及將其移至可安裝狀態所需的詳細資料 (檢查和動作)  (也就是下一個狀態) 。

\- [可安裝] 狀態中的 SoftwareElement 會描述成功安裝它所需的詳細資料，以及在可執行狀態中建立元素所需的詳細資料 (檢查和動作)  (也就是下一個狀態) 。

\- 可執行檔狀態中的 SoftwareElement 會描述成功啟動它所需的詳細資料，以及將其移至執行中狀態所需的詳細資料 (檢查和動作)  (也就是下一個狀態) 。

\- 處於執行中狀態的 SoftwareElement 會描述管理已啟動元素所需的詳細資料。

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

可 **部署** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

可 **安裝** 的 (1) 


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

**可執行檔** (2) 


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**正在** 執行 (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 子元件 Software \| 001.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ 作業系統**](/windows/desktop/CIMWin32Prov/cim-operatingsystem)。**OSType**") 
</dt> </dl>

Software 元素的作業系統。 這個屬性的值不確定它是否為二進位可執行檔。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

**MACOS** (2) 


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

**ATTUNIX** (3) 


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

**DGUX** (4) 


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

**DECNT** (5) 


</dt> <dd></dd> <dt>

<span id="Tru64_UNIX"></span><span id="tru64_unix"></span><span id="TRU64_UNIX"></span>

**TRU64 UNIX** (6) 


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

**OpenVMS** (7) 


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

**HPUX** (8) 


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

**AIX** (9) 


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

**MVS** (10) 


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

**OS400** (11) 


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

**OS/2** (12) 


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

**JAVAVM** (13) 


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

**Msdos.sys** (14) 


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

**WIN3x** (15) 


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

**WIN95** (16) 


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

**WIN98** (17) 


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

**WINNT** (18) 


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

**WINCE** (19) 


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

**NCR3000** (20) 


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

**NetWare** (21) 


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

**憑證** (22) 


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

**DC/OS** (23) 


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

相依 **UNIX** (24) 


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

**SCO UnixWare** (25) 


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

**SCO OpenServer** (26) 


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

**Sequent** (27) 


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

**IRIX** (28) 


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

**Solaris** (29) 


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

**SunOS** (30) 


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

**U6000** (31) 


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

**ASERIES** (32) 


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OS"></span><span id="hp_nonstop_os"></span><span id="HP_NONSTOP_OS"></span>

**HP 持續作業系統** (33) 


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OSS"></span><span id="hp_nonstop_oss"></span><span id="HP_NONSTOP_OSS"></span>

**HP 持續 OSS** (34) 


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

**BS2000** (35) 


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

**LINUX** (36) 


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

**Lynx** (37) 


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

**XENIX** (38) 


</dt> <dd></dd> <dt>

<span id="VM"></span><span id="vm"></span>

**VM** (39) 


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

**互動式 UNIX** (40) 


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

**BSDUNIX** (41) 


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

**FreeBSD** (42) 


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

**NetBSD** (43) 


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

**GNU Hurd** (44) 


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

**OS9** (45) 


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

**符合 Kernel** (46) 


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

**Inferno** (47) 


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

**QNX** (48) 


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

**EPOC** (49) 


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

**IxWorks** (50) 


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

**VxWorks** (51) 


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

**MiNT** (52) 


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

**BeOS** (53) 


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

**HP MPE** (54) 


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

**NextStep** (55) 


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

**PalmPilot** (56) 


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

**Rhapsody** (57) 


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

**Windows 2000** (58) 


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

**專用** (59) 


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

**OS/390** (60) 


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

**VSE** (61) 


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

**TPF** (62) 


</dt> <dd></dd> <dt>

<span id="Windows__R__Me"></span><span id="windows__r__me"></span><span id="WINDOWS__R__ME"></span>

**Windows (R) Me** (63) 


</dt> <dd></dd> <dt>

<span id="Caldera_Open_UNIX"></span><span id="caldera_open_unix"></span><span id="CALDERA_OPEN_UNIX"></span>

**Caldera OPEN UNIX** (64) 


</dt> <dd></dd> <dt>

<span id="OpenBSD"></span><span id="openbsd"></span><span id="OPENBSD"></span>

**OpenBSD** (65) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (66) 


</dt> <dd></dd> <dt>

<span id="Windows_XP"></span><span id="windows_xp"></span><span id="WINDOWS_XP"></span>

**WINDOWS XP** (67) 


</dt> <dd></dd> <dt>

<span id="z_OS"></span><span id="z_os"></span><span id="Z_OS"></span>

**z/OS** (68) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003"></span><span id="microsoft_windows_server_2003"></span><span id="MICROSOFT_WINDOWS_SERVER_2003"></span>

**Microsoft Windows Server 2003** (69) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003_64-Bit"></span><span id="microsoft_windows_server_2003_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2003_64-BIT"></span>

**Microsoft Windows Server 2003 64 位** (70) 


</dt> <dd></dd> <dt>

<span id="Windows_XP_64-Bit"></span><span id="windows_xp_64-bit"></span><span id="WINDOWS_XP_64-BIT"></span>

**WINDOWS XP 64 位** (71) 


</dt> <dd></dd> <dt>

<span id="Windows_XP_Embedded"></span><span id="windows_xp_embedded"></span><span id="WINDOWS_XP_EMBEDDED"></span>

**WINDOWS XP Embedded** (72) 


</dt> <dd></dd> <dt>

<span id="Windows_Vista"></span><span id="windows_vista"></span><span id="WINDOWS_VISTA"></span>

**Windows Vista** (73) 


</dt> <dd></dd> <dt>

<span id="Windows_Vista_64-Bit"></span><span id="windows_vista_64-bit"></span><span id="WINDOWS_VISTA_64-BIT"></span>

**Windows Vista 64 位** (74) 


</dt> <dd></dd> <dt>

<span id="Windows_Embedded_for_Point_of_Service"></span><span id="windows_embedded_for_point_of_service"></span><span id="WINDOWS_EMBEDDED_FOR_POINT_OF_SERVICE"></span>

**Windows Embedded For Point Of Service** (75) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008"></span><span id="microsoft_windows_server_2008"></span><span id="MICROSOFT_WINDOWS_SERVER_2008"></span>

**Microsoft Windows Server 2008** (76) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_64-Bit"></span><span id="microsoft_windows_server_2008_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_64-BIT"></span>

**Microsoft Windows Server 2008 64 位** (77) 


</dt> <dd></dd> <dt>

<span id="FreeBSD_64-Bit"></span><span id="freebsd_64-bit"></span><span id="FREEBSD_64-BIT"></span>

**FreeBSD 64** 位 (78) 


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux"></span><span id="redhat_enterprise_linux"></span><span id="REDHAT_ENTERPRISE_LINUX"></span>

**RedHat Enterprise Linux** (79) 


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux_64-Bit"></span><span id="redhat_enterprise_linux_64-bit"></span><span id="REDHAT_ENTERPRISE_LINUX_64-BIT"></span>

**RedHat Enterprise Linux 64** 位 (80) 


</dt> <dd></dd> <dt>

<span id="Solaris_64-Bit"></span><span id="solaris_64-bit"></span><span id="SOLARIS_64-BIT"></span>

**Solaris 64** 位 (81) 


</dt> <dd></dd> <dt>

<span id="SUSE"></span><span id="suse"></span>

**SUSE** (82) 


</dt> <dd></dd> <dt>

<span id="SUSE_64-Bit"></span><span id="suse_64-bit"></span><span id="SUSE_64-BIT"></span>

**SUSE 64** 位 (83) 


</dt> <dd></dd> <dt>

<span id="SLES"></span><span id="sles"></span>

**SLES** (84) 


</dt> <dd></dd> <dt>

<span id="SLES_64-Bit"></span><span id="sles_64-bit"></span><span id="SLES_64-BIT"></span>

**SLES 64** 位 (85) 


</dt> <dd></dd> <dt>

<span id="Novell_OES"></span><span id="novell_oes"></span><span id="NOVELL_OES"></span>

**NOVELL OES** (86) 


</dt> <dd></dd> <dt>

<span id="Novell_Linux_Desktop"></span><span id="novell_linux_desktop"></span><span id="NOVELL_LINUX_DESKTOP"></span>

**Novell Linux Desktop** (87) 


</dt> <dd></dd> <dt>

<span id="Sun_Java_Desktop_System"></span><span id="sun_java_desktop_system"></span><span id="SUN_JAVA_DESKTOP_SYSTEM"></span>

**Sun JAVA Desktop System** (88) 


</dt> <dd></dd> <dt>

<span id="Mandriva"></span><span id="mandriva"></span><span id="MANDRIVA"></span>

**Mandriva** (89) 


</dt> <dd></dd> <dt>

<span id="Mandriva_64-Bit"></span><span id="mandriva_64-bit"></span><span id="MANDRIVA_64-BIT"></span>

**Mandriva 64** 位 (90) 


</dt> <dd></dd> <dt>

<span id="TurboLinux"></span><span id="turbolinux"></span><span id="TURBOLINUX"></span>

**TurboLinux** (91) 


</dt> <dd></dd> <dt>

<span id="TurboLinux_64-Bit"></span><span id="turbolinux_64-bit"></span><span id="TURBOLINUX_64-BIT"></span>

**TurboLinux 64** 位 (92) 


</dt> <dd></dd> <dt>

<span id="Ubuntu"></span><span id="ubuntu"></span><span id="UBUNTU"></span>

**Ubuntu** (93) 


</dt> <dd></dd> <dt>

<span id="Ubuntu_64-Bit"></span><span id="ubuntu_64-bit"></span><span id="UBUNTU_64-BIT"></span>

**Ubuntu 64** 位 (94) 


</dt> <dd></dd> <dt>

<span id="Debian"></span><span id="debian"></span><span id="DEBIAN"></span>

**Debian** (95) 


</dt> <dd></dd> <dt>

<span id="Debian_64-Bit"></span><span id="debian_64-bit"></span><span id="DEBIAN_64-BIT"></span>

**Debian 64** 位 (96) 


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x"></span><span id="linux_2.4.x"></span><span id="LINUX_2.4.X"></span>

**Linux 2.4. x** (97) 


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x_64-Bit"></span><span id="linux_2.4.x_64-bit"></span><span id="LINUX_2.4.X_64-BIT"></span>

**Linux 2.4. x 64** 位 (98) 


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x"></span><span id="linux_2.6.x"></span><span id="LINUX_2.6.X"></span>

**Linux 2.6. x** (99) 


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x_64-Bit"></span><span id="linux_2.6.x_64-bit"></span><span id="LINUX_2.6.X_64-BIT"></span>

**Linux 2.6. x 64** 位 (100) 


</dt> <dd></dd> <dt>

<span id="Linux_64-Bit"></span><span id="linux_64-bit"></span><span id="LINUX_64-BIT"></span>

**Linux 64** 位 (101) 


</dt> <dd></dd> <dt>

<span id="Other_64-Bit"></span><span id="other_64-bit"></span><span id="OTHER_64-BIT"></span>

**其他 64** 位 (102) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_R2"></span><span id="microsoft_windows_server_2008_r2"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_R2"></span>

**Microsoft Windows Server 2008 R2** (103) 


</dt> <dd></dd> <dt>

<span id="VMware_ESXi"></span><span id="vmware_esxi"></span><span id="VMWARE_ESXI"></span>

**VMware ESXi** (104) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_7"></span><span id="microsoft_windows_7"></span><span id="MICROSOFT_WINDOWS_7"></span>

**Microsoft Windows 7** (105) 


</dt> <dd></dd> <dt>

<span id="CentOS_32-bit"></span><span id="centos_32-bit"></span><span id="CENTOS_32-BIT"></span>

**CentOS 32** 位 (106) 


</dt> <dd></dd> <dt>

<span id="CentOS_64-bit"></span><span id="centos_64-bit"></span><span id="CENTOS_64-BIT"></span>

**CentOS 64** 位 (107) 


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_32-bit"></span><span id="oracle_enterprise_linux_32-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_32-BIT"></span>

**Oracle Enterprise Linux 32** 位 (108) 


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_64-bit"></span><span id="oracle_enterprise_linux_64-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_64-BIT"></span>

**Oracle Enterprise Linux 64** 位 (109) 


</dt> <dd></dd> <dt>

<span id="eComStation_32-bitx"></span><span id="ecomstation_32-bitx"></span><span id="ECOMSTATION_32-BITX"></span>

**eComStation 32-bitx** (110) 


</dt> <dd></dd> </dl>

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 子元件軟體 \| 001.4 ") 
</dt> </dl>

格式為的軟體 *<Major>* 版本。 *<Minor>**<Revision>* 或 *<Major>* 。 *<Minor><letter><revision>*

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 


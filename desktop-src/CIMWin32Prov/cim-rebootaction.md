---
description: CIM \_ RebootAction 類別會導致系統重新開機，其中安裝了 software 元素。
ms.assetid: 4da5f0b0-3c09-4dd6-b821-43953f629829
ms.tgt_platform: multiple
title: CIM_RebootAction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RebootAction
- CIM_RebootAction.ActionID
- CIM_RebootAction.Caption
- CIM_RebootAction.Description
- CIM_RebootAction.Direction
- CIM_RebootAction.Name
- CIM_RebootAction.SoftwareElementID
- CIM_RebootAction.SoftwareElementState
- CIM_RebootAction.TargetOperatingSystem
- CIM_RebootAction.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 88cfbd66c21abbc46b05da706ebe2ff6125d1f87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936117"
---
# <a name="cim_rebootaction-class"></a>CIM \_ RebootAction 類別

**CIM \_ RebootAction** 類別會導致系統重新開機，其中安裝了 software 元素。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[UUID("{AB08D884-DB30-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_RebootAction : CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
};
```

## <a name="members"></a>成員

**CIM \_ RebootAction** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ RebootAction** 類別具有這些方法。



| 方法                                                    | 描述                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------|
| [**調用**](invoke-method-in-class-cim-rebootaction.md) | 採取特定動作。 不是由 WMI 所執行。<br/> |



 

### <a name="properties"></a>屬性

**CIM \_ RebootAction** 類別具有這些屬性。

<dl> <dt>

**ActionID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

指派給軟體元素特定動作的唯一識別碼。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

</dd> <dt>

[方向]
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出特定 [**CIM \_ 動作**](cim-action.md) 物件是否為一連串動作的一部分，以將目前的軟體專案轉換為下一個狀態，例如 "Install"，或移除目前的 software 元素，例如 "Uninstall"。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

**安裝** (0) 


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

**卸載** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

識別軟體元素。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

Software 元素的識別碼。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

軟體元素的狀態。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) 


</dt> <dd>

描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) 


</dt> <dd>

描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) 


</dt> <dd>

描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) 


</dt> <dd>

描述監視和操作開始專案所需的詳細資料。

</dd> </dl>

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") 
</dt> </dl>

擁有軟體元素的目標作業系統。

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MACOS** (2) 


</dt> <dd>

Mac OS

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) 


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) 


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) 


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) 


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) 


</dt> <dd>

開啟 VM

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) 


</dt> <dd>

HP-UX

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span id="AIX"></span><span id="aix"></span>**AIX** (9) 


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span id="MVS"></span><span id="mvs"></span>**MVS** (10) 


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span id="OS400"></span><span id="os400"></span>**OS400** (11) 


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) 


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) 


</dt> <dd>

適用于 JAVA 的 Microsoft 虛擬機器 (VM) 

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) 


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) 


</dt> <dd>

Windows 3。x

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**WIN95** (16) 


</dt> <dd>

Windows 95

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**WIN98** (17) 


</dt> <dd>

Windows 98

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) 


</dt> <dd>

Windows NT

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WINCE** (19) 


</dt> <dd>

Windows CE

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) 


</dt> <dd>

NCR 3000

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) 


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span id="OSF"></span><span id="osf"></span>**憑證** (22) 


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) 


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) 


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) 


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) 


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) 


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span id="IRIX"></span><span id="irix"></span>**IRIX** (28) 


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) 


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) 


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31) 


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) 


</dt> <dd>

系列

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) 


</dt> <dd>

串聯 NSK

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) 


</dt> <dd>

將 NT

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) 


</dt> <dd>

BS2000/OSD

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**LINUX** (36) 


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) 


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) 


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) 


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) 


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) 


</dt> <dd>

BSD UNIX

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) 


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) 


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) 


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**OS9** (45) 


</dt> <dd>

Mac OS 9

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) 


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) 


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**QNX** (48) 


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) 


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) 


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) 


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) 


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) 


</dt> <dd>

為 OS

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) 


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) 


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) 


</dt> <dd>

掌上作業系統

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) 


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) 


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) 


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (60) 


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (61) 


</dt> <dd></dd> </dl>

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") 
</dt> </dl>

作業的版本。

作業的版本應該採用下列其中一種形式：

-   <major>.<minor>.<revision>
-   <major>.<minor><letter><revision>

這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 動作**](cim-action.md)
</dt> </dl>

 


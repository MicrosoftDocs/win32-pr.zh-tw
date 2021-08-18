---
title: 'GUESTOSVERSIONINFOEX 結構 (VPCCOMInterfaces .h) '
description: 包含客體作業系統的作業系統版本資訊。
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX 結構虛擬電腦
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848196448c2bd6f021d85f7c13972e81664dd60a0e4a0bbbd2e05ef3455aade7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056906"
---
# <a name="guestosversioninfoex-structure"></a>GUESTOSVERSIONINFOEX 結構

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

包含客體作業系統的作業系統版本資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a>成員

<dl> <dt>

**dwOSVersionInfoSize**
</dt> <dd>

此資料結構的大小（以位元組為單位）。 將這個成員設定為 `sizeof(GUESTOSVERSIONINFOEX)` 。

</dd> <dt>

**dwMajorVersion**
</dt> <dd>

主要版本號碼。

</dd> <dt>

**dwMinorVersion**
</dt> <dd>

次要版本號碼。

</dd> <dt>

**dwBuildNumber**
</dt> <dd>

組建編號。

</dd> <dt>

**dwPlatformId**
</dt> <dd>

作業系統平臺。 此成員可以是 **\_ PLATFORM \_ WIN32 \_ NT** (2) 。

</dd> <dt>

**szCSDVersion**
</dt> <dd>

以 null 終止的字串，例如 "Service Pack 3"，表示系統上安裝的最新 Service Pack。 如果未安裝 Service Pack，則字串是空的。

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

已安裝最新 Service Pack 的主要版本號碼。

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

已安裝最新 Service Pack 的次要版本號碼。

</dd> <dt>

**wSuiteMask**
</dt> <dd>

識別系統上可用之產品套件的位元遮罩。 這個成員可以是下列值的組合。



| 值                                                                                                                                                                                                                                                                                          | 意義                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**VER \_SUITE \_ BACKOFFICE**</dt> <dt>0x00000004</dt> </dl>                                            | 已安裝 Microsoft BackOffice 元件。<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**VER \_SUITE \_ BLADE**</dt> <dt>0x00000400</dt> </dl>                                                           | Windows伺服器2003，Web Edition 已安裝。<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**VER \_SUITE \_ COMPUTE \_ SERVER**</dt> <dt>0x00004000</dt> </dl>                               | Windows已安裝 Server 2003、Compute Cluster Edition。<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**VER \_SUITE \_ DATACENTER**</dt> <dt>0x00000080</dt> </dl>                                            | Windows已安裝 server 2008 datacenter、Windows server 2003、datacenter Edition 或 Windows 2000 datacenter Server。<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**VER \_SUITE \_ 企業**</dt> <dt>0x00000002</dt> </dl>                                            | Windows已安裝 Server 2008 Enterprise、Windows server 2003、Enterprise Edition 或 Windows 2000 Advanced Server。 如需此位旗標的詳細資訊，請參閱「備註」一節。<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**VER \_SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows已安裝 XP Embedded。<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**VER \_SUITE \_ 個人**</dt> <dt>0x00000200</dt> </dl>                                                  | Windowsvista home 進階版、Windows vista home Basic 或 Windows XP home Edition 皆已安裝。<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**VER \_SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | 支援遠端桌面，但只支援一個互動式會話。 除非系統是在應用程式伺服器模式中執行，否則會設定此值。<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**VER \_SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server 已安裝在系統上，但可能已升級至另一個版本的 Windows。 如需此位旗標的詳細資訊，請參閱「備註」一節。<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**VER \_SUITE \_ SMALLBUSINESS \_ 受限**</dt>的 <dt>0x00000020</dt> </dl> | Microsoft Small Business Server 會以強制的嚴格用戶端授權安裝。 如需此位旗標的詳細資訊，請參閱「備註」一節。<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**VER \_SUITE \_ STORAGE \_ SERVER**</dt> <dt>0x00002000</dt> </dl>                               | Windows 已安裝儲存體 server 2003 R2 或 Windows 儲存體 server 2003is。<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**VER \_SUITE \_ 終端**</dt> <dt>0x00000010</dt> </dl>                                                  | 已安裝終端機服務。 一律會設定這個值。<br/> 如果設定了 **ver \_ suite \_ 終端** 機，但未設定 **ver \_ suite \_ SINGLEUSERTS** ，系統就會在應用程式伺服器模式中執行。<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**VER \_SUITE \_ WH \_ 伺服器**</dt> <dt>0x00008000</dt> </dl>                                              | Windows已安裝 Home Server。<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

系統的任何其他資訊。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**VER \_NT \_ 域 \_ 控制器**</dt> <dt>0x0000002</dt> </dl> | 系統是網域控制站，而作業系統是 Windows Server 2008 r2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**VER \_NT \_ 伺服器**</dt> <dt>0x0000003</dt> </dl>                                   | 作業系統是 Windows Server 2008 r2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。<br/> 請注意，同時也是網域控制站的伺服器會回報為 **ver \_ nt \_ 域 \_ 控制器**，而不是 **\_ nt \_ server**。<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**VER \_NT \_ 工作站**</dt> <dt>0x0000001</dt> </dl>                    | 作業系統是 Windows 7、Windows Vista、Windows XP 或 Windows 2000 Professional。<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

保留供未來使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 


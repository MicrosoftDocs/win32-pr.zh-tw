---
description: 包含印表機驅動程式資訊。
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: 'DRIVER_INFO_8 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320612"
---
# <a name="driver_info_8-structure"></a>驅動程式 \_ 資訊 \_ 8 結構

包含印表機驅動程式資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DRIVER_INFO_8 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a>成員

<dl> <dt>

**cVersion**
</dt> <dd>

寫入驅動程式的作業系統版本。 支援的值為3。

</dd> <dt>

**pName**
</dt> <dd>

以 null 結束的字串指標，指定驅動程式的名稱 (例如，QMS 810) 。

</dd> <dt>

**pEnvironment**
</dt> <dd>

以 null 結束的字串指標，指定驅動程式所撰寫的環境 (例如，Windows x86、Windows IA64 和 Windows x64。

</dd> <dt>

**pDriverPath**
</dt> <dd>

以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\Pscript.dll) 。

</dd> <dt>

**pDataFile**
</dt> <dd>

以 null 結束的字串指標，這個字串會指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Qms810) 。

</dd> <dt>

**pConfigFile**
</dt> <dd>

以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 C： \\ 驅動程式 \\Pscrptui.dll) 。

</dd> <dt>

**pHelpFile**
</dt> <dd>

以 null 結束的字串指標，指定設備磁碟機的說明檔的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Pscrptui .hlp) 。

</dd> <dt>

**pDependentFiles**
</dt> <dd>

MultiSZ 緩衝區的指標，其中包含以 null 終止之字串的序列。 緩衝區中每個以 null 結束的字串都包含驅動程式相依的檔案名。 字串序列會以空的零長度字串來終止。 如果 **pDependentFiles** 不是 **Null** ，而且不包含任何檔案名，則會指向包含兩個空字串的緩衝區。

</dd> <dt>

**pMonitorName**
</dt> <dd>

指定語言監視器 (之以 null 結束的字串指標，例如「PJL 監視器」 ) 。 這個成員可以是 **Null** ，而且只能針對能夠進行雙向通訊的印表機指定。

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

以 null 結束的字串指標，指定列印工作的預設資料類型 (例如 "EMF" ) 。

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

以 null 結束的字串指標，這個字串會指定與此驅動程式相容的先前印表機驅動程式名稱。 例如，OldName1 \\ 0OldName2 \\ 0 \\ 0。

</dd> <dt>

**ftDriverDate**
</dt> <dd>

驅動程式套件的日期，以驅動程式檔案中的程式碼為程式碼。

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

驅動程式的版本號碼。 這是來自驅動程式的版本結構。

</dd> <dt>

**pszMfgName**
</dt> <dd>

指定制造商名稱之以 null 結束的字串指標。

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

指定制造商 URL 之以 null 結束的字串指標。

</dd> <dt>

**pszHardwareID**
</dt> <dd>

以 null 結束的字串指標，指定印表機驅動程式的硬體識別碼。

</dd> <dt>

**pszProvider**
</dt> <dd>

以 null 結束的字串指標，指定印表機驅動程式的提供者 (例如「Microsoft Windows 2000」 ) 。

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

以 null 結束的字串指標，指定列印處理器 (例如 "WinPrint" ) 。

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

以 null 結束的字串指標，指定廠商的驅動程式安裝 DLL 和進入點。

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

以 null 結束的字串指標，指定與驅動程式相關聯的色彩設定檔。

</dd> <dt>

**pszInfPath**
</dt> <dd>

以 null 結束的字串指標，指定驅動程式的 .inf 檔案在驅動程式存放區中的路徑。  (請參閱 [備註]。如果要將驅動程式 \_ 資訊 \_ 8 傳遞給 [**AddPrinterDriver**](addprinterdriver.md)或 [**AddPrinterDriverEx**](addprinterdriverex.md)，請 ) 此值必須是 Null。

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

印表機驅動程式的屬性旗標。 如果即將將驅動程式 \_ 資訊 \_ 8 傳遞給 [**AddPrinterDriver**](addprinterdriver.md) 或 [**AddPrinterDriverEx**](addprinterdriverex.md)，這就必須是0。 否則，它可以是下列旗標的任意組合：



| 旗標名稱/值                                                         | 意義                                                                                                                                                                                                                                                                                                                                             | 最低 OS                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| 印表機 \_ 驅動程式 \_ 套件 \_ 感知<br/> 0x00000001<br/>        | 印表機驅動程式是驅動程式套件的一部分。                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| 印表機 \_ 驅動程式 \_ XPS<br/> 0x00000002<br/>                   | 印表機驅動程式支援 [XML 檔規格：總覽](/previous-versions/windows/hardware/design/dn641615(v=vs.85))和產品行為中所述的 Microsoft XPS 格式 [，<27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)。                        | Windows 8<br/> Windows Server 2012<br/>    |
| 印表機 \_ 驅動程式 \_ 沙箱 \_ 已啟用<br/> 0x00000004<br/>      | 印表機驅動程式與 [印表機驅動程式隔離](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)相容。 如需詳細資訊，請參閱 [產品行為 <28>一節 ](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)。 | Windows 7<br/> Windows Server 2008 R2<br/> |
| 印表機 \_ 驅動程式 \_ 類別<br/> 0x00000008<br/>                 | 印表機驅動程式是 [類別的印表機驅動程式](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)。                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| 衍生的印表機 \_ 驅動程式 \_<br/> 0x00000010<br/>               | 印表機驅動程式是 [衍生的印表機驅動程式](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)。                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| 印表機 \_ 驅動程式 \_ 無法 \_ 共用<br/> 0x00000020<br/>        | 無法共用使用此印表機驅動程式的印表機。                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| 印表機 \_ 驅動程式 \_ 類別 \_ 傳真<br/> 0x00000040<br/>         | 印表機驅動程式的目的是要與 [傳真印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)搭配使用。                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| 印表機 \_ 驅動程式 \_ 類別檔案 \_<br/> 0x00000080<br/>        | 印表機驅動程式的目的是要與檔案 [印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)搭配使用。                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| 印表機 \_ 驅動程式 \_ 類別 \_ 虛擬<br/> 0x00000100<br/>     | 印表機驅動程式的目的是要搭配 [虛擬印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)使用。                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| 印表機 \_ 驅動程式 \_ 類別 \_ 服務<br/> 0x00000200<br/>     | 印表機驅動程式的目的是要與 [服務印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)一起使用。                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_需要印表機驅動程式 \_ 軟 \_ 重設 \_<br/> 0x00000400<br/> | 使用此印表機驅動程式的印表機應遵循 USB 裝置類別定義中所述的指導方針。 如需詳細資訊，請參閱 [產品行為，第 <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

以 null 終止的多字串指標，指定驅動程式相依的所有核心印表機驅動程式。 如果即將將 **驅動程式 \_ 資訊 \_ 8** 傳遞給 [**AddPrinterDriver**](addprinterdriver.md)或 [**AddPrinterDriverEx**](addprinterdriverex.md)，這就必須是 **Null** 。

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

Windows 隨附的任何驅動程式和此驅動程式相依的最早允許日期。

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

隨附于 Windows 以及此驅動程式所相依之任何驅動程式的最早允許版本。

</dd> </dl>

## <a name="remarks"></a>備註

這些成員的字串包含在用來新增驅動程式的 .inf 檔案中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 驅動程式 \_ 資訊 \_ 8W** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 8A** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 


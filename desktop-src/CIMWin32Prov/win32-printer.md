---
description: 代表連接到在 Microsoft Windows 作業系統上執行之電腦的裝置，該電腦可在紙張或其他媒體上產生列印的影像或文字。
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Win32_Printer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f1a91ac90560343a38e546590005e8b984d13843eba8195381daa204e2d22cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077308"
---
# <a name="win32_printer-class"></a>Win32 \_ 印表機類別

**Win32 \_ 印表機** [WMI 類別](../wmisdk/retrieving-a-class.md)代表連接到在 Microsoft Windows 作業系統上執行之電腦的裝置，該電腦可在紙張或其他媒體上產生列印的影像或文字。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a>成員

**Win32 \_ 印表機** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ 印表機** 類別有這些方法。



| 方法                                                                               | 描述                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddPrinterConnection**](addprinterconnection-method-in-class-win32-printer.md)   | 將連接新增至印表機。<br/>                                                                                                                                                                      |
| [**CancelAllJobs**](cancelalljobs-method-in-class-win32-printer.md)                 | 取消所有作業。<br/>                                                                                                                                                                                      |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-printer.md) | 傳回控制印表機存取的安全描述項。<br/>                                                                                                                                   |
| [**暫停**](pause-method-in-class-win32-printer.md)                                 | 暫停列印佇列。<br/>                                                                                                                                                                                |
| [**PrintTestPage**](printtestpage-method-in-class-win32-printer.md)                 | 列印測試頁面。<br/>                                                                                                                                                                                    |
| [**RenamePrinter**](renameprinter-method-in-class-win32-printer.md)                 | 重新命名印表機。<br/>                                                                                                                                                                                     |
| **重設**                                                                            | 未實作。 如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ 印表機**](cim-printer.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。<br/>                 |
| [**繼續**](resume-method-in-class-win32-printer.md)                               | 繼續暫停的列印佇列。<br/>                                                                                                                                                                            |
| [**SetDefaultPrinter**](setdefaultprinter-method-in-class-win32-printer.md)         | 設定預設印表機。<br/>                                                                                                                                                                              |
| **SetPowerState**                                                                    | 未實作。 如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ 印表機**](cim-printer.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。<br/> |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-printer.md) | 寫入控制印表機存取權之安全描述項的更新版本。<br/>                                                                                                              |



 

### <a name="properties"></a>屬性

**Win32 \_ 印表機** 類別具有這些屬性。

<dl> <dt>

**屬性**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以 Windows 為基礎的列印裝置的屬性點陣圖。

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**印表機 \_屬性已 \_ 排入佇列** (1 (0x1) ) 


</dt> <dd>

已排入佇列

列印工作已緩衝處理並排入佇列。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**印表機 \_屬性 \_ 直接** (2 (0x2) ) 


</dt> <dd>

直接

要直接傳送到印表機的檔。 如果列印工作未正確排入佇列，則會使用這個值。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**印表機 \_屬性 \_ 預設** (4 (0x4) ) 


</dt> <dd>

預設

電腦上的預設印表機。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**印表機 \_屬性 \_ 共用** (8 (0x8) ) 


</dt> <dd>

共用

可作為共用網路資源。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**印表機 \_ATTRIBUTE \_ NETWORK** (16 (0x10) ) 


</dt> <dd>

網路

附加至網路。 如果同時設定了本機和網路位，這就表示網路印表機。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**印表機 \_屬性 \_ 隱藏** (32 (0x20) ) 


</dt> <dd>

Hidden

從網路上的某些使用者隱藏。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**印表機 \_屬性 \_ LOCAL** (64 (0x40) ) 


</dt> <dd>

本機

直接連接到電腦。 如果同時設定了本機和網路位，這就表示網路印表機。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**印表機 \_屬性 \_ ENABLEDEVQ** (128 (0x80) ) 


</dt> <dd>

EnableDevQ

啟用印表機上的佇列（如果有的話）。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**印表機 \_屬性 \_ KEEPPRINTEDJOBS** (256 (0x100) ) 


</dt> <dd>

KeepPrintedJobs

列印多工緩衝處理器不應該在列印檔案之後刪除它們。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**印表機 \_屬性 \_ \_ \_ 先完成** (512 (0x200) ) 


</dt> <dd>

DoCompleteFirst

啟動先完成幕後處理的作業。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**印表機 \_屬性 \_ \_ 離線工作** (1024 (0x400) ) 


</dt> <dd>

WorkOffline

無法使用印表機時，將列印工作排在佇列中。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**印表機 \_ATTRIBUTE \_ 啟用 \_ 雙向** (2048 (0x800) ) 


</dt> <dd>

EnableBIDI

啟用雙向列印。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**印表機 \_\_ \_ 僅限 RAW 屬性** (4096 (0x1000) ) 


</dt> <dd>

只允許對原始資料類型作業進行多工緩衝處理。

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**印表機 \_屬性 \_ 發行** (8192 (0x2000) ) 


</dt> <dd>

已發行

發佈于網路目錄服務。

</dd> </dl>

</dd> <dt>

**可用性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") 
</dt> </dl>

裝置的可用性和狀態。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) 


</dt> <dd>

執行中或完整電源

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) 


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) 


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) 


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) 


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) 


</dt> <dd>

裝置已知處於省電模式，但其確切狀態不明。

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) 


</dt> <dd>

裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) 


</dt> <dd>

裝置無法正常運作，但可快速進入完整電源。

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) 


</dt> <dd>

裝置處於警告狀態，但也處於省電模式。

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) 


</dt> <dd>

裝置已暫停。

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) 


</dt> <dd>

裝置未就緒。

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) 


</dt> <dd>

裝置未設定。

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) 


</dt> <dd>

裝置為靜音。

</dd> </dl>

</dd> <dt>

**AvailableJobSheets**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. RequiredJobSheets" ) 
</dt> </dl>

印表機上所有可用工作表的陣列。 也可以用來描述印表機可能會在每個作業開始時提供的橫幅，或其他使用者指定的選項。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**AveragePagesPerMinute**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

印表機可以產生輸出的列印速率（平均每分鐘頁面數）。

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (」[**CIM \_ 印表機**](cim-printer.md)。CapabilityDescriptions "、" CIM \_ PrintJob. 完成 "、" cim \_ PrintService. 功能 ") 
</dt> </dl>

印表機功能的陣列。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) 


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) 


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) 


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) 


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) 


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) 


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) 


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) 


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) 


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) 


</dt> <dd>

Two-Sided 長邊緣

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) 


</dt> <dd>

Two-Sided 短邊緣

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) 


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) 


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) 


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) 


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) 


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) 


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (」[**CIM \_ 印表機**](cim-printer.md)。**功能**") 
</dt> </dl>

自由格式字串的陣列，提供 **功能** 陣列中指出之印表機功能的詳細說明。 這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短描述（單行字串）。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**CharSetsSupported**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**MODELCORRESPONDENCE**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. 字元集" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-prtLocalizationCharacterSet ") 
</dt> </dl>

輸出的可用字元集陣列。 在此屬性中提供的字串必須符合 RFC 2046 (MIME 第2部分) 中的第4.1.2 節 ( "字元集參數" ) 所指定的語義和語法，並且包含在 IANA 字元集登錄中。 範例包括 "UTF-8"、"us-ASCII" 和 "iso-8859-1"。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**註解**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

列印佇列的批註。

範例：彩色印表機

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 
</dt> </dl>

Win32 設定管理員錯誤碼。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**  (0)


</dt> <dd>

裝置運作正常。

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。** (1)


</dt> <dd>

裝置未正確設定。

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。** (3)


</dt> <dd>

此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。** (4)


</dt> <dd>

裝置無法正常運作。 其中一個驅動程式或登錄可能已損毀。

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。** (5)


</dt> <dd>

裝置的驅動程式需要 Windows 無法管理的資源。

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。** (6)


</dt> <dd>

裝置的開機設定與其他裝置發生衝突。

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。** (8)


</dt> <dd>

遺漏裝置的驅動程式載入器。

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。** (9)


</dt> <dd>

裝置無法正常運作。 控制的固件未正確報告裝置的資源。

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。** (10)


</dt> <dd>

裝置無法啟動。

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。** (11)


</dt> <dd>

裝置失敗。

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**  (12) 


</dt> <dd>

裝置找不到足夠的可用資源。

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。** (13)


</dt> <dd>

Windows 無法驗證裝置的資源。

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。** (14)


</dt> <dd>

裝置在重新開機電腦之前無法正常運作。

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。** (15)


</dt> <dd>

裝置因可能的重新列舉問題而無法正常運作。

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。** (16)


</dt> <dd>

Windows 無法識別裝置使用的所有資源。

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。** (17)


</dt> <dd>

裝置正在要求未知的資源類型。

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。** (18)


</dt> <dd>

必須重新安裝設備磁碟機。

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。** (20)


</dt> <dd>

登錄可能已損毀。

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。** (21)


</dt> <dd>

系統失敗。 如果變更設備磁碟機是不正確，請參閱硬體檔。 Windows 正在移除裝置。

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。** (22)


</dt> <dd>

裝置已停用。

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。** (23)


</dt> <dd>

系統失敗。 如果變更設備磁碟機是不正確，請參閱硬體檔。

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。** (24)


</dt> <dd>

裝置不存在、無法正常運作，或未安裝所有的驅動程式。

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。** (25)


</dt> <dd>

Windows 仍在設定裝置。

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。** (26)


</dt> <dd>

Windows 仍在設定裝置。

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。** (27)


</dt> <dd>

裝置沒有有效的記錄檔設定。

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。** (28)


</dt> <dd>

未安裝設備磁碟機。

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。** (29)


</dt> <dd>

裝置已停用。 裝置固件未提供所需的資源。

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。** (30)


</dt> <dd>

裝置正在使用其他裝置正在使用的 IRQ 資源。

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**  (31) 


</dt> <dd>

裝置無法正常運作。 Windows 無法載入所需的設備磁碟機。

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 
</dt> </dl>

若 **為 TRUE**，則裝置會使用使用者定義的設定。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

第一個實體類別的名稱，這個類別會出現在用來建立實例的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**CurrentCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**功能**") 
</dt> </dl>

目前正在使用的印表機功能陣列。 這個屬性中的專案也必須列在 **功能** 陣列中。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) 


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) 


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) 


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) 


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) 


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) 


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) 


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) 


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) 


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) 


</dt> <dd>

Two-Sided 長邊緣

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) 


</dt> <dd>

Two-Sided 短邊緣

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) 


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) 


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) 


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) 


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) 


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) 


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentCharSet**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**CharSetsSupported**") 
</dt> </dl>

目前用於輸出的字元集。 在此屬性中提供的字串必須符合 RFC 2046 (MIME 第2部分) 中的第4.1.2 節 ( "字元集參數" ) 所指定的語義和語法，並且包含在 IANA 字元集登錄中。 範例包括 "utf-8"、"us-ASCII" 和 iso-8859-1。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。LanguagesSupported "，"**CIM \_ Printer**.**CurrentMimeType**") 
</dt> </dl>

目前使用的印表機語言。 使用的語言必須列在 **LanguagesSupported** 屬性中。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3) 


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4) 


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5) 


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6) 


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7) 


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**Ipd** (8) 


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9) 


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10) 


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11) 


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12) 


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13) 


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14) 


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**行資料** (15) 


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16) 


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17) 


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18) 


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19) 


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20) 


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21) 


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22) 


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23) 


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24) 


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25) 


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26) 


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27) 


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28) 


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29) 


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30) 


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**簡單文字** (31) 


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32) 


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33) 


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span> (34) 的 **印象深刻**


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35) 


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36) 


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37) 


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動** (38) 


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**頁面** (39) 


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lip** (40) 


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41) 


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (42) 


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43) 


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**排除** (44) 


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Lcd** (45) 


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46) 


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47) 


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**CurrentMimeType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**CurrentLanguage**") 
</dt> </dl>

如果 **CurrentLanguage** 是 mime 類型 (值 = 47) ，目前正在使用 mime 類型。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**CurrentNaturalLanguage**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**NaturalLanguagesSupported**") 
</dt> </dl>

印表機目前用來管理的語言。 此處所列的語言也必須列在 **NaturalLanguagesSupported** 屬性中。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**CurrentPaperType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**PaperTypesAvailable**") 
</dt> </dl>

印表機正在使用的紙張類型。 必須以 ISO/IEC 10175 檔列印應用程式所指定的格式來表示 (DPA) ，在 RFC 1759 (印表機 MIB) 的附錄 C 中摘要說明。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**預設值**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，表示印表機為預設印表機。

</dd> <dt>

**DefaultCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**功能**") 
</dt> </dl>

預設使用的印表機功能陣列。 **DefaultCapabilities** 陣列中的每個專案也都必須列在 **功能** 陣列中。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) 


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) 


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) 


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) 


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) 


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) 


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) 


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) 


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) 


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) 


</dt> <dd>

Two-Sided 長邊緣

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) 


</dt> <dd>

Two-Sided 短邊緣

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) 


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) 


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) 


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) 


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) 


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) 


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultCopies**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

除非另有指定，否則為一個作業產生的複本數目。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**DefaultLanguage**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。LanguagesSupported "，"**CIM \_ Printer**.**DefaultMimeType**") 
</dt> </dl>

預設印表機語言。 此處所列的語言也必須列在 **LanguagesSupported** 屬性中。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3) 


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4) 


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5) 


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6) 


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7) 


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**Ipd** (8) 


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9) 


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10) 


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11) 


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12) 


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13) 


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14) 


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**行資料** (15) 


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16) 


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17) 


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18) 


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19) 


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20) 


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21) 


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22) 


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23) 


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24) 


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25) 


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26) 


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27) 


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28) 


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29) 


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30) 


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**簡單文字** (31) 


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32) 


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33) 


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span> (34) 的 **印象深刻**


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35) 


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36) 


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37) 


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動** (38) 


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**頁面** (39) 


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lip** (40) 


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41) 


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (42) 


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43) 


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**排除** (44) 


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Lcd** (45) 


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46) 


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47) 


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**DefaultMimeType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**DefaultLanguage**") 
</dt> </dl>

目前使用的 MIME 類型，如果 **DefaultLanguage** 值是 mime 類型 (值 = 47) 。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**DefaultNumberUp**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

印表機在一個媒體紙上轉譯的列印資料流程頁面數目，除非作業另有指定。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**DefaultPaperType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**PaperTypesAvailable**") 
</dt> </dl>

印表機使用的紙張類型，除非列印工作指定不同的紙張類型。 字串必須以 ISO/IEC 1017 檔列印應用程式所指定的格式表示 (DPA) ，在 [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (印表機 MIB) 的附錄 C 中摘要說明。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**DefaultPriority**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指派給每個列印工作的預設優先權值。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DetectedErrorState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**ErrorInformation**") ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB。IETF \| 印表機-hrPrinterDetectedErrorState ") 
</dt> </dl>

印表機錯誤資訊。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

**沒有錯誤** (2) 


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

**低紙** (3) 


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

**沒有紙張** (4) 


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

**低碳粉** (5) 


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

**沒有碳粉** (6) 


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

**門開啟** (7) 


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

**卡** (8) 


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**離線** (9) 


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

**要求的服務** (10) 


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

**輸出 Bin Full** (11) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

系統上印表機的唯一識別碼。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**直接**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，列印工作會直接傳送至印表機。 如果 **為 FALSE**，則表示列印工作已進行多工緩衝處理。

</dd> <dt>

**DoCompleteFirst**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則印表機會啟動已完成幕後處理的工作。 如果 **為 FALSE**，則印表機會依接收工作的順序啟動作業。

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

Windows 印表機驅動程式的名稱。

範例： Windows 傳真驅動程式

</dd> <dt>

**EnableBIDI**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，印表機可以列印雙向。

</dd> <dt>

**EnableDevQueryPrint**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，當檔和印表機的設置不相符時，印表機會將檔保留在佇列中。

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會清除 **LastErrorCode** 中回報的錯誤。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**LastErrorCode** 中所記錄之錯誤的相關資訊，以及可採取之矯正措施的相關資訊。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**ErrorInformation**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**DetectedErrorState**") 
</dt> </dl>

**DetectedErrorState** 中指出之目前錯誤狀態的補充資訊陣列。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**ExtendedDetectedErrorState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

報告標準錯誤資訊。 您應該在 **DetectedErrorState** 中記錄其他資訊。

值為：

<dt>

0 (0x0) 
</dt> <dd>

Unknown

</dd> <dt>

1 (0x1) 
</dt> <dd>

其他

</dd> <dt>

2 (0x2) 
</dt> <dd>

沒有錯誤

</dd> <dt>

3 (0x3) 
</dt> <dd>

紙張不足

</dd> <dt>

4 (0x4) 
</dt> <dd>

沒有紙張

</dd> <dt>

5 (0x5) 
</dt> <dd>

碳粉不足

</dd> <dt>

6 (0x6) 
</dt> <dd>

碳粉用完

</dd> <dt>

7 (0x7) 
</dt> <dd>

機門開啟

</dd> <dt>

8 (0x8) 
</dt> <dd>

夾紙

</dd> <dt>

9 (0x9) 
</dt> <dd>

要求的服務

</dd> <dt>

10 (0xA) 
</dt> <dd>

輸出紙匣已滿

</dd> <dt>

11 (0xB) 
</dt> <dd>

紙張問題

</dd> <dt>

12 (0xC) 
</dt> <dd>

無法列印頁面

</dd> <dt>

13 (0xD) 
</dt> <dd>

需要使用者介入

</dd> <dt>

14 (0xE) 
</dt> <dd>

記憶體不足

</dd> <dt>

15 (0xF) 
</dt> <dd>

伺服器不明

</dd> </dl>

</dd> <dt>

**ExtendedPrinterStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與 **Availability** 屬性中指定之資訊不同的印表機狀態資訊。

<dt>

1 (0x1) 
</dt> <dd>

其他

</dd> <dt>

2 (0x2) 
</dt> <dd>

Unknown

</dd> <dt>

3 (0x3) 
</dt> <dd>

閒置

</dd> <dt>

4 (0x4) 
</dt> <dd>

列印

</dd> <dt>

5 (0x5) 
</dt> <dd>

正在準備

</dd> <dt>

6 (0x6) 
</dt> <dd>

停止列印

</dd> <dt>

7
</dt> <dd>

離線

</dd> <dt>

8 (0x8) 
</dt> <dd>

已暫停

</dd> <dt>

9 (0x9) 
</dt> <dd>

錯誤

</dd> <dt>

10 (0xA) 
</dt> <dd>

忙碌

</dd> <dt>

11 (0xB) 
</dt> <dd>

無法使用

</dd> <dt>

12 (0xC) 
</dt> <dd>

等候中

</dd> <dt>

13 (0xD) 
</dt> <dd>

Processing

</dd> <dt>

14 (0xE) 
</dt> <dd>

初始化

</dd> <dt>

15
</dt> <dd>

省電

</dd> <dt>

16 (0x10) 
</dt> <dd>

暫止刪除

</dd> <dt>

17 (0x11) 
</dt> <dd>

I/o 主動

</dd> <dt>

18 (0x12) 
</dt> <dd>

手動送紙

</dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則會隱藏網路使用者的印表機。

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. HorizontalResolution" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "圖元/英寸" ) 
</dt> </dl>

印表機的水準解析度，以每英吋像素為單位。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

物件的安裝日期和時間。 可能會在沒有將值寫入這個屬性的情況下安裝物件。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**JobCountSinceLastReset**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **計數器**
</dt> </dl>

自上次重設印表機後的列印工作數目。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**KeepPrintedJobs**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，列印多工緩衝處理器就不會刪除已完成的作業。

</dd> <dt>

**LanguagesSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| printer-prtInterpreterLangFamily ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ printer**](cim-printer.md)。MimeTypesSupported "、" CIM \_ PrintJob Language "、" cim \_ PrintService. LanguagesSupported ") 
</dt> </dl>

原生支援的列印語言陣列。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3) 


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4) 


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5) 


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6) 


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7) 


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**Ipd** (8) 


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9) 


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10) 


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11) 


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12) 


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13) 


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14) 


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**行資料** (15) 


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16) 


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**REGIS** (17) 


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18) 


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19) 


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20) 


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21) 


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22) 


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23) 


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24) 


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25) 


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26) 


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27) 


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28) 


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29) 


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30) 


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**簡單文字** (31) 


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32) 


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**DOC** (33) 


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span> (34) 的 **印象深刻**


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35) 


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36) 


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37) 


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動** (38) 


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**頁面** (39) 


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lip** (40) 


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41) 


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (42) 


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43) 


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**排除** (44) 


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Lcd** (45) 


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**XES** (46) 


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47) 


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span id="XPS"></span><span id="xps"></span>**XPS** (48) 


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49) 


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50) 


</dt> <dd></dd> </dl>

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置報告的最後一個錯誤碼。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**本機**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，表示印表機未連接到網路。 如果 [ **本機** ] 和 [ **網路** ] 屬性都設定為 [ **TRUE**]，則印表機為網路印表機。

</dd> <dt>

**位置**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

印表機的實體位置。

範例： Bldg。 38，房間1164

</dd> <dt>

**MarkingTechnology**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-prtMarkerMarkTech ") 
</dt> </dl>

標示印表機所使用的技術。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

**ELECTROPHOTOGRAPHIC LED** (3) 


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

**Electrophotographic 鐳射** (4) 


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

**Electrophotographic 其他** (5) 


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

**移動頭部點矩陣 9pin** (6) 的影響


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

**移動頭部點矩陣 24pin** (7) 的影響


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

將 **頭部點矩陣移至其他** (8) 的影響


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

移動前端 (9) 的 **完整格式影響**


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

**影響波段** (10) 


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

**影響其他** (11) 


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

**噴墨 Aqueous** (12) 


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

**噴墨** (13) 


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

**其他** (14) 的噴墨


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

**畫筆** (15) 


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

 (16) 的 **熱傳輸**


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

 (17) 的 **熱機密**


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

 (18) 的 **熱擴散**


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

**其他熱** (19) 


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

**Electroerosion** (20) 


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

**靜電** (21) 


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

**攝影縮微膠片** (22) 


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

**攝影照排機** (23) 


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

**攝影其他** (24) 


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

**離子 Deposition** (25) 


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

**eBeam** (26) 


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

**Typesetter** (27) 


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxCopies**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「CIM \_ PrintJob」 ) 
</dt> </dl>

印表機可以為一個工作產生的最大複本數目。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**MaxNumberUp**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. NumberUp" ) 
</dt> </dl>

印表機可以在一張媒體紙上轉譯的列印資料流程頁面數目上限，例如紙張。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**MaxSizeSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. JobSize" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

最大的作業（以 kb 為單位），可供印表機接受。 值為 0 (零) 表示未設定任何限制。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**MimeTypesSupported**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。LanguagesSupported "、" CIM \_ PrintJob. mimetype "、" cim \_ PrintService. MimeTypesSupported ") 
</dt> </dl>

印表機支援的詳細 MIME 類型說明的陣列。 如果提供了資料，則值 47 ( "MIME" ) 必須包含在 **LanguagesSupported** 屬性中。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) 
</dt> </dl>

印表機的名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**NaturalLanguagesSupported**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| Printer-prtLocalizationLanguage ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ") 
</dt> </dl>

印表機用來輸出管理資訊的字串所支援的語言陣列。 必須符合 [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt)。 例如，"en" 用於英文。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**Network**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，表示印表機為網路印表機。 如果 [ **本機** ] 和 [ **網路** ] 屬性都設定為 [ **TRUE**]，則印表機為網路印表機。

</dd> <dt>

**PaperSizesSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

印表機支援的紙張類型陣列。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span id="A"></span><span id="a"></span>**(2**) 


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (3) 


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span id="C"></span><span id="c"></span>**C** (4) 


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span id="D"></span><span id="d"></span>**D** (5) 


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (6) 


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**字母** (7) 


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**合法** (8) 


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-信封** (9) 


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-信封** (10) 


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-數位-10-信封** (11) 


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-信封** (12) 


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-信封** (13) 


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-信封** (14) 


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-數位-9-信封** (15) 


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-信封** (16) 


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-信封** (17) 


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span id="A0"></span><span id="a0"></span>**A0** (18) 


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span id="A1"></span><span id="a1"></span>**A1** (19) 


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span id="A2"></span><span id="a2"></span>**A2** (20) 


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span id="A3"></span><span id="a3"></span>**A3** (21) 


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span id="A4"></span><span id="a4"></span>**A4** (22) 


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span id="A5"></span><span id="a5"></span>**A5** (23) 


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span id="A6"></span><span id="a6"></span>**A6** (24) 


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span id="A7"></span><span id="a7"></span>**A7** (25) 


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span id="A8"></span><span id="a8"></span>**A8** (26) 


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27) 


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span id="B0"></span><span id="b0"></span>**B0** (28) 


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span id="B1"></span><span id="b1"></span>**B1** (29) 


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span id="B2"></span><span id="b2"></span>**B2** (30) 


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span id="B3"></span><span id="b3"></span>**B3** (31) 


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span id="B4"></span><span id="b4"></span>**B4** (32) 


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span id="B5"></span><span id="b5"></span>**B5** (33) 


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span id="B6"></span><span id="b6"></span>**B6** (34) 


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span id="B7"></span><span id="b7"></span>**B7** (35) 


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span id="B8"></span><span id="b8"></span>**B8** (36) 


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span id="B9"></span><span id="b9"></span>**B9** (37) 


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span id="B10"></span><span id="b10"></span>**B10** (38) 


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span id="C0"></span><span id="c0"></span>**C0** (39) 


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span id="C1"></span><span id="c1"></span>**C1** (40) 


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41) 


</dt> <dd>

C2

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span id="C4"></span><span id="c4"></span>**C4** (42) 


</dt> <dd>

C3

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span id="C5"></span><span id="c5"></span>**C5** (43) 


</dt> <dd>

C4

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span id="C6"></span><span id="c6"></span>**C6** (44) 


</dt> <dd>

C5

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span id="C7"></span><span id="c7"></span>**C7** (45) 


</dt> <dd>

C6

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span id="C8"></span><span id="c8"></span>**C8** (46) 


</dt> <dd>

C7

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-指定** (47) 


</dt> <dd>

C8

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48) 


</dt> <dd>

ISO-Designated

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49) 


</dt> <dd>

JIS B0

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50) 


</dt> <dd>

JIS B1

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51) 


</dt> <dd>

JIS B2

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52) 


</dt> <dd>

JIS B3

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53) 


</dt> <dd>

JIS B4

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54) 


</dt> <dd>

JIS B5

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55) 


</dt> <dd>

JIS B6

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56) 


</dt> <dd>

JIS B7

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57) 


</dt> <dd>

JIS B8

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58) 


</dt> <dd>

JIS B9

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-字母** (59) 


</dt> <dd>

JIS B10

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-合法** (60) 


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-信封** (61) 


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-信封** (62) 


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-信封** (63) 


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-信封** (64) 


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-信封** (65) 


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-信封** (66) 


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**指定-長信封** (67) 


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-信封** (68) 


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69) 


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span> (70) 的 **對開**


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**發票** (71) 


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**總帳** (72) 


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73) 


</dt> <dd></dd> </dl>

</dd> <dt>

**PaperTypesAvailable**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**MODELCORRESPONDENCE**](../wmisdk/standard-qualifiers.md) ( "cim \_ PrintJob. RequiredPaperType"，"cim \_ PrintService. PaperTypesAvailable" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-prtInputMediaName ") 
</dt> </dl>

印表機目前提供的紙張類型陣列。 每個字串都必須以 ISO/IEC 10175 檔列印應用程式所指定的格式表示 (DPA) ，在 [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (印表機 MIB) 的附錄 C 中摘要說明。 這個屬性中所識別的任何紙張大小也必須出現在 **PaperSizesSupported** 屬性中。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

範例： iso-a4-彩色

</dd> <dt>

**參數**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

列印處理器的選擇性參數。

範例： "副本 = 2"

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 
</dt> </dl>

Windows隨插即用邏輯裝置的裝置識別碼。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

範例： \* PNP030b

</dd> <dt>

**PortName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來將資料傳輸至印表機的埠。 如果印表機連線到一個以上的埠，每個埠的名稱會以逗號分隔。

範例： LPT1：、LPT2：、LPT3：

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置的特定電源相關功能陣列。

這個屬性繼承自 **CIM \_ LogicalDevice**。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) 


</dt> <dd>

電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) 


</dt> <dd>

裝置可以根據使用方式或其他準則來變更其電源狀態。

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) 


</dt> <dd>

支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。 這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**


</dt> <dd>

您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**


</dt> <dd>

支援計時 Power-On

您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則可以管理裝置的電源，這表示它可以放入暫停模式。 屬性不會指出電源管理功能是否已啟用，只有邏輯裝置能夠進行電源管理。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**PrinterPaperNames**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

印表機支援的紙張大小陣列。 印表機指定的名稱是用來表示支援的紙張大小。

範例： B5 (JIS) 

</dd> <dt>

**PrinterState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

與此印表機相關的可能狀態之一。 這個屬性已經過時。 若要取代這個屬性，請使用 **PrinterStatus**。

<dt>

0
</dt> <dd>

閒置-如需詳細資訊，請參閱下面的「備註」一節。

</dd> <dt>

1
</dt> <dd>

已暫停

</dd> <dt>

2
</dt> <dd>

錯誤

</dd> <dt>

3
</dt> <dd>

暫止刪除

</dd> <dt>

4
</dt> <dd>

紙紙

</dd> <dt>

5
</dt> <dd>

論文

</dd> <dt>

6
</dt> <dd>

手動送紙

</dd> <dt>

7
</dt> <dd>

紙張問題

</dd> <dt>

8
</dt> <dd>

離線

</dd> <dt>

9
</dt> <dd>

I/o 主動

</dd> <dt>

10
</dt> <dd>

忙碌

</dd> <dt>

11
</dt> <dd>

列印

</dd> <dt>

12
</dt> <dd>

輸出紙匣已滿

</dd> <dt>

13
</dt> <dd>

無法使用

</dd> <dt>

14
</dt> <dd>

等候中

</dd> <dt>

15
</dt> <dd>

Processing

</dd> <dt>

16
</dt> <dd>

初始化

</dd> <dt>

17
</dt> <dd>

正在準備

</dd> <dt>

18
</dt> <dd>

碳粉不足

</dd> <dt>

19
</dt> <dd>

碳粉用完

</dd> <dt>

20
</dt> <dd>

頁面

</dd> <dt>

21
</dt> <dd>

需要使用者介入

</dd> <dt>

22
</dt> <dd>

記憶體不足

</dd> <dt>

23
</dt> <dd>

機門開啟

</dd> <dt>

24
</dt> <dd>

伺服器 \_ 不明

</dd> <dt>

25
</dt> <dd>

省電

</dd> </dl>

</dd> <dt>

**PrinterStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-hrPrinterStatus ") 
</dt> </dl>

印表機的狀態資訊，與 [邏輯裝置 **可用性** ] 屬性中指定的資訊不同。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**閒置** (3) 


</dt> <dd>

閒置-如需詳細資訊，請參閱下面的「備註」一節。

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**列印** (4) 


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**預熱** (5) 


</dt> <dd>

正在準備

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**已停止列印** (6) 


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (7) 


</dt> <dd></dd> </dl>

</dd> <dt>

**PrintJobDataType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

等候以 Windows 為基礎的列印裝置之列印工作的資料類型。

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

處理列印工作的列印多工緩衝處理器名稱。

範例： SPOOLSS.DLL

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

印表機的優先順序。 較高優先順序的印表機上的工作會先排程。

</dd> <dt>

**已發行**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則會在網路目錄服務中發佈印表機。

</dd> <dt>

**已排入佇列**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則印表機會緩衝並將列印工作排在佇列中。

</dd> <dt>

**RawOnly**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，則印表機只接受要進行多工緩衝處理的原始資料。

</dd> <dt>

**SeparatorFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來建立分隔符號頁面的檔案名。 此頁面是用來分隔傳送至印表機的列印工作。

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制印表機的伺服器名稱。 如果這個字串是 **Null**，則會在本機控制印表機。

</dd> <dt>

[共用]
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若為 **TRUE**，則會將印表機作為共用網路資源提供。

</dd> <dt>

**共用**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

以 Windows 為基礎的列印裝置的共用名稱。

範例： " \\ \\ PRINTSERVER1 \\ PRINTER2"

</dd> <dt>

**SpoolEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

這個屬性已過時;請勿使用。 若為 **TRUE**，則會啟用印表機的多工緩衝處理。

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

印表機可以開始列印工作的日期和時間—如果印表機受限於在特定時間列印。 此值會表示自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括： **[確定]、[****降級**] 和 [ **Pred** ] (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括： **錯誤**、 **啟動**、 **停止** 及 **服務**。 後者可能會在磁片的鏡像重新同步處理期間 **套用，而** 重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素並不是 **正常** 的，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") 
</dt> </dl>

邏輯裝置的狀態。 如果此屬性不適用於邏輯裝置，則應該使用值 5 (**不適用**) 。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (3) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**已停用** (4) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

範圍電腦之 **CreationClassName** 屬性的值。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

範圍系統的名稱。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次重設印表機的日期和時間。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

印表機可以列印最後一個工作的日期和時間—如果印表機受限於在特定時間列印。 此值會表示自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. HorizontalResolution" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "圖元/英寸" ) 
</dt> </dl>

印表機的垂直解析度（以圖元為單位）。

這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。

</dd> <dt>

**WorkOffline**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 TRUE**，您可以在印表機離線時，將電腦上的列印工作排入佇列。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 印表機** 類別衍生自 [**CIM \_ 印表機**](cim-printer.md)。 針對 **Win32 \_ 印表機** 實例呼叫 [**SWbemObject \_ . Put**](../wmisdk/swbemobject-put-.md)或 [**IWbemServices：:P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance)之前，必須啟用 Visual Basic 和) LoadDriver 的 **SeLoadDriverPrivilege** 許可權 (**wbemPrivilegeLoadDriver** 。 如需詳細資訊，請參閱 [**許可權常數**](../wmisdk/privilege-constants.md) 和 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。 下列 VBScript 程式碼範例顯示如何在腳本中啟用 **SetLoadDriverPrivilege** 許可權。

如需使用 MSCS 印表機叢集，請使用 prnadmin.dll 元件，或 .NET Framework 的[System. 列印](/dotnet/api/system.printing)命名空間。


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



Windows 使用執行腳本之使用者的認證來判斷可用的印表機是什麼。 因此，如果您是從遠端執行腳本，您只能存取該遠端系統上您的使用者帳戶所能使用的任何印表機。

您無法針對 MSCS 列印叢集上的印表機使用 **Win32 \_ 印表機** 類別。 相反地，您可能需要使用 PrinterAdmin 工具 (PrnAdmin.dll) 或 .NET Framework [System. 列印](/dotnet/api/system.printing)命名空間。

> [!Note]  
> 如果您要抓取 **PrinterStatus** = 3 或 **PrinterState** = 0，印表機驅動程式可能無法將正確的資訊饋送至 WMI。 WMI 會從 spoolsv.exe 進程抓取印表機資訊。 印表機驅動程式可能不會將其狀態報表給多工緩衝處理器。 在此情況下， **Win32 \_ 印表機** 會將印表機報告為 **閒置**。

 

## <a name="examples"></a>範例

PS 使用 TechNet 資源庫上的 Visio PowerShell 範例來 [建立電腦設定繪圖](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557)使用 **Win32 \_ 印表機** 與 Visio automation 模型互動，以建立 Visio 繪圖。

[Powershell 遠端電腦資訊腳本](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436)會使用許多類別（包括 **Win32 \_ 印表機**）來取得遠端電腦的相關資訊。

下列 PowerShell 程式碼範例顯示如何判斷本機電腦的預設印表機。


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



下列 VBScript 程式碼範例說明如何從 **Win32 \_ 印表機** 的實例取出印表機統計資料。


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



下列 Perl 程式碼範例說明如何從 **Win32 \_ 印表機** 的實例取出印表機統計資料。


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



下列 VBScript 程式碼範例顯示如何取得電腦預設印表機的名稱。


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 印表機**](cim-printer.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> <dt>

[WMI 工作：印表機和列印](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 

---
Description: Win32 \_ 進程&\# 32;WMI 類別代表作業系統上的進程。
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Win32_Process 類別
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999205"
---
# <a name="win32_process-class"></a>Win32 \_ 進程類別

**Win32 \_ 進程** [WMI 類別](../wmisdk/retrieving-a-class.md)代表作業系統上的進程。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

> [!NOTE]
> 如需 Windows 內進程和執行緒的一般討論，請參閱「程式 [和執行緒](/ProcThread/processes-and-threads.md)」主題。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a>成員

**Win32 \_ 進程** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ 進程** 類別具有這些方法。



| 方法                                                                   | 描述                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachDebugger**](attachdebugger-method-in-class-win32-process.md)   | 啟動處理常式目前註冊的偵錯工具。<br/>                                                                                                                                                                                                                      |
| [**建立**](create-method-in-class-win32-process.md)                   | 建立新的進程。<br/>                                                                                                                                                                                                                                                         |
| [**GetAvailableVirtualSize**](getavailablevirtualsize-win32-process.md) | 抓取進程可用之可用虛擬位址空間的目前大小（以位元組為單位）。<br/> **Windows server 2012、Windows 8、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | 抓取進程執行時所使用的使用者名稱和功能變數名稱。<br/>                                                                                                                                                                                                    |
| [**GetOwnerSid**](getownersid-method-in-class-win32-process.md)         | 抓取進程擁有者 (SID) 的安全識別碼。<br/>                                                                                                                                                                                                            |
| [**SetPriority**](setpriority-method-in-class-win32-process.md)         | 變更進程的執行優先權。<br/>                                                                                                                                                                                                                                   |
| [**終止**](terminate-method-in-class-win32-process.md)             | 終止進程及其所有線程。<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>屬性

**Win32 \_ 進程** 類別具有這些屬性。

<dl> <dt>

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

**CommandLine**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "命令列以啟動進程" ) 
</dt> </dl>

用來啟動特定進程的命令列（如果適用）。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "CreationDate" ) 
</dt> </dl>

進程開始執行的日期。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CSCreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 電腦系統類別名稱 ") 
</dt> </dl>

範圍電腦系統的建立類別名稱。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CSName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Computer System Name ") 
</dt> </dl>

範圍電腦系統的名稱。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

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

**ExecutablePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：[**許可權**](../wmisdk/standard-wmi-qualifiers.md) ( "SeDebugPrivilege" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Tool 說明結構 \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| SzExePath" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可執行檔路徑" ) 
</dt> </dl>

進程可執行檔的路徑。

範例： "C： \\ Windows \\ System \\Explorer.Exe"

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「執行狀態」 ) 
</dt> </dl>

進程目前的操作狀況。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

Unknown

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

其他

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**就緒** (2) 


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) 


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**封鎖** (4) 


</dt> <dd>

封鎖

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**擱置** 的已封鎖 (5) 


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>已 **暫止就緒** (6) 


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**終止** (7) 


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (8) 


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span> (9) **成長**


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Handle" ) 
</dt> </dl>

處理序識別碼。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程狀態 \| 系統 \_ 進程 \_ 資訊 \| HandleCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「控制碼計數」 ) 
</dt> </dl>

進程所擁有的開啟控制碼總數。 **HandleCount** 是此進程中，每個執行緒目前開啟之控制碼的總和。 控制碼可用來檢查或修改系統資源。 每個控制碼在內部維護的資料表中都有一個專案。 專案包含用來識別資源類型的資源和資料位址。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

物件的安裝日期。 可能會在沒有將值寫入這個屬性的情況下安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "KernelModeTime" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) 
</dt> </dl>

核心模式中的時間（以毫秒為單位）。 如果無法使用這項資訊，請使用 0 (零) 的值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**MaximumWorkingSetSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**許可權**](../wmisdk/standard-wmi-qualifiers.md) ( "SeDebugPrivilege" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32 \| WINNT。H \| 配額 \_ 限制 \| MaximumWorkingSetSize ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 工作集大小上限 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") 
</dt> </dl>

進程的工作集大小上限。 處理常式的工作集是實體 RAM 中處理常式可見的記憶體頁面集。 這些頁面是常駐的，可供應用程式使用，而不會觸發分頁錯誤。

範例：1413120

</dd> <dt>

**MinimumWorkingSetSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**許可權**](../wmisdk/standard-wmi-qualifiers.md) ( "SeDebugPrivilege" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32 \| WINNT。H \| 配額 \_ 限制 \| MinimumWorkingSetSize ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 工作集大小下限 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") 
</dt> </dl>

進程的工作集大小下限。 處理常式的工作集是實體 RAM 中處理常式可見的記憶體頁面集。 這些頁面是常駐的，可供應用程式使用，而不會觸發分頁錯誤。

範例：20480

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) 
</dt> </dl>

負責處理常式的可執行檔名稱，相當於工作管理員中的 [映射名稱] 屬性。

當子類別繼承時，可以將屬性覆寫為索引鍵屬性。 名稱會硬式編碼為應用程式本身，而不會受到變更的檔案名影響。 例如，即使您將 Calc.exe 重新命名，Calc.exe 的名稱仍會出現在工作管理員以及任何可取出進程名稱的 WMI 腳本中。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 作業系統類別名稱 ") 
</dt> </dl>

範圍作業系統的建立類別名稱。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**Name**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 作業系統 Name ") 
</dt> </dl>

範圍作業系統的名稱。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**OtherOperationCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| OtherOperationCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「其他作業計數」 ) 
</dt> </dl>

未讀取或寫入作業所執行的 i/o 作業數目。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**OtherTransferCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| OtherTransferCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「其他傳輸計數」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) 
</dt> </dl>

作業期間在非讀取或寫入作業期間傳輸的資料量。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**PageFaults**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PageFaultCount" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「分頁錯誤數」 ) 
</dt> </dl>

進程產生的分頁錯誤數目。

範例：10

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程狀態 \| 系統 \_ 進程 \_ 資訊 \| PagefileUsage」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「分頁檔案使用方式」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) 
</dt> </dl>

進程目前正在使用的分頁檔案空間量。 此值與 TaskMgr.exe 中的 **VMSize** 值一致。

範例：102435

</dd> <dt>

**ParentProcessId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| InheritedFromUniqueProcessId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "上層處理序識別碼" ) 
</dt> </dl>

建立進程之進程的唯一識別碼。 系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。 **ParentProcessId** 所識別的進程可能會終止，因此 **ParentProcessId** 可能不會參考執行中的進程。 **ParentProcessId** 也可能不正確地參考重複使用處理序識別碼的進程。 您可以使用 **CreationDate** 屬性來判斷指定的父系是否在建立此 **Win32 \_ 進程** 實例所表示的進程之後建立。

</dd> <dt>

**PeakPageFileUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PeakPagefileUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰分頁檔案使用方式」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) 
</dt> </dl>

進程存留期間使用的分頁檔空間數量上限。

範例：102367

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PeakVirtualSize" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "尖峰虛擬位址空間使用量" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

進程一次使用的虛擬位址空間上限。 使用虛擬位址空間不一定表示對應使用的是磁片或主儲存體頁面。 不過，虛擬空間是有限的，而且使用太多進程可能無法載入程式庫。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PeakWorkingSetSize" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰工作集大小」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) 
</dt> </dl>

進程的尖峰工作集大小。

範例：1413120

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "priority" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| 根據 basepriority" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Priority" ) 
</dt> </dl>

排程作業系統內進程的優先順序。 值愈高，進程所收到的優先順序愈高。 優先權值的範圍可以從 0 (零) ，也就是最高優先順序的最低優先順序為31。

範例：7

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PrivatePageCount" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Private Page Count" ) 
</dt> </dl>

目前配置的頁面數目只能供這個 **Win32 \_ 進程** 實例所代表的進程存取。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**進程**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| [**處理 \_ 資訊**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「處理序識別碼」 ) 
</dt> </dl>

用來區別某個進程與另一個進程的數值識別碼。 ProcessIDs 從處理常式建立到處理終止都有效。 終止時，可以將相同的數值識別碼套用至新的進程。

這表示您無法單獨使用 ProcessID 來監視特定的進程。 例如，應用程式的 ProcessID 可能是7，然後失敗。 當新的進程啟動時，可能會將新的進程指派給 ProcessID 7。 只針對指定的 ProcessID 檢查的腳本，因此可以「愚弄」，以為原始應用程式仍在執行中。

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaNonPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「非分頁集區使用量配額」 ) 
</dt> </dl>

進程的非分頁集區使用量配額量。

範例：15

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "分頁集區使用量配額" ) 
</dt> </dl>

進程的分頁集區使用量配額量。

範例：22

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaPeakNonPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰非分頁集區使用量配額」 ) 
</dt> </dl>

進程的非分頁集區使用量的尖峰配額量。

範例：31

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaPeakPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰分頁集區使用量配額」 ) 
</dt> </dl>

進程之分頁集區使用量的尖峰配額量。

範例：31

</dd> <dt>

**ReadOperationCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| ReadOperationCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「讀取作業計數」 ) 
</dt> </dl>

執行的讀取作業數。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**ReadTransferCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| ReadTransferCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「讀取傳輸計數」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) 
</dt> </dl>

讀取的資料量。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| SessionId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Session Id" ) 
</dt> </dl>

當建立會話時，作業系統所產生的唯一識別碼。 會話會在一段時間內進行登入，直到從特定系統登出為止。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

這個屬性不會執行，也不會填入這個類別的任何實例。 一律為 **Null**。

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

**TerminationDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "終止日期" ) 
</dt> </dl>

進程已停止或終止。 若要取得終止時間，處理常式的控制碼必須保持開啟狀態。 否則，此屬性會傳回 **Null**。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**ThreadCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| NumberOfThreads" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Thread Count" ) 
</dt> </dl>

進程中的作用中線程數目。 指令是處理器中的基本執行單位，而執行緒是執行指令的物件。 每個執行中的進程至少都有一個執行緒。

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "UserModeTime" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) 
</dt> </dl>

使用者模式中的時間，以100的毫微秒數單位表示。 如果無法使用這項資訊，請使用 0 (零) 的值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| VirtualSize" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「虛擬位址空間使用量」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「bytes」 ) 
</dt> </dl>

進程正在使用的虛擬位址空間目前的大小，而不是處理常式實際使用的實體或虛擬記憶體。 使用虛擬位址空間不一定表示對應使用的是磁片或主儲存體頁面。 虛擬空間有限，且使用太多，進程可能無法載入程式庫。 此值與您在 Perfmon.exe 中看到的值一致。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒函式 \| GetProcessVersion" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Windows Version" ) 
</dt> </dl>

進程執行所在的 Windows 版本。

範例：4。0

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "工作集大小" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

進程需要有效率地執行的記憶體數量（以位元組為單位），適用于使用以頁面為基礎的記憶體管理的作業系統。 如果系統沒有足夠的記憶體 (小於) 的工作集大小，就會發生錯誤。 如果工作集的大小不是已知的，請使用 **Null** 或 0 (零) 。 如果提供了工作集資料，您可以監視資訊，以瞭解進程的變更記憶體需求。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。

</dd> <dt>

**WriteOperationCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| WriteOperationCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「寫入作業計數」 ) 
</dt> </dl>

執行的寫入作業數目。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**WriteTransferCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| WriteTransferCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「寫入傳輸計數」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) 
</dt> </dl>

寫入的資料量。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 進程** 類別衍生自 [**CIM \_ 進程**](cim-process.md)。 使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。 如需詳細資訊，請參閱 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。

### <a name="overview"></a>概觀

進程幾乎是在電腦上執行的所有作業。 事實上，大部分電腦問題的根本原因可以追蹤至進程;例如，電腦上可能正在執行太多進程 (並且爭用一組有限的資源) ，或單一進程可能使用的資源超過其共用。 這些因素對於在電腦上執行的進程保持密切監看是很重要的。 進程監視是程式管理中的主要活動，可讓您判斷電腦的實際功能、電腦執行的應用程式，以及這些應用程式在運算環境中的變更如何受到影響。

### <a name="monitoring-a-process"></a>監視進程

定期監視程式可協助您確保電腦以尖峰效率執行，而且會如預期般執行其已分配的工作。 例如，藉由監視程式，您可以立即通知任何已停止回應的應用程式，然後採取步驟來結束該進程。 此外，進程監視還可讓您在問題發生之前加以識別。 例如，藉由重複檢查進程所使用的記憶體數量，您可以找出記憶體流失。 然後，您可以在不當應用程式使用所有可用的記憶體之前停止進程，並讓電腦停止運作。

程式監視也有助於將計畫中斷進行升級和維護所造成的中斷情況降到最低。 例如，藉由檢查用戶端電腦上執行之資料庫應用程式的狀態，您可以判斷讓資料庫離線以升級軟體的影響。

監視進程的可用性。 測量進程可用的時間百分比。 可用性通常是使用簡單探查來監視，它會報告進程是否仍在執行中。 藉由追蹤每個探查的結果，您可以計算進程的可用性。 例如，在這種情況下，會探查100次並回應95的進程，其可用性為95%。 這種類型的監視通常會保留給資料庫、郵件程式，以及預期會在任何時間執行的其他應用程式。 這不適用於每日定期啟動和停止的文字處理程式、試算表或其他應用程式。

您可以建立 [**Win32 \_ ProcessStartup**](win32-processstartup.md) 類別的實例來設定處理常式。

您可以使用 [**Win32 \_ PerfFormattedData \_ perfproc.dll \_ process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) 類別和 WMI 重新整理程式物件（例如 [**SWbemRefresher**](../wmisdk/swbemrefresher.md)）來監視流程效能。 如需詳細資訊，請參閱 [監視效能資料](../wmisdk/monitoring-performance-data.md)。

## <a name="examples"></a>範例

TechNet 元件庫上 [WMI 類別](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell 程式碼範例的內容清單說明 **Win32 \_ Process** 類別，並以 Excel 格式輸出結果。

在 [多部伺服器上終止](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) 執行的進程會終止在單一或多部電腦上執行的處理常式。

在 [範例中：呼叫提供者方法](../wmisdk/example--calling-a-provider-method.md) 主題時，程式碼會使用 c + + 呼叫 **Win32 \_ 進程** 來建立進程。

可用性是最簡單的程式監視形式：使用此方法時，您只需確定進程正在執行中。 當您監視程式可用性時，通常會取出電腦上執行的處理常式清單，然後確認特定進程是否仍在作用中。 如果進程在使用中，則會被視為可用。 如果進程不在使用中，則無法使用。 下列 VBScript 範例會藉由檢查電腦上執行的處理常式清單，並在找不到 Database.exe 進程時發出通知，來監視進程的可用性。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



下列 VBScript 範例會使用暫存事件取用者來監視進程建立。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



下列 VBScript 會監視進程效能資訊。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



下列 VBScript 程式碼範例顯示如何取得本機電腦上每個處理常式的擁有者。 您可以使用此腳本從遠端電腦取得資料，例如，若要判斷哪些使用者有執行終端機伺服器的處理常式，請在第一行以 "." 取代遠端電腦的名稱。 您也必須是遠端電腦上的系統管理員。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



下列 VBScript 程式碼範例示範如何取得與執行中進程相關聯的登入會話。 處理常式必須在腳本啟動之前 Notepad.exe 執行。 此範例會尋找與代表 Notepad.exe 的 **win32 \_ 進程** 相關聯的 [**win32 \_ LogonSession**](win32-logonsession.md)實例。 [**Win32 \_SessionProcess**](win32-sessionprocess.md) 會指定為 association 類別。 如需詳細資訊，請參閱 [語句的 associators of](../wmisdk/associators-of-statement.md)。


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



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

[**CIM \_ 進程**](cim-process.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> <dt>

[WMI 工作：進程](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 

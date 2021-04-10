---
description: 代表安裝在電腦上的 Windows 作業系統。
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191014"
---
# <a name="win32_operatingsystem-class"></a>Win32 \_ 作業系統類別

**Win32 \_ 作業系統** [WMI 類別](../wmisdk/retrieving-a-class.md)代表安裝在電腦上的 Windows 作業系統。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a>成員

**Win32 \_ 作業系統** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ 作業系統** 類別具有這些方法。



| 方法                                                                                     | 描述                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**重新啟動**](reboot-method-in-class-win32-operatingsystem.md)                             | 關機後再重新開機電腦系統。<br/>                                                                                                                                                                                                           |
| [**SetDateTime**](setdatetime-method-in-class-win32-operatingsystem.md)                   | 允許設定電腦日期和時間。<br/>                                                                                                                                                                                                                |
| [**關閉**](shutdown-method-in-class-win32-operatingsystem.md)                         | 將程式和 Dll 卸載至關閉電腦的安全點。<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | 提供 Windows 作業系統所支援的一組完整關機選項。<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | 提供 **Win32 \_ 作業系統** 中 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)方法所支援的相同關機選項組，但也可讓您指定批註、關機原因或超時。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ 作業系統** 類別具有這些屬性。

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| DRIVE \_ MAP \_ INFO \| btInt13Unit" ) 
</dt> </dl>

Windows 作業系統啟動所在之磁片磁碟機的名稱。

範例： " \\ \\ Device \\ Harddisk0"

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber" ) 
</dt> </dl>

作業系統的組建編號。 它可用於比產品發行版本號碼更精確的版本資訊。

範例： "1381"

</dd> <dt>

**BuildType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType" ) 
</dt> </dl>

用於作業系統的組建類型。

範例： "" retail build ""、"checked build" "

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短描述（單行字串）。 字串包含作業系統版本。 例如「Microsoft Windows 7 企業版」。 這個屬性可以當地語系化。

**Windows Vista 和 windows 7：** 這個屬性可包含尾端的字元。 例如，包含的字串 "Microsoft Windows 7 企業版" (尾端空格) 可能需要使用這個屬性來取得資訊。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (6) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API language \| Language Support 函數 \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ IDEFAULTANSICODEPAGE" ) 
</dt> </dl>

作業系統所使用的字碼頁值。 字碼頁包含作業系統用來轉譯不同語言之字串的字元資料表。 美國國家標準局 (ANSI) 會列出代表已定義字碼頁的值。 如果作業系統未使用 ANSI 字碼頁，此成員會設定為 0 (零) 。 **CodeSet** 字串最多可以使用六個字元來定義字碼頁值。

範例： "1255"

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 國家語言支援函式 \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ICOUNTRY" ) 
</dt> </dl>

作業系統使用的國家/地區代碼。 值是以國際電話撥號首碼為基礎，也稱為 IBM 國家/地區代碼。 這個屬性可以使用最多六個字元來定義國家/地區代碼值。

範例： "1" (美國) 

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍電腦系統的建立類別名稱。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**" ) 
</dt> </dl>

以 **Null** 終止的字串，表示電腦上所安裝的最新 service pack。 如果未安裝 service pack，則字串為 **Null**。

範例： "Service Pack 3"

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍電腦系統的名稱。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

資料類型： **sint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "分鐘" ) 
</dt> </dl>

以分鐘為單位的作業系統與格林尼治平均時間 (GMT) 的位移。 此數位為正數、負數或零。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**DataExecutionPrevention \_ 32BitApplications**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

當資料執行防止硬體功能可供使用時，此屬性會指出該功能已設定為適用于32位應用程式（如果 **為 True**）。 在64位的電腦上，資料執行防止功能是在 [開機設定資料 (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) 存放區中設定，而且 **Win32 \_ 作業系統** 中的屬性會據以進行設定。

</dd> <dt>

**DataExecutionPrevention \_ 可用**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

「資料執行防止」是一項硬體功能，可在資料類型記憶體頁面上停止執行程式碼，以防止緩衝區溢位的攻擊。 若 **為 True**，則可使用這項功能。 在64位的電腦上，會在 BCD 存放區中設定資料執行防止功能，並據此設定 **Win32 \_ 作業系統** 中的屬性。

</dd> <dt>

**DataExecutionPrevention \_ 驅動程式**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

當資料執行防止硬體功能可供使用時，此屬性會指出該功能已設定為適用于驅動程式（如果 **為 True**）。 在64位的電腦上，會在 BCD 存放區中設定資料執行防止功能，並據此設定 **Win32 \_ 作業系統** 中的屬性。

</dd> <dt>

**DataExecutionPrevention \_ SupportPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

指出套用 (DEP) 設定的資料執行防止。 DEP 設定會指定 DEP 套用至系統上32位應用程式的範圍。 DEP 一律會套用至 Windows 核心。

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**一律關閉** (0) 


</dt> <dd>

電腦上所有32位應用程式的 DEP 都會關閉，且不會發生例外狀況。 使用者介面無法使用此設定。

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1) 


</dt> <dd>

電腦上的所有32位應用程式都已啟用 DEP。 使用者介面無法使用此設定。

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**加入宣告** (2) 


</dt> <dd>

DEP 已啟用有限的二進位檔、核心和所有 Windows 服務的數目。 不過，它預設會針對所有32位應用程式關閉。 使用者或系統管理員必須明確選擇 **Always On** 或選擇 **退出** 設定，才能將 DEP 套用至32位應用程式。

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**退出** (3) 


</dt> <dd>

預設會針對所有32位應用程式啟用 DEP。 使用者或系統管理員可以將應用程式新增至例外狀況清單，以明確移除32位應用程式的支援。

</dd> </dl>

</dd> <dt>

**偵錯**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ DEBUG" ) 
</dt> </dl>

作業系統是已檢查的 () 組建的偵錯工具。 若 **為 True**，則會安裝偵錯工具版本。 已檢查的組建提供錯誤檢查、引數驗證和系統偵錯工具代碼。 已檢查二進位檔中的其他程式碼會產生內核偵錯工具錯誤訊息，並中斷偵錯工具。 這有助於立即判斷錯誤的原因和位置。 由於執行的額外程式碼，效能可能會受到已檢查組建的影響。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Description" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

Windows 作業系統的描述。 某些使用者介面（例如允許編輯此描述的使用者介面）會將其長度限制為48個字元。

</dd> <dt>

**分散式**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則會將作業系統分散到數個電腦系統節點。 如果是，則應該將這些節點分組為叢集。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安全交易的加密層級：40位、128位或 *n* 位。

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

**40** 位 (0) 


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

**128** 位 (1) 


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

**n 位** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ForegroundApplicationBoost**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation" ) 
</dt> </dl>

提高優先順序會給予前景應用程式。 應用程式提升的執行方式，是讓應用程式更多的執行時間配量 (量子長度) 。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (0) 


</dt> <dd>

系統會將量子長度提升為6。

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**最小** (1) 


</dt> <dd>

系統會將量子長度提高12。

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**最大** (2) 


</dt> <dd>

系統會將量子長度提高18。

</dd> </dl>

</dd> <dt>

**FreePhysicalMemory**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

目前未使用且可用的實體記憶體數目（以 kb 為單位）。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**FreeSpaceInPagingFiles**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統記憶體設定 \| 001.4 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") 
</dt> </dl>

可以對應到作業系統分頁檔的數位（以 kb 為單位），而不會造成其他任何頁面交換。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**FreeVirtualMemory**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

目前未使用且可用的虛擬記憶體數目（以 kb 為單位）。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

已安裝日期物件。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**LargeSystemCache**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

這個屬性已過時，不受支援。

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**針對應用程式優化** (0) 


</dt> <dd>

優化應用程式的記憶體。

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**針對系統效能優化** (1) 


</dt> <dd>

優化記憶體的系統效能。

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業系統上次重新開機的日期和時間。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**>datetimeoffset.localdatetime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemDate "，" MIF。DMTF \| 一般資訊 \| 001.6 ") 
</dt> </dl>

本機日期和當日時間的作業系統版本。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**地區設定**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 國家語言支援函式 \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ILANGUAGE" ) 
</dt> </dl>

作業系統所使用的語言識別項。 語言識別項是國家/地區的標準國際數位縮寫。 每種語言都有唯一的語言識別項 (LANGID) ，它是由主要語言識別項和次要語言識別項組成的16位值。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

作業系統製造商的名稱。 如果是以 Windows 為基礎的系統，此值會是 "Microsoft Corporation"。

</dd> <dt>

**MaxNumberOfProcesses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemMaxProcesses ") 
</dt> </dl>

作業系統可支援的進程內容數目上限。 提供者所設定的預設值為 4294967295 (0xFFFFFFFF) 。 如果沒有固定的最大值，此值應為 0 (零) 。 在具有固定最大值的系統上，此物件可協助診斷到達最大值時所發生的失敗，如果不明，請輸入 4294967295 (0xFFFFFFFF) 。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**MaxProcessMemorySize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

可以配置給進程的最大記憶體數目（以 kb 為單位）。 對於沒有虛擬記憶體的作業系統，通常此值等於實體記憶體的總數量減去 BIOS 和作業系統所使用的記憶體。 對於某些作業系統而言，這個值可能是無限大的，在此情況下，應該輸入 0 (零) 。 在其他情況下，此值可以是常數，例如2G 或4G。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**MUILanguages**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

電腦上安裝的多語系消費者介面套件 (MUI 套件 ) 語言。 例如，"en-us"。 MUI 套件語言是可安裝在英文版作業系統上的資源檔。 安裝 MUI 套件之後，您可以將使用者介面語言變更為33支援的語言之一。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦系統內的作業系統實例。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**NumberOfLicensedUsers**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業系統的使用者授權數目。 如果沒有限制，請輸入 0 (零) 。 如果不明，請輸入-1。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**NumberOfProcesses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemProcesses ") 
</dt> </dl>

目前已載入或正在作業系統上執行的進程內容數目。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**Numberofusers 位**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemNumUsers ") 
</dt> </dl>

作業系統目前儲存狀態資訊的使用者會話數目。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**OperatingSystemSKU**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

作業系統的庫存單位 (SKU) 號碼。 這些值與在 WinNT 中定義的 ** \_ \* PRODUCT* _ 常數相同，與 [_ *GetProductInfo* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo)函數搭配使用。

下列清單列出可能的 SKU 值。

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**產品 \_未定義** (0) 


</dt> <dd>

未定義

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**產品 \_旗艦** (1) 


</dt> <dd>

旗艦版，例如 Windows Vista 旗艦版。

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**產品 \_HOME \_ BASIC** (2) 


</dt> <dd>

Home Basic 版

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**產品 \_HOME \_ PREMIUM** (3) 


</dt> <dd>

Home Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**產品 \_ENTERPRISE** (4) 


</dt> <dd>

企業版

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**產品 \_BUSINESS** (6) 


</dt> <dd>

Business Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**產品 \_標準 \_ 伺服器** (7) 


</dt> <dd>

Windows Server Standard Edition (桌面體驗安裝) 

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**產品 \_DATACENTER \_ SERVER** (8) 


</dt> <dd>

Windows Server Datacenter Edition (桌面體驗安裝) 

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**產品 \_SMALLBUSINESS \_ SERVER** (9) 


</dt> <dd>

Small Business Server 版本

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**產品 \_企業 \_ 伺服器** (10) 


</dt> <dd>

Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**產品 \_入門** (11) 


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**產品 \_DATACENTER \_ SERVER \_ CORE** (12) 


</dt> <dd>

Datacenter Server Core Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**產品 \_標準 \_ SERVER \_ CORE** (13) 


</dt> <dd>

標準 Server Core 版本

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**產品 \_ENTERPRISE \_ SERVER \_ CORE** (14) 


</dt> <dd>

Enterprise Server Core 版

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**產品 \_WEB \_ 伺服器** (17) 


</dt> <dd>

Web 服務器版本

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**產品 \_HOME \_ SERVER** (19) 


</dt> <dd>

Home Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**產品 \_STORAGE \_ EXPRESS \_ SERVER** (20) 


</dt> <dd>

Storage Express Server 版本

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**產品 \_STORAGE \_ STANDARD \_ SERVER** (21) 


</dt> <dd>

Windows Storage Server Standard Edition (桌面體驗安裝) 

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**產品 \_STORAGE \_ WORKGROUP \_ SERVER** (22) 


</dt> <dd>

Windows Storage Server Workgroup Edition (桌面體驗安裝) 

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**產品 \_STORAGE \_ ENTERPRISE \_ SERVER** (23) 


</dt> <dd>

Storage Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**產品 \_SERVER \_ FOR \_ SMALLBUSINESS** (24) 


</dt> <dd>

適用于 Small Business Edition 的伺服器

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**產品 \_SMALLBUSINESS \_ SERVER \_ PREMIUM** (25) 


</dt> <dd>

Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**產品 \_企業 \_ N** (27) 


</dt> <dd>

Windows Enterprise Edition

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**產品 \_終極 \_ N** (28) 


</dt> <dd>

Windows 旗艦版

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**產品 \_WEB \_ SERVER \_ CORE** (29) 


</dt> <dd>

Windows Server Web Server Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**產品 \_STANDARD \_ SERVER \_ V** (36) 


</dt> <dd>

不含 Hyper-v 的 Windows Server Standard Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**產品 \_DATACENTER \_ SERVER \_ V** (37) 


</dt> <dd>

沒有 Hyper-v 的 Windows Server Datacenter Edition (完整安裝) 

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**產品 \_ENTERPRISE \_ SERVER \_ V** (38) 


</dt> <dd>

沒有 Hyper-v 的 Windows Server Enterprise Edition (完整安裝) 

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**產品 \_DATACENTER \_ SERVER \_ CORE \_ V** (39) 


</dt> <dd>

沒有 Hyper-v 的 Windows Server Datacenter Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**產品 \_標準 \_ SERVER \_ CORE \_ V** (40) 


</dt> <dd>

沒有 Hyper-v 的 Windows Server Standard Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**產品 \_ENTERPRISE \_ SERVER \_ CORE \_ V** (41) 


</dt> <dd>

沒有 Hyper-v 的 Windows Server Enterprise Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**產品 \_HYPERV** (42) 


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**產品 \_STORAGE \_ EXPRESS \_ SERVER \_ CORE** (43) 


</dt> <dd>

Storage Server Express Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**產品 \_STORAGE \_ STANDARD \_ SERVER \_ CORE** (44) 


</dt> <dd>

Storage Server Standard Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**產品 \_STORAGE \_ WORKGROUP \_ SERVER \_ CORE** (45) 


</dt> <dd>

Storage Server Workgroup Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**產品 \_STORAGE \_ ENTERPRISE \_ SERVER \_ CORE** (46) 


</dt> <dd>

Storage Server Workgroup Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**產品 \_PROFESSIONAL** (48) 


</dt> <dd>

Windows 專業版

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**產品 \_SB \_ 解決方案 \_ 伺服器** (50) 


</dt> <dd>

Windows Server Essentials (桌面體驗安裝) 

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**產品 \_SMALLBUSINESS \_ SERVER \_ PREMIUM \_ CORE** (63) 


</dt> <dd>

Small Business Server Premium (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**產品 \_CLUSTER \_ SERVER \_ V** (64) 


</dt> <dd>

不含 Hyper-v 的 Windows Compute Cluster Server

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**產品 \_核心 \_ ARM** (97) 


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**產品 \_CORE** (101) 


</dt> <dd>

Windows 首頁

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**產品 \_PROFESSIONAL \_ WMC** (103) 


</dt> <dd>

具有 Media Center 的 Windows 專業版

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**產品 \_MOBILE \_ CORE** (104) 


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**產品 \_IOTUAP** (123) 


</dt> <dd>

Windows IoT (物聯網) 核心

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**產品 \_DATACENTER \_ NANO \_ server** (143) 


</dt> <dd>

Windows Server Datacenter Edition (Nano Server 安裝) 

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**產品 \_標準 \_ NANO \_ SERVER** (144) 


</dt> <dd>

Windows Server Standard Edition (Nano Server 安裝) 

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**產品 \_DATACENTER \_ WS \_ SERVER \_ CORE** (147) 


</dt> <dd>

Windows Server Datacenter Edition (Server Core 安裝) 

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**產品 \_標準 \_ WS \_ SERVER \_ CORE** (148) 


</dt> <dd>

Windows Server Standard Edition (Server Core 安裝) 

</dd> </dl>

</dd> <dt>

組織
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization" ) 
</dt> </dl>

作業系統註冊使用者的公司名稱。

範例： "Microsoft Corporation"

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業系統的架構，而不是處理器。 這個屬性可以當地語系化。

範例：32位

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| DEFAULT \\ \\ 主控台 \\ \\ 國際 \| 地區設定" ) 
</dt> </dl>

已安裝作業系統的語言版本。 下列清單列出可能的值。 範例： 0x0807 (德文、瑞士) 。

<dt>

1 (0x1) 
</dt> <dd>

阿拉伯文

</dd> <dt>

4 (0x4) 
</dt> <dd>

中文 (簡體) –中國

</dd> <dt>

9 (0x9) 
</dt> <dd>

英文

</dd> <dt>

1025 (0x401) 
</dt> <dd>

阿拉伯文-沙烏地阿拉伯

</dd> <dt>

1026 (0x402) 
</dt> <dd>

保加利亞文

</dd> <dt>

1027 (0x403) 
</dt> <dd>

卡達隆尼亞文

</dd> <dt>

1028 (0x404) 
</dt> <dd>

繁體中文) -臺灣 (

</dd> <dt>

1029 (0x405) 
</dt> <dd>

捷克文

</dd> <dt>

1030 (0x406) 
</dt> <dd>

丹麥文

</dd> <dt>

1031 (0x407) 
</dt> <dd>

德文 – 德國

</dd> <dt>

1032 (0x408) 
</dt> <dd>

希臘文

</dd> <dt>

1033 (0x409) 
</dt> <dd>

英文-美國

</dd> <dt>

1034 (0x40A) 
</dt> <dd>

西班牙文-傳統排序

</dd> <dt>

1035 (0x40B) 
</dt> <dd>

芬蘭文

</dd> <dt>

1036 (0x40C) 
</dt> <dd>

法文 – 法國

</dd> <dt>

1037 (0x40D) 
</dt> <dd>

Hebrew

</dd> <dt>

1038 (0x40E) 
</dt> <dd>

匈牙利文

</dd> <dt>

1039 (0x40F) 
</dt> <dd>

冰島文

</dd> <dt>

1040 (0x410) 
</dt> <dd>

義大利文 – 義大利

</dd> <dt>

1041 (0x411) 
</dt> <dd>

日文

</dd> <dt>

1042 (0x412) 
</dt> <dd>

韓文

</dd> <dt>

1043 (0x413) 
</dt> <dd>

荷蘭文 – 荷蘭

</dd> <dt>

1044 (0x414) 
</dt> <dd>

挪威文–博克瑪律

</dd> <dt>

1045 (0x415) 
</dt> <dd>

波蘭文

</dd> <dt>

1046 (0x416) 
</dt> <dd>

葡萄牙文 – 巴西

</dd> <dt>

1047 (0x417) 
</dt> <dd>

Rhaeto-Romanic

</dd> <dt>

1048 (0x418) 
</dt> <dd>

羅馬尼亞文

</dd> <dt>

1049 (0x419) 
</dt> <dd>

俄文

</dd> <dt>

1050 (0x41A) 
</dt> <dd>

克羅埃西亞文

</dd> <dt>

1051 (0x41B) 
</dt> <dd>

斯洛伐克文

</dd> <dt>

1052 (0x41C) 
</dt> <dd>

阿爾巴尼亞文

</dd> <dt>

1053 (0x41D) 
</dt> <dd>

瑞典文

</dd> <dt>

1054 (0x41E) 
</dt> <dd>

泰文

</dd> <dt>

1055 (0x41F) 
</dt> <dd>

土耳其文

</dd> <dt>

1056 (0x420) 
</dt> <dd>

烏都文

</dd> <dt>

1057 (0x421) 
</dt> <dd>

印尼文

</dd> <dt>

1058 (0x422) 
</dt> <dd>

烏克蘭文

</dd> <dt>

1059 (0x423) 
</dt> <dd>

白俄羅斯文

</dd> <dt>

1060 (0x424) 
</dt> <dd>

斯洛維尼亞文

</dd> <dt>

1061 (0x425) 
</dt> <dd>

愛沙尼亞文

</dd> <dt>

1062 (0x426) 
</dt> <dd>

拉脫維亞文

</dd> <dt>

1063 (0x427) 
</dt> <dd>

立陶宛文

</dd> <dt>

1065 (0x429) 
</dt> <dd>

波斯文

</dd> <dt>

1066 (0x42A) 
</dt> <dd>

越南文

</dd> <dt>

1069 (0x42D) 
</dt> <dd>

巴斯克文 (巴斯克)

</dd> <dt>

1070 (0x42E) 
</dt> <dd>

塞爾維亞文

</dd> <dt>

1071 (0x42F) 
</dt> <dd>

馬其頓 (北美洲馬其頓) 

</dd> <dt>

1072 (0x430) 
</dt> <dd>

Sutu

</dd> <dt>

1073 (0x431) 
</dt> <dd>

Tsonga

</dd> <dt>

1074 (0x432) 
</dt> <dd>

茨瓦納語

</dd> <dt>

1076 (0x434) 
</dt> <dd>

科薩文

</dd> <dt>

1077 (0x435) 
</dt> <dd>

祖魯文

</dd> <dt>

1078 (0x436) 
</dt> <dd>

南非荷蘭文

</dd> <dt>

1080 (0x438) 
</dt> <dd>

法羅文

</dd> <dt>

1081 (0x439) 
</dt> <dd>

Hindi

</dd> <dt>

1082 (0x43A) 
</dt> <dd>

馬爾他文

</dd> <dt>

1084 (0x43C) 
</dt> <dd>

蘇格蘭蓋爾文 (英國) 

</dd> <dt>

1085 (0x43D) 
</dt> <dd>

意第緒文

</dd> <dt>

1086 (0x43E) 
</dt> <dd>

馬來–馬來西亞

</dd> <dt>

2049 (0x801) 
</dt> <dd>

阿拉伯文–伊拉克

</dd> <dt>

2052 (0x804) 
</dt> <dd>

中文 (簡化) –中國

</dd> <dt>

2055 (0x807) 
</dt> <dd>

德文–瑞士

</dd> <dt>

2057 (0x809) 
</dt> <dd>

英文-英國

</dd> <dt>

2058 (0x80A) 
</dt> <dd>

西班牙文–墨西哥

</dd> <dt>

2060 (0x80C) 
</dt> <dd>

法文-比利時

</dd> <dt>

2064 (0x810) 
</dt> <dd>

義大利文–瑞士

</dd> <dt>

2067 (0x813) 
</dt> <dd>

荷蘭文–比利時

</dd> <dt>

2068 (0x814) 
</dt> <dd>

挪威文–挪威文

</dd> <dt>

2070 (0x816) 
</dt> <dd>

葡萄牙文 (葡萄牙)

</dd> <dt>

2072 (0x818) 
</dt> <dd>

羅馬尼亞文–摩爾多瓦

</dd> <dt>

2073 (0x819) 
</dt> <dd>

俄文–摩爾多瓦

</dd> <dt>

2074 (0x81A) 
</dt> <dd>

塞爾維亞文-拉丁

</dd> <dt>

2077 (0x81D) 
</dt> <dd>

瑞典文–芬蘭

</dd> <dt>

3073 (0xC01) 
</dt> <dd>

阿拉伯文-埃及

</dd> <dt>

3076 (0xC04) 
</dt> <dd>

中文 (傳統) –香港特別行政區

</dd> <dt>

3079 (0xC07) 
</dt> <dd>

德文–奧地利

</dd> <dt>

3081 (0xC09) 
</dt> <dd>

英文-澳大利亞

</dd> <dt>

3082 (0xC0A) 
</dt> <dd>

西班牙文-國際排序

</dd> <dt>

3084 (0xC0C) 
</dt> <dd>

法文-加拿大

</dd> <dt>

3098 (0xC1A) 
</dt> <dd>

塞爾維亞文–斯拉夫

</dd> <dt>

4097 (0x1001) 
</dt> <dd>

阿拉伯文–利比亞

</dd> <dt>

4100 (0x1004) 
</dt> <dd>

中文 (簡體) -新加坡

</dd> <dt>

4103 (0x1007) 
</dt> <dd>

德文–盧森堡

</dd> <dt>

4105 (0x1009) 
</dt> <dd>

英文-加拿大

</dd> <dt>

4106 (0x100A) 
</dt> <dd>

西班牙文-瓜地馬拉

</dd> <dt>

4108 (0x100C) 
</dt> <dd>

法文-瑞士

</dd> <dt>

5121 (0x1401) 
</dt> <dd>

阿拉伯文-阿爾及利亞

</dd> <dt>

5127 (0x1407) 
</dt> <dd>

德文–列支敦斯登

</dd> <dt>

5129 (0x1409) 
</dt> <dd>

英文–紐西蘭

</dd> <dt>

5130 (0x140A) 
</dt> <dd>

西班牙文–哥斯大黎加

</dd> <dt>

5132 (0x140C) 
</dt> <dd>

法文–盧森堡

</dd> <dt>

6145 (0x1801) 
</dt> <dd>

阿拉伯文–摩洛哥

</dd> <dt>

6153 (0x1809) 
</dt> <dd>

英文-愛爾蘭

</dd> <dt>

6154 (0x180A) 
</dt> <dd>

西班牙文–巴拿馬

</dd> <dt>

7169 (0x1C01) 
</dt> <dd>

阿拉伯文–突尼斯

</dd> <dt>

7177 (0x1C09) 
</dt> <dd>

英文-南非

</dd> <dt>

7178 (0x1C0A) 
</dt> <dd>

西班牙文–多明尼加共和國

</dd> <dt>

8193 (0x2001) 
</dt> <dd>

阿拉伯文-阿曼

</dd> <dt>

8201 (0x2009) 
</dt> <dd>

英文–牙買加

</dd> <dt>

8202 (0x200A) 
</dt> <dd>

西班牙文–委內瑞拉

</dd> <dt>

9217 (0x2401) 
</dt> <dd>

阿拉伯文–葉門

</dd> <dt>

9226 (0x240A) 
</dt> <dd>

西班牙文–哥倫比亞

</dd> <dt>

10241 (0x2801) 
</dt> <dd>

阿拉伯文–敘利亞

</dd> <dt>

10249 (0x2809) 
</dt> <dd>

英文-貝里斯

</dd> <dt>

10250 (0x280A) 
</dt> <dd>

西班牙文–秘魯

</dd> <dt>

11265 (0x2C01) 
</dt> <dd>

阿拉伯文–約旦

</dd> <dt>

11273 (0x2C09) 
</dt> <dd>

英文–特立尼達

</dd> <dt>

11274 (0x2C0A) 
</dt> <dd>

西班牙文-阿根廷

</dd> <dt>

12289 (0x3001) 
</dt> <dd>

阿拉伯文-黎巴嫩

</dd> <dt>

12298 (0x300A) 
</dt> <dd>

西班牙文–厄瓜多爾

</dd> <dt>

13313 (0x3401) 
</dt> <dd>

阿拉伯文–科威特

</dd> <dt>

13322 (0x340A) 
</dt> <dd>

西班牙文–智利

</dd> <dt>

14337 (0x3801) 
</dt> <dd>

阿拉伯文–阿拉伯聯合大公國

</dd> <dt>

14346 (0x380A) 
</dt> <dd>

西班牙文-烏拉圭

</dd> <dt>

15361 (0x3C01) 
</dt> <dd>

阿拉伯文–巴林

</dd> <dt>

15370 (0x3C0A) 
</dt> <dd>

西班牙文–巴拉圭

</dd> <dt>

16385 (0x4001) 
</dt> <dd>

阿拉伯文-卡塔爾

</dd> <dt>

16394 (0x400A) 
</dt> <dd>

西班牙文–玻利維亞

</dd> <dt>

17418 (0x440A) 
</dt> <dd>

西班牙文-薩爾瓦多

</dd> <dt>

18442 (0x480A) 
</dt> <dd>

西班牙文–宏都拉斯

</dd> <dt>

19466 (0x4C0A) 
</dt> <dd>

西班牙文–尼加拉瓜

</dd> <dt>

20490 (0x500A) 
</dt> <dd>

西班牙文-波多黎各

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ ProductOptions \| ProductSuite" ) 、 [**BitValues**](../wmisdk/standard-qualifiers.md) ( "Small Business"、"Enterprise"、"BackOffice"、"Communication Server"、"Terminal server"、"Small Business (受限的) "、"Embedded NT"、"Data Center" ) 
</dt> </dl>

已安裝並授權系統產品新增至作業系統。 例如， **OSProductSuite** (0x92) 的146值表示企業、終端機服務和資料中心 (位1、四和七組) 。 下列清單列出可能的值。

<dt>

1 (0x1) 
</dt> <dd>

Microsoft Small Business Server 已安裝完成，但可能已升級至另一個版本的 Windows。

</dd> <dt>

2 (0x2) 
</dt> <dd>

已安裝 Windows Server 2008 Enterprise。

</dd> <dt>

4 (0x4) 
</dt> <dd>

已安裝 Windows BackOffice 元件。

</dd> <dt>

8 (0x8) 
</dt> <dd>

已安裝通訊伺服器。

</dd> <dt>

16 (0x10) 
</dt> <dd>

已安裝終端機服務。

</dd> <dt>

32 (0x20) 
</dt> <dd>

Microsoft Small Business Server 已安裝了嚴格的用戶端授權。

</dd> <dt>

64 (0x40) 
</dt> <dd>

已安裝 Windows Embedded。

</dd> <dt>

128 (0x80) 
</dt> <dd>

已安裝 Datacenter edition。

</dd> <dt>

256 (0x100)
</dt> <dd>

已安裝終端機服務，但只支援一個互動式會話。

</dd> <dt>

512 (0x200) 
</dt> <dd>

已安裝 Windows Home Edition。

</dd> <dt>

1024 (0x400) 
</dt> <dd>

已安裝 Web 服務器版本。

</dd> <dt>

8192 (0x2000) 
</dt> <dd>

已安裝 Storage Server Edition。

</dd> <dt>

16384 (0x4000) 
</dt> <dd>

已安裝 Compute Cluster Edition。

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**OtherTypeDescription**") 
</dt> </dl>

作業系統的類型。 下列清單會識別可能的值。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

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

宏

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


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) 


</dt> <dd></dd> <dt>

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


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) 


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) 


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**WIN95** (16) 


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**WIN98** (17) 


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) 


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WINCE** (19) 


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) 


</dt> <dd></dd> <dt>

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


</dt> <dd>

Solaris

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) 


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31) 


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) 


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) 


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) 


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) 


</dt> <dd></dd> <dt>

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


</dt> <dd></dd> <dt>

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


</dt> <dd></dd> <dt>

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


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) 


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) 


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) 


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) 


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) 


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) 


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**OS/390** (60) 


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (61) 


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (62) 


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OSType**") 
</dt> </dl>

目前作業系統版本的其他描述。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**PAEEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則會由在 Intel 處理器上執行的作業系統啟用 (PAE) 的實體位址延伸模組。 PAE 可讓應用程式處理超過 4 GB 的實體記憶體。 啟用 PAE 時，作業系統會使用三層級的線性位址轉譯，而不是兩個層級。 為應用程式提供更多實體記憶體，可減少將記憶體交換至分頁檔的需求，並提升效能。 若要啟用，PAE，請使用 Boot.ini 檔案中的 "/PAE" 參數。 如需實體位址延伸功能的詳細資訊，請參閱 <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> 。

</dd> <dt>

**PlusProductID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| plus ProductId ") 
</dt> </dl>

不支援。

</dd> <dt>

**PlusVersionNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| plus VersionNumber ") 
</dt> </dl>

不支援。

</dd> <dt>

**PortableOperatingSystem**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定作業系統是否從外部 USB 裝置開機。 若為 true，表示作業系統偵測到在支援的本機連線存放裝置上開機。

**Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個屬性。

</dd> <dt>

**主要**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

指定這是否為主要作業系統。

</dd> <dt>

**ProductType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

其他系統資訊。

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**工作站** (1) 


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**網域控制站** (2) 


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**伺服器** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumLength**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation" ) 
</dt> </dl>

不支援

* * Windows Server 2008 和 Windows Vista： * *

**QuantumLength** 屬性會定義每個量子的時鐘刻度數目。 量子是在切換至其他應用程式之前，允許排程器提供給應用程式的執行時間單位。 當執行緒執行一個量子時，核心會 shutdown 它，並將其移至具有相同優先順序的應用程式佇列結尾。 執行緒的量子的實際長度會因不同的 Windows 平臺而異。 僅限 Windows NT/Windows 2000。

可能的值為。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

**一個刻度** (1) 


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

**兩個刻度** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

不支援

* * Windows Server 2008 和 Windows Vista： * *

**QuantumType** 屬性會指定固定或可變長度的量程。 Windows 預設為可變長度的量子，其中前景應用程式的量子比背景應用程式更長。 Windows Server 預設為固定長度的量程。 量子是在切換到另一個應用程式之前，允許排程器提供給應用程式的執行時間單位。 當執行緒執行一個量子時，核心會 shutdown 它，並將其移至具有相同優先順序的應用程式佇列結尾。 執行緒的量子的實際長度會因不同的 Windows 平臺而異。

可能的值為。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

已 **修正** (1) 


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**變數** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**RegisteredUser**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| >registeredowner" ) 
</dt> </dl>

作業系統的已註冊使用者名稱。

範例： "Ben Smith"

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductId" ) 
</dt> </dl>

作業系統產品序列識別碼。

範例： "10497-OEM-0031416-71674"

</dd> <dt>

**ServicePackMajorVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**" ) 
</dt> </dl>

電腦系統上所安裝 service pack 的主要版本號碼。 如果未安裝 service pack，則值為 0 (零) 。

</dd> <dt>

**ServicePackMinorVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**" ) 
</dt> </dl>

電腦系統上安裝之 service pack 的次要版本號碼。 如果未安裝 service pack，則值為 0 (零) 。

</dd> <dt>

**SizeStoredInPagingFiles**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統記憶體設定 \| 001.3 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") 
</dt> </dl>

作業系統分頁檔案中可儲存的 kb 總數— 0 (零) 表示沒有分頁檔案。 請注意，此數目不代表磁片上分頁檔案的實際實際大小。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素，例如智慧型啟用的硬碟可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 服務狀態適用于系統管理工作，例如磁片的鏡像重新同步處理、重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

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

**SuiteMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**BitMap**](../wmisdk/standard-qualifiers.md) ( "0"、"1"、"2"、"3"、"4"、"5"、"6"、"7"、"8"、"9"、"10" ) 、 [**BitValues**](../wmisdk/standard-qualifiers.md) ( "Windows Server Small Business Edition"、"Windows server、Enterprise Edition"、"Windows server，Backoffice Edition"、"Windows server，communication Edition"、"Microsoft Terminal Services"、"Windows Server，Small Business edition 限制"、"windows Embedded"、"Windows server、Datacenter Edition"、"Single User"、"Windows server、Datacenter edition"、"Windows server、Web edition" ) 
</dt> </dl>

識別系統上可用之產品套件的位旗標。

例如，若要同時指定個人和 BackOffice，請將 **SuiteMask** 設定為 `4 | 512` 或 `516` 。

<dt>

1
</dt> <dd>

小型企業

</dd> <dt>

2
</dt> <dd>

Enterprise

</dd> <dt>

4
</dt> <dd>

BackOffice

</dd> <dt>

8
</dt> <dd>

通訊

</dd> <dt>

16
</dt> <dd>

終端機服務

</dd> <dt>

32
</dt> <dd>

小型企業受限

</dd> <dt>

64
</dt> <dd>

Embedded Edition

</dd> <dt>

128
</dt> <dd>

Datacenter Edition

</dd> <dt>

256
</dt> <dd>

單一使用者

</dd> <dt>

512
</dt> <dd>

Home Edition

</dd> <dt>

1024
</dt> <dd>

Web 服務器版本

</dd> </dl>

</dd> <dt>

**SystemDevice**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Registry 函數 \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| Paths \| TargetDevice" ) 
</dt> </dl>

作業系統安裝所在的實體磁碟分割。

</dd> <dt>

**SystemDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊函數 [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)) 
</dt> </dl>

作業系統的系統目錄。

範例： "C： \\ WINDOWS \\ SYSTEM32"

</dd> <dt>

**SystemDrive**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業系統所在磁片磁碟機的字母。 範例： "C："

</dd> <dt>

**TotalSwapSpaceSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

交換空間總計（以 kb 為單位）。 如果交換空間與分頁檔不區分，則此值可能是 **Null** (未指定) 。 不過，有些作業系統會區分這些概念。 例如，在 UNIX 中，當免費頁面清單落在低於指定的數量時，可以將整個進程交換。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**TotalVirtualMemorySize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

虛擬記憶體的數目（以 kb 為單位）。 例如，這可能是藉由將總 RAM 的數量新增至分頁空間量來計算，也就是將電腦系統的記憶體數量新增或匯總至屬性 **SizeStoredInPagingFiles**。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**TotalVisibleMemorySize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

作業系統可用的實體記憶體總量（以 kb 為單位）。 此值不一定會指出真正的實體記憶體數量，而是向作業系統回報的可用記憶體。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Version" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion，dwMinorVersion" ) 
</dt> </dl>

作業系統的版本號碼。

範例： "4.0"

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊函數 \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)" ) 
</dt> </dl>

作業系統的 Windows 目錄。

範例： "C： \\ WINDOWS"

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 作業系統** 類別衍生自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。

可以安裝在可執行 Windows 作業系統之電腦上的任何作業系統都是此類別的子系或成員。 **Win32 \_作業系統** 是單一類別。 若要取得單一實例，請使用 "@" 作為索引鍵。

不同于 Mgmtclassgen.exe 所產生的其他大部分 WMI 類別， **作業系統 CreateInstance** () 方法會傳回空白的 **作業系統** 物件。 因此，如果您使用 C 搭配 \# mgmtclassgen.exe，您可以使用下列程式碼：


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>範例

您可以在 [**win32 \_ 處理器**](win32-processor.md)主題範例中找到 VBScript 範例，以取得 [**win32 \_**](win32-computersystem.md)系統、 [**win32 \_ 處理器**](win32-processor.md)和 **win32 作業系統 \_** 的作業系統和處理器資料。

在 TechNet 資源庫上 [使用 powershell powershell 範例產生 Exchange 環境報告](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) ，會使用 **Win32 \_ 作業系統** 類別做為較大應用程式的一部分，以產生 Exchange 環境報告。

TechNet 資源庫中的「 [使用 WMI 取得伺服器執行時間](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) 」範例會使用 **LastBootupTime** 屬性來判斷伺服器的作用時間。 此範例也會使用 timeout 選項，以確保 WMI 呼叫不會停止回應。

TechNet 資源庫上的 [WMI 資訊](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) 取回程序 VBScript 程式碼範例會使用 **Win32 \_ 作業系統** 類別，從多部遠端電腦抓取作業系統資訊。

下列腳本會取得預設「根 CIMv2」命名空間中的 **Win32 \_ 作業系統** 實例 \\ ，然後顯示作業系統的相關資訊。


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



下列 PowerShell 程式碼範例會顯示有關目前作業系統的所有操作資訊。


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
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

[**CIM \_ 作業系統**](cim-operatingsystem.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> <dt>

[WMI 工作：作業系統](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[WMI 工作：電腦硬體](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[WMI 工作：桌面管理](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 

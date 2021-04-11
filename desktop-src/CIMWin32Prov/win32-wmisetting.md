---
description: Win32 \_ WMISetting 單一 wmi 類別包含 wmi 服務的指令引數。 這個類別只能有一個實例，每個 Windows 系統一律會有一個實例，而且無法刪除。 無法建立其他實例。
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847073"
---
# <a name="win32_wmisetting-class"></a>Win32 \_ WMISetting 類別

**Win32 \_ WMISetting** 單一 [wmi 類別](../wmisdk/retrieving-a-class.md)包含 wmi 服務的指令引數。 這個類別只能有一個實例，每個 Windows 系統一律會有一個實例，而且無法刪除。 無法建立其他實例。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a>成員

**Win32 \_ WMISetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ WMISetting** 類別具有這些屬性。

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ 腳本 \| 預設命名空間" ) 
</dt> </dl>

預設腳本命名空間。 如果呼叫端未指定，則此屬性包含從 WMI 的腳本 API 呼叫所使用的命名空間。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本 \| 預設命名空間**    

範例：根 \\ cimv2

如需使用這個屬性的範例腳本，請參閱「備註」一節。

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ 腳本 \| 啟用 ASP" ) 
</dt> </dl>

若 **為 True，則** 可在 Active Server PAGES (ASP) 上使用 WMI 腳本。 這個屬性在執行不支援之 Windows 版本的系統上是有效的。 針對支援的 Windows 系統，ASP 上一律允許 WMI 腳本處理。

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| mof" ) 
</dt> </dl>

用來初始化或復原 WMI 儲存機制的完整 MOF 檔案名清單。 此清單決定 MOF 檔案的編譯順序。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| 自動回復 mof**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X" ) 
</dt> </dl>

不支援。

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**請勿開始** (0) 


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Autostart** (1) 


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**在重新開機時開始** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**BackupInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 備份間隔閾值」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) 
</dt> </dl>

不支援。 請改以手動方式備份 WMI 存放庫。

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Time 函數 \| GetTimeZoneInformation" ) 
</dt> </dl>

上次執行備份的日期和時間。

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Build" ) 
</dt> </dl>

目前已安裝之 WMI 服務的版本資訊。

在 WMI 資料庫的備份之間經過的時間長度。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| 組建**

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Repository Directory" ) 
</dt> </dl>

包含 WMI 存放庫的目錄路徑。

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB Size" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) 
</dt> </dl>

WMI 存放庫的大小上限。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections" ) 
</dt> </dl>

不支援。

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents" ) 
</dt> </dl>

若 **為 True**，則應啟用 WMI 事件子系統。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation" ) 
</dt> </dl>

若 **為 True**，當 wmi 初始化時，wmi 會使用 **LastStartupHeapPreallocation** 值的大小來建立預先配置的堆積。

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| 在用戶端物件上的高閾值」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒的物件數」 ) 
</dt> </dl>

提供者建立的物件可以傳遞至用戶端的最大速率。 為了配合提供者與用戶端之間的速度差異，WMI 會將物件保留在佇列中，再將它們傳遞給取用者。 為了提高效率，取用者必須以符合提供者的步調來收集物件。 如果未回收物件所持有的記憶體達到 **LowThresholdOnObjects**，WMI 就會減緩將新物件排入佇列中的速度。 如果未回收事件持續累積，而且當使用的記憶體是在 **HighThresholdOnClientObjects** 中的值時，就會達到 **MaxWaitOnClientObjects** 中傳遞事件的最大等待時間，然後 WMI 不會接受來自提供者的物件，並將 **WBEM \_ E \_ \_ 的 \_ 記憶體** 傳回給用戶端。

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| ) 事件上的高臨界值"，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒事件數」 ) 
</dt> </dl>

事件傳遞至用戶端的最大速率。 為了配合提供者與用戶端之間的速度差異，WMI 會將事件排入佇列，然後再傳遞給取用者。 為了提高效率，取用者必須以符合提供者的步調來收集事件。 如果未回收事件所保留的記憶體達到 **LowThresholdOnObjects**，WMI 就會減緩將新事件排入佇列中的速度。 如果未回收事件持續累積，而且當使用的記憶體是在 **HighThresholdOnEvents** 中的值時，就會達到 **MaxWaitOnEvents** 中傳遞事件的最大等待時間，WMI 不接受來自提供者的其他事件，並將 **WBEM \_ E \_ \_ 的 \_ 記憶體** 傳回給用戶端。

> [!Note]  
> 節流只適用于永久事件取用者，因此當事件在 WMI 內部事件佇列中備份時，暫時取用者不應預期進行節流。

 

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 的用戶端物件上的高閾值 (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| 安裝目錄" ) 
</dt> </dl>

已安裝 WMI 軟體的目錄路徑。 預設位置為 \\ System32 \\ Wbem。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| 安裝目錄**

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

WMI 在初始化期間所建立之預先配置堆積的大小。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 記錄目錄" ) 
</dt> </dl>

目錄路徑，其中包含 WMI 系統記錄檔的位置。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| 記錄目錄**

</dd> <dt>

**Logginglevel.information**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 記錄" ) 
</dt> </dl>

啟用事件記錄和使用的記錄詳細程度。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| 記錄**

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Off** (0) 


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**錯誤記錄** (1) 


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**詳細的錯誤記錄** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| 的用戶端物件上的低臨界值" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒的物件數」 ) 
</dt> </dl>

WMI 開始為用戶端建立的新物件建立速度變慢的速率。 為了配合提供者與用戶端之間的速度差異，WMI 會將物件保留在佇列中，再將它們傳遞給取用者。 為了提高效率，取用者必須以符合提供者的步調來收集物件。 如果物件要求的速率達到 **LowThresholdOnClientObjects**，WMI 就會逐漸降低建立新物件的速度，以符合用戶端的使用率。 當建立物件的速率超過此屬性的值時，就會導致這個緩慢的啟動。 請參閱 **HighThresholdOnClientObjects**。

這個屬性會反映登錄值。

**金鑰 \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 的用戶端物件上的高閾值 (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| ) 事件的低閾值"，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒事件數」 ) 
</dt> </dl>

WMI 開始減緩新事件傳遞速度的速率。 為了配合提供者與用戶端之間的速度差異，WMI 會將事件排入佇列，然後再傳遞給取用者。 為了提高效率，取用者必須以符合提供者的步調來收集物件。 如果佇列的控制權超出控制權，WMI 節流會使事件的傳遞逐漸下降，以符合用戶端的速率。 當產生事件的速率超過此屬性的值時，就會啟動此緩慢。 請參閱 **HighThresholdOnEvents**。

> [!Note]  
> 節流只適用于永久事件取用者，因此當事件在 WMI 內部事件佇列中備份時，暫時取用者不應預期進行節流。

 

這個屬性會反映登錄值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 在用戶端物件上的高閾值 {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 記錄檔大小上限」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) 
</dt> </dl>

WMI 服務所產生之記錄檔的大小上限。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| 記錄檔大小上限**

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| Events Max Wait" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) 
</dt> </dl>

新建立的物件在捨棄之前等候用戶端使用的時間量，並傳回錯誤值。 這個屬性會與 **LowThresholdOnClientObjects** 和 **HighThresholdOnClientObjects** 屬性互動以進行節流：當取用者接收物件的速度太慢時，將物件傳遞給取用者。

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| Events Max Wait" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) 
</dt> </dl>

傳送至用戶端的事件在被捨棄之前排入佇列的時間量。 這個屬性會使用 **LowThresholdOnEvents** 和 **HighThresholdOnEvents** 來進行節流處理—當取用者接收物件的速度太慢時，將物件傳遞給取用者的速度會變慢。

這個屬性會反映登錄值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 的最大等候事件等候 (ms)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory" ) 
</dt> </dl>

將 MOF 檔案安裝到 WMI 存放庫的應用程式目錄路徑。 WMI 會自動編譯放在此目錄中的任何 MOF 檔案，而且根據其成功與否，會將 MOF 移至標示為「良好」或「不良」的子目錄。 如果包含 \# [pragma 自動](../wmisdk/pragma-autorecover.md) 復原命令，則完整檔案名會新增至 WMI 初始化或復原存放庫時所使用的 **AutorecoverMofs** 清單。 此清單決定編譯 Mof 的順序。

這個屬性會反映登錄機碼中的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = 安裝目錄**

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ WMISetting** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。 電腦上只能有一個這個類別的實例。

當您要對 WMI 服務本身的腳本或疑難排解問題進行疑難排解時，瞭解 WMI 在電腦上的設定方式可能會非常有用。 例如，許多 WMI 腳本是以假設根 \\ cimv2 是目的電腦上的預設命名空間來撰寫的。 如此一來，需要存取「根 CIMv2」中類別的腳本寫入器 \\ 通常無法在 GetObject 標記中包含命名空間，如下列程式碼範例所示：

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

如果根 \\ cimv2 不是目的電腦上的預設命名空間，此腳本將會失敗。 為了避免發生這種情況，命名空間根 \\ cimv2 必須包含在標記中，如下列程式碼範例所示：

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

如果目的電腦上的預設命名空間與腳本所假設的命名空間不同，腳本將會失敗。 最重要的是，使用者會看到一些誤導的錯誤訊息「不正確類別」。 老實說，失敗是因為類別無效，但因為在預設命名空間中找不到類別。 這是很難排解的問題，因為您可能會調查類別的可能問題，而不是使用 (的命名空間問題，而在此情況下未) 指定。

您可以使用 **Win32 \_ WMISetting** 類別來判斷電腦上 WMI 的設定方式。 設定詳細資料（例如，預設命名空間或 WMI 組建編號）有助於疑難排解腳本問題。 這些設定也提供重要的系統管理資訊，例如，WMI 錯誤是否記錄在電腦上，以及如果您需要重建 WMI 存放庫，哪些 WMI 提供者會自動重載。

## <a name="examples"></a>範例

TechNet 資源庫上的 [修改 Wmi 設定](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript 程式碼範例會 **使用 \_ Win32 WMISETTING** 類別來設定 WMI 備份間隔和記錄層級。

TechNet 資源庫上 [預設命名空間](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript 程式碼範例的清單，會使用 **Win32 \_ WMISetting** 類別來抓取和顯示目前的 WMI 「腳本的預設命名空間」設定。

TechNet 資源庫上的 [修改預設 Wmi 命名空間](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript 程式碼範例會使用 **ASPScriptDefaultNamespace** 屬性，將 WMI 「腳本的預設命名空間」設定設為「根 \\ cimv2」。

清單中的 [所有 Wmi 設定](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript 程式碼範例會使用 **Win32 \_ WMISetting** 上的許多屬性來傳回電腦上所設定的 wmi 設定清單。

[清單 Wmi 設定資訊](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d)JavaScript 程式碼範例會在 **Win32 \_ WMISetting** 上使用一些屬性，以傳回電腦上所設定的 wmi 設定清單。

[清單 Wmi 設定資訊](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d)Python 程式碼範例會在 **Win32 \_ WMISetting** 上使用一些屬性，以傳回電腦上所設定的 wmi 設定清單。

[清單 WMI 設定資訊](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2)物件 REXX 程式碼範例會使用 **Win32 \_ WMISetting** 上的一些屬性來傳回電腦上所設定的 wmi 設定清單。

下列 VBScript 程式碼範例顯示如何取得在本機電腦上執行的 WMI 版本。 "Win32 \_ WMISetting = @" 表示類別的單一實例。 如需詳細資訊，請參閱 WMI 版本。


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[WMI 服務管理類別](./wmi-service-management-classes.md)
</dt> </dl>

 

 

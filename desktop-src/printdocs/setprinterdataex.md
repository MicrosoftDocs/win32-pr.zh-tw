---
description: SetPrinterDataEx 函數會設定印表機或列印伺服器的設定資料。 此函數會將設定資料儲存在印表機登錄機碼下。
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: 'SetPrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 6d2904c853510efeb379c9d590852c8f082a4644315560c4dfa5a7f51daca6ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460348"
---
# <a name="setprinterdataex-function"></a>SetPrinterDataEx 函式

**SetPrinterDataEx** 函數會設定印表機或列印伺服器的設定資料。 此函數會將設定資料儲存在印表機的登錄機碼下。

## <a name="syntax"></a>語法


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

此函式會設定設定資料之印表機或列印伺服器的控制碼。 使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。

</dd> <dt>

*pKeyName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定包含要設定之值的索引鍵。 如果指定的機碼或子機碼不存在，則函式會建立它們。

若要儲存可在目錄服務 (DS) 中發佈的設定資料，請指定下列其中一個預先定義的登錄機碼。



| 值                                                                                                                                                                      | 意義                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | 印表機驅動程式會使用此金鑰來儲存驅動程式屬性。<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | 保留的。 僅供列印多工緩衝處理器用來儲存內部多工緩衝處理器屬性。<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | 應用程式會使用此金鑰來儲存印表機內容，例如印表機資產號碼。<br/> |



 

只有當架構中有對應的屬性時，儲存在 SPLDS_USER_KEY 機碼下的值才會在目錄服務中發行。 網域系統管理員必須建立屬性（如果尚未存在）。 若要在使用 **SetPrinterDataEx** 來加入或變更值之後發行使用者定義的屬性，請呼叫 [**SetPrinter**](setprinter.md) （ *Level* = 7），並將 [**PRINTER_INFO_7**](printer-info-7.md)的 **dwAction** 成員設為 **DSPRINT_UPDATE**。

您可以指定其他金鑰來儲存非 DS 設定資料。 使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。

如果 *hPrinter* 是印表機的控制碼，而 *pKeyName* 為 **Null** 或空字串，則 **SetPrinterDataEx** 會傳回 **ERROR_INVALID_PARAMETER**。

如果 *hPrinter* 是列印伺服器的控制碼，則會忽略 *pKeyName* 。

請勿使用 **SPLDS_SPOOLER_KEY**。 若要變更多工緩衝處理器印表機屬性，請使用 *Level* = 2 的 [**SetPrinter**](setprinter.md) 。

</dd> <dt>

*pValueName* \[在\]
</dt> <dd>

以 null 結束的字串指標，可識別要設定的資料。

若為印表機，此字串會在 *pKeyName* 索引鍵下指定值的名稱。

針對列印伺服器，這個字串是下列 [備註] 區段中所列的其中一個預先定義的字串。

</dd> <dt>

*類型* \[在\]
</dt> <dd>

表示 *.pdata* 參數所指向之資料類型的代碼。 如需可能的類型代碼清單，請參閱登錄 [數值型別](/windows/desktop/SysInfo/registry-value-types)。

如果 *pKeyName* 指定其中一個預先定義的目錄服務金鑰，則 *類型* 必須是 **REG_SZ**、 **REG_MULTI_SZ**、 **REG_DWORD** 或 **REG_BINARY**。 如果使用 **REG_BINARY** ， *cbData* 必須等於1，而目錄服務會將資料視為布林值。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

包含印表機設定資料之緩衝區的指標。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

陣列的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **ERROR_SUCCESS**。

如果函式失敗，則傳回值會是錯誤值。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

若要取出印表機的現有設定資料或列印多工緩衝處理器，請呼叫 [**GetPrinterDataEx**](getprinterdataex.md) 函式。

使用設定為 "PrinterDriverData" 的 *pKeyName* 參數呼叫 **SetPrinterDataEx** 相當於呼叫 [**SetPrinterData**](setprinterdata.md)函數。

如果 *hPrinter* 是列印伺服器的控制碼， *pValueName* 可以指定下列其中一個預先定義的值。



| 值                                                               | 註解                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_ALLOW_USER_MANAGEFORMS**                                | WindowsXP Service Pack 2 (SP2) 和更新版本<br/> WindowsServer 2003 Service Pack 1 (SP1) 和更新版本<br/>                                                                                                    |
| **SPLREG_BEEP_ENABLED**                                           |                                                                                                                                                                                                                                 |
| **SPLREG_DEFAULT_SPOOL_DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **SPLREG_EVENT_LOG**                                              |                                                                                                                                                                                                                                 |
| **SPLREG_NET_POPUP**                                              | Windows Server 2003 和更新版本中不支援<br/>                                                                                                                                                                       |
| **SPLREG_PORT_THREAD_PRIORITY_DEFAULT**                         |                                                                                                                                                                                                                                 |
| **SPLREG_PORT_THREAD_PRIORITY**                                  |                                                                                                                                                                                                                                 |
| **SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**                        | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**         | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE** | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**                 | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**             | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**              | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG_RETRY_POPUP**                                            | 在成功傳回時，如果伺服器設定為所有作業的 [重試] 快顯視窗， *.pdata* 會包含 1; 如果伺服器不會針對所有作業重試快顯視窗，則為0。<br/> Windows Server 2003 和更新版本中不支援<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows伺服器2003和更新版本<br/>                                                                                                                                                                                        |



 

當發生錯誤時，傳遞下列其中一個預先定義的值做為 *pValueName* 會設定集區列印行為。



| 值                                       | 註解                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | *.Pdata* 的值表示在發生錯誤之後，于另一個埠上重新開機作業的時間（以秒為單位）。 這項設定會搭配 **SPLREG_RESTART_JOB_ON_POOL_ENABLED** 使用。<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | *.Pdata* 中的非零值表示已啟用 **SPLREG_RESTART_JOB_ON_POOL_ERROR** 。<br/>                                                                                            |



 

**SPLREG_RESTART_JOB_ON_POOL_ERROR** 中指定的時間是最短的時間。 實際的時間可能會比較長，取決於下列埠監視器設定，這些設定是此登錄機碼下的登錄值：

**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ monitor \\ < *MonitorName* > \\ 埠**

呼叫 [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) 函數來設定這些值。



| 埠監視器設定     | 資料類型      | 意義                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG_DWORD** | 如果非零值，可讓埠監視器以埠狀態更新多工緩衝處理器。<br/>            |
| **StatusUpdateInterval** | **REG_DWORD** | 指定埠監視器以埠狀態更新多工緩衝處理器時的間隔（以分鐘為單位）。<br/> |



 

為了確保多工緩衝處理程式會將工作重新導向至集區中的下一個可用印表機 (當列印工作未在設定的時間) 內列印時，埠監視器必須支援 SNMP，且集區中的網路埠必須設定為「已啟用 SNMP 狀態」。 支援 SNMP 的埠監視器是標準 TCP/IP 埠監視器。

在 Windows 7 和更新版本的 Windows 中，傳送至列印伺服器的列印工作預設會在用戶端上呈現。 您可以將 *pKeyName* 設定為 "PrinterDriverData"，並 *pValueName* 至下表中的設定值，來設定列印工作的用戶端轉譯。



| 設定                      | 資料類型      | 描述                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG_DWORD** | 值為0，或如果此值不存在於登錄中，則會啟用列印工作的預設用戶端轉譯。<br/> 值為1時，會停用列印工作的用戶端轉譯。<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG_DWORD** | 值為0，或如果此值不存在於登錄中，則會在用戶端上呈現列印工作。 如果無法在用戶端上呈現列印工作，則會在伺服器上轉譯。 如果無法在伺服器上轉譯列印工作，它將會失敗。<br/> 值為1時，會在用戶端上呈現列印工作。 如果無法在用戶端上呈現列印工作，則會失敗。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **SetPrinterDataExW** (Unicode) 和 **SetPrinterDataExA** (ANSI) <br/>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 


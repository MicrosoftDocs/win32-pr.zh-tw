---
description: GetPrinterData 函式會抓取指定印表機或列印伺服器的設定資料。
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: 'GetPrinterData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996844"
---
# <a name="getprinterdata-function"></a>GetPrinterData 函式

**GetPrinterData** 函式會抓取指定印表機或列印伺服器的設定資料。

在 Windows 2000 和更新版本的 Windows 中，呼叫 **GetPrinterData** 相當於呼叫 [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) ，並將 *PKeyName* 參數設定為 "PrinterDriverData"。

## <a name="syntax"></a>語法


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

由函式抓取設定資料之印表機或列印伺服器的控制碼。 使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。

</dd> <dt>

*pValueName* \[在\]
</dt> <dd>

以 null 結束的字串指標，可識別要取出的資料。

針對印表機，此字串是登錄中印表機 "PrinterDriverData" 機碼下的登錄值名稱。

針對列印伺服器，這個字串是下列 [備註] 區段中所列的其中一個預先定義的字串。

</dd> <dt>

*pType* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收表示在 *.pdata* 中取出之資料類型的值。 函數會傳回儲存資料的 [**SetPrinterData**](setprinterdata.md) 或 [**SetPrinterDataEx**](setprinterdataex.md) 呼叫中指定的型別。 如果您不需要資料類型，請將此參數設定為 **Null** 。

</dd> <dt>

*.pdata* \[擴展\]
</dt> <dd>

接收設定資料之緩衝區的指標。

</dd> <dt>

*nSize* \[在\]
</dt> <dd>

*.Pdata* 指向的緩衝區大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收設定資料的大小（以位元組為單位）。 如果 *nSize* 所指定的緩衝區大小太小，則函式會傳回 **錯誤的 \_ \_ 資料**，而 *pcbNeeded* 會指出所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「 **錯誤 \_ 成功**」。 如果函式失敗，則傳回值會是錯誤值。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

**GetPrinterData** 會抓取 [**SetPrinterDataEx**](setprinterdataex.md) 或 [**SetPrinterData**](setprinterdata.md) 函數所設定的印表機設定資料。

**GetPrinterData** 可能會觸發對 [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85))的 Windows 呼叫，這可能會寫入登錄中。 如果有的話，就會發生副作用，例如，如果在網路上共用印表機，則會在用戶端中觸發更新或升級印表機事件識別碼20。

如果 *hPrinter* 是列印伺服器的控制碼， *pValueName* 可以指定下列其中一個預先定義的值。



| 值                                                               | 註解                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ 允許 \_ 使用者 \_ MANAGEFORMS**                                | Windows XP Service Pack 2 (SP2) 和更新版本<br/> Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本<br/>                                                                                                    |
| **SPLREG \_ 架構**                                            |                                                                                                                                                                                                                                 |
| **SPLREG \_ 嗶聲 \_ 已啟用**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ 預設多工 \_ 緩衝處理 \_ 目錄**                               |                                                                                                                                                                                                                                 |
| **SPLREG \_ DNS \_ 電腦 \_ 名稱**                                      |                                                                                                                                                                                                                                 |
| **\_存在 SPLREG DS \_**                                             | 在成功傳回時，如果電腦位於 DS 網域， *.pdata* 會包含0x0001，否則為0。<br/>                                                                                                                         |
| **\_ \_ \_ 為 \_ 使用者提供 SPLREG DS**                                  | 在成功傳回時，如果使用者登入 DS 網域， *.pdata* 會包含0x0001，否則為0。<br/>                                                                                                                   |
| **SPLREG \_ 事件 \_ 記錄檔**                                              |                                                                                                                                                                                                                                 |
| **SPLREG \_ 主要 \_ 版本**                                          |                                                                                                                                                                                                                                 |
| **SPLREG \_ 次要 \_ 版本**                                          |                                                                                                                                                                                                                                 |
| **SPLREG \_ NET \_ 快顯視窗**                                              | Windows Server 2003 和更新版本不支援<br/>                                                                                                                                                                       |
| **SPLREG \_ NET \_ POPUP \_ 至 \_ 電腦**                                | 在成功傳回時，如果工作通知應該傳送至用戶端電腦， *.pdata* 會包含 1; 如果要將工作通知傳送給使用者，則為0。<br/> Windows Server 2003 和更新版本不支援<br/> |
| **SPLREG \_ OS \_ 版本**                                             | Windows XP 及更新版本<br/>                                                                                                                                                                                                 |
| **SPLREG \_ OS \_ VERSIONEX**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ 埠 \_ 執行緒 \_ 優先順序 \_ 預設值**                         |                                                                                                                                                                                                                                 |
| **SPLREG \_ 埠 \_ 執行緒 \_ 優先順序**                                  |                                                                                                                                                                                                                                 |
| **SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 群組**                        | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **\_回收前的 SPLREG 列印 \_ 驅動程式 \_ 隔離 \_ 時間 \_ \_**         | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG \_ 列印 \_ 驅動 \_ 程式 \_ \_ \_ 在回收前隔離的最大物件 \_** | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 空閒 \_ 時間**                 | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG \_ 列印 \_ 驅動程式 \_ 隔離 \_ 執行 \_ 原則**             | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG \_ 列印 \_ 驅動程式 \_ 隔離覆 \_ 寫 \_ 原則**              | Windows 7 和更新版本<br/>                                                                                                                                                                                                  |
| **SPLREG \_ 遠端 \_ 傳真**                                             | 在成功傳回時，如果傳真服務支援遠端用戶端， *.pdata* 會包含0x0001，否則為0。<br/>                                                                                                               |
| **SPLREG \_ 重試 \_ 快顯視窗**                                            | 在成功傳回時，如果伺服器設定為所有作業的 [重試] 快顯視窗， *.pdata* 會包含 1; 如果伺服器不會針對所有作業重試快顯視窗，則為0。<br/> Windows Server 2003 和更新版本不支援<br/> |
| **SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序**                             |                                                                                                                                                                                                                                 |
| **SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序 \_ 預設值**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 和更新版本<br/>                                                                                                                                                                                        |



 

下列 *pValueName* 值指出發生錯誤時的集區列印行為。



| 值                                       | 註解                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_集區 \_ 上的 SPLREG 重新開機作業 \_ \_ \_ 錯誤**   | *.Pdata* 的值表示在發生錯誤之後，于另一個埠上重新開機作業的時間（以秒為單位）。 這項設定會 **\_ \_ \_ 在 \_ \_ 已啟用集區的 SPLREG 重新開機作業** 時使用。<br/> |
| **\_ \_ \_ \_ 已啟用集區上的 SPLREG 重新開機作業 \_** | *.Pdata* 中的非零值表示已啟用 **集區 \_ \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業**。<br/>                                                                                            |



 

在 **\_ 集區 \_ \_ \_ \_ 錯誤的 SPLREG 重新開機作業** 中指定的時間是最短時間。 實際的時間可能會比較長，取決於下列埠監視器設定，這些設定是此登錄機碼下的登錄值：

**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ monitor \\ < *MonitorName* > \\ 埠**

呼叫 [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) 函數來查詢這些值。



| 埠監視器設定     | 資料類型      | 意義                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | 如果非零值，可讓埠監視器以埠狀態更新多工緩衝處理器。<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | 指定埠監視器以埠狀態更新多工緩衝處理器時的間隔（以分鐘為單位）。<br/> |



 

在 Windows 7 和更新版本的 Windows 中，預設會在用戶端上轉譯傳送至列印伺服器的列印工作。 下列值會設定列印工作的用戶端轉譯，如果您在 *pValueName* 中設定下列值，就可以讀取這些值。



| 設定                      | 資料類型      | 描述                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | 值為0，或如果此值不存在於登錄中，則會啟用列印工作的預設用戶端轉譯。<br/> 值為1時，會停用列印工作的用戶端轉譯。<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | 值為0，或如果此值不存在於登錄中，則會在用戶端上呈現列印工作。 如果無法在用戶端上呈現列印工作，則會在伺服器上轉譯。 如果無法在伺服器上轉譯列印工作，它將會失敗。<br/> 值為1時，會在用戶端上呈現列印工作。 如果無法在用戶端上呈現列印工作，則會失敗。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetPrinterDataW** (Unicode) 和 **GetPrinterDataA** (ANSI) <br/>                                   |



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

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> <dt>

[**PRINTPROCESSOR \_ CAPS \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 


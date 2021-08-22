---
description: GetPrinterDataEx 函式會抓取指定印表機或列印伺服器的設定資料。
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: 'GetPrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 146c4f650b646e5b2be9e0ec809221beebe9f596fcb591fe148be615417faa04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034176"
---
# <a name="getprinterdataex-function"></a>GetPrinterDataEx 函式

**GetPrinterDataEx** 函式會抓取指定印表機或列印伺服器的設定資料。 **GetPrinterDataEx** 可以取出 [**SetPrinterData**](setprinterdata.md) 函數所儲存的值。 此外， **GetPrinterDataEx** 可以取出 [**SetPrinterDataEx**](setprinterdataex.md) 函數儲存在指定索引鍵下的值。

## <a name="syntax"></a>語法


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
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

*pKeyName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定包含要抓取之值的索引鍵。 使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。

如果 *hPrinter* 是印表機的控制碼，而 *pKeyName* 為 **Null** 或空字串，則 **GetPrinterDataEx** 會傳回 **錯誤 \_ 不正確 \_ 參數**。

如果 *hPrinter* 是列印伺服器的控制碼，則會忽略 *pKeyName* 。

</dd> <dt>

*pValueName* \[在\]
</dt> <dd>

以 null 結束的字串指標，可識別要取出的資料。

若為印表機，此字串會在 *pKeyName* 索引鍵下指定值的名稱。

針對列印伺服器，這個字串是下列 [備註] 區段中所列的其中一個預先定義的字串。

</dd> <dt>

*pType* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存在值中的資料類型。 當儲存資料時，函數會傳回 [**SetPrinterDataEx**](setprinterdataex.md) 呼叫中指定的型別。 如果您不需要此資訊，這個參數可以是 **Null** 。 **GetPrinterDataEx** 會將 *pType* 當作 [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)函式呼叫的 *lpdwType* 參數傳遞。

</dd> <dt>

*.pdata* \[擴展\]
</dt> <dd>

接收設定資料之緩衝區的指標。

</dd> <dt>

*nSize* \[在\]
</dt> <dd>

*.Pdata* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收設定資料的大小（以位元組為單位）。 如果 *nSize* 所指定的緩衝區大小太小，則函式會傳回 **錯誤的 \_ \_ 資料**，而 *pcbNeeded* 會指出所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「 **錯誤 \_ 成功**」。

如果函式失敗，則傳回值會是錯誤值。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

**GetPrinterDataEx** 會抓取 [**SetPrinterDataEx**](setprinterdataex.md) 和 [**SetPrinterData**](setprinterdata.md) 函式所設定的印表機設定資料。

使用設定為 "PrinterDriverData" 的 *pKeyName* 參數呼叫 **GetPrinterDataEx** 相當於呼叫 [**GetPrinterData**](getprinterdata.md)函數。

如果 *hPrinter* 是列印伺服器的控制碼， *pValueName* 可以指定下列其中一個預先定義的值。



| 值                                                               | 註解                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ 允許 \_ 使用者 \_ MANAGEFORMS**                                | WindowsXP Service Pack 2 (SP2) 和更新版本<br/> WindowsServer 2003 Service Pack 1 (SP1) 和更新版本<br/>                                                                                                    |
| **SPLREG \_ 架構**                                            |                                                                                                                                                                                                                                 |
| **SPLREG \_ 嗶聲 \_ 已啟用**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ 預設多工 \_ 緩衝處理 \_ 目錄**                               |                                                                                                                                                                                                                                 |
| **SPLREG \_ DNS \_ 電腦 \_ 名稱**                                      |                                                                                                                                                                                                                                 |
| **\_存在 SPLREG DS \_**                                             | 在成功傳回時，如果電腦位於 DS 網域， *.pdata* 會包含0x0001，否則為0。<br/>                                                                                                                         |
| **\_ \_ \_ 為 \_ 使用者提供 SPLREG DS**                                  | 在成功傳回時，如果使用者登入 DS 網域， *.pdata* 會包含0x0001，否則為0。<br/>                                                                                                                   |
| **SPLREG \_ 事件 \_ 記錄檔**                                              |                                                                                                                                                                                                                                 |
| **SPLREG \_ 主要 \_ 版本**                                          |                                                                                                                                                                                                                                 |
| **SPLREG \_ 次要 \_ 版本**                                          |                                                                                                                                                                                                                                 |
| **SPLREG \_ NET \_ 快顯視窗**                                              | Windows Server 2003 和更新版本中不支援<br/>                                                                                                                                                                       |
| **SPLREG \_ NET \_ POPUP \_ 至 \_ 電腦**                                | 在成功傳回時，如果工作通知應該傳送至用戶端電腦， *.pdata* 會包含 1; 如果要將工作通知傳送給使用者，則為0。<br/> Windows Server 2003 和更新版本中不支援<br/> |
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
| **SPLREG \_ 重試 \_ 快顯視窗**                                            | 在成功傳回時，如果伺服器設定為所有作業的 [重試] 快顯視窗， *.pdata* 會包含 1; 如果伺服器不會針對所有作業重試快顯視窗，則為0。<br/> Windows Server 2003 和更新版本中不支援<br/> |
| **SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序**                             |                                                                                                                                                                                                                                 |
| **SPLREG 排程器 \_ \_ 執行緒 \_ 優先順序 \_ 預設值**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows伺服器2003和更新版本<br/>                                                                                                                                                                                        |



 

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



 

如果 *pKeyName* 是其中一個預先定義的目錄服務 (DS) 金鑰 (請參閱 [**SetPrinter**](setprinter.md)) 和 *pValueName* 包含逗號 ( '，' ) ，則逗號之前的 *pValueName* 部分是值名稱，而逗號右邊的 *pValueName* 部分是 DS 屬性 OID。 會建立名為 OID 的子機碼，並在 OID 索引鍵底下輸入值名稱和 OID 所組成的新值。 [**SetPrinterDataEx**](setprinterdataex.md) 也會在 DS 機碼下新增值名稱和資料。

在 Windows 7 和更新版本的 Windows 中，傳送至列印伺服器的列印工作預設會在用戶端上呈現。 您可以將 *pKeyName* 設定為 "PrinterDriverData"，並 *pValueName* 至下表中的設定值，以讀取印表機的用戶端轉譯設定。



| 設定                      | 資料類型      | 描述                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | 值為0，或如果此值不存在於登錄中，則會啟用列印工作的預設用戶端轉譯。<br/> 值為1時，會停用列印工作的用戶端轉譯。<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | 值為0，或如果此值不存在於登錄中，則會在用戶端上呈現列印工作。 如果無法在用戶端上呈現列印工作，則會在伺服器上轉譯。 如果無法在伺服器上轉譯列印工作，它將會失敗。<br/> 值為1時，會在用戶端上呈現列印工作。 如果無法在用戶端上呈現列印工作，則會失敗。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetPrinterDataExW** (Unicode) 和 **GetPrinterDataExA** (ANSI) <br/>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 


---
description: GetPrinter 函式會捕獲指定印表機的相關資訊。
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: 'GetPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: b6823795ea715ac72dfdb7150dac08fd7feb34445fcfab94412cb2dd0c6bd7a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949087"
---
# <a name="getprinter-function"></a>GetPrinter 函式

**GetPrinter** 函式會捕獲指定印表機的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

函式用來抓取資訊之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

函數儲存在 *pPrinter* 所指向之緩衝區中的結構層級或類型。

此值可以是1、2、3、4、5、6、7、8或9。

</dd> <dt>

*pPrinter* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收包含指定印表機相關資訊的結構。 緩衝區必須夠大，才能接收結構以及結構成員指向的任何字串或其他資料。 如果緩衝區太小， *pcbNeeded* 參數會傳回所需的緩衝區大小。

結構的類型取決於 *層級* 的值。



| 層級                                                                                                | 結構                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 包含一般印表機資訊的 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md) 結構。<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構，內含印表機的詳細資訊。<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**印表機 \_ 資訊 \_ 3**](printer-info-3.md)結構，內含印表機的安全性資訊。<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**印表機 \_ 資訊 \_ 4**](printer-info-4.md)結構，其中包含最少量的印表機資訊，包括印表機的名稱、伺服器的名稱，以及印表機是否為遠端或本機。<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**印表機 \_ 資訊 \_ 5**](printer-info-5.md)結構，包含印表機屬性和超時設定等印表機資訊。<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**印表機 \_ 資訊 \_ 6**](printer-info-6.md)結構，指定印表機的狀態值。<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | [**印表機 \_ 資訊 \_ 7**](printer-info-7.md)結構，指出是否在目錄服務中發佈印表機。<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**印表機 \_ 資訊 \_ 8**](printer-info-8.md)結構，指定全域預設印表機設定。<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構，指定每個使用者的預設印表機設定。<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PPrinter* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此函式會將其設定為印表機資訊的大小（以位元組為單位）。 如果 *cbBuf* 小於此值，則 **GetPrinter** 會失敗，而值代表所需的緩衝區大小。 如果 *cbBuf* 等於或大於此值， **GetPrinter** 會成功，而值代表緩衝區中儲存的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)、[**印表機 \_ 資訊 \_ 8**](printer-info-8.md)和 [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構中的 **pDevMode** 成員可以是 **Null**。 發生這種情況時，印表機會無法使用，直到重新安裝驅動程式為止。

針對包含安全描述項指標的 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 和 [**印表機 \_ 資訊 \_ 3**](printer-info-3.md) 結構，此函式只會抓取呼叫端有權讀取之安全描述項的元件。 若要取得特定的安全描述項元件，您必須在呼叫 [**OpenPrinter**](openprinter.md) 函式來取得印表機的控制碼時，指定必要的存取權限。 下表顯示讀取各種安全描述項元件所需的存取權限。



| 存取權限                        | 安全描述項元件                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 讀取 \_ 控制<br/>            | 擁有者<br/> 主要群組<br/> 任意存取控制清單 (DACL) <br/> |
| 存取 \_ 系統 \_ 安全性<br/> | 系統存取控制清單 (SACL) <br/>                                                  |



 

如果您指定層級7，則 [**印表機 \_ 資訊 \_ 7**](printer-info-7.md)的 **dwAction** 成員會傳回下列其中一個值，指出是否在目錄服務中發佈印表機。



| dwAction 值     | 意義                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPRINT \_ 發行   | 印表機已發佈。 **PszObjectGUID** 成員包含與印表機相關聯之目錄服務列印佇列物件的 GUID。                                                                                                       |
| DSPRINT \_ 取消發佈 | 未發佈印表機。                                                                                                                                                                                                                            |
| DSPRINT \_ 暫止   | 指出系統正在嘗試完成發行或取消發行作業。 如果 [**SetPrinter**](setprinter.md) 呼叫無法發行或取消發行印表機，系統會進一步嘗試在背景中完成此作業。 |



 

從 Windows Vista 開始，當 *hPrinter* 參考列印伺服器所裝載的印表機，而且至少有一個開啟的列印伺服器連線時，就會從本機快取中取出 **GetPrinter** 傳回的印表機資料。 在所有其他設定中，會從列印伺服器查詢印表機資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetPrinterW** (Unicode) 和 **GetPrinterA** (ANSI) <br/>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AbortPrinter**](abortprinter.md)
</dt> <dt>

[**Interactivesession.addprinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**>enumprinters**](enumprinters.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 1**](printer-info-1.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 5**](printer-info-5.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 7**](printer-info-7.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 8**](printer-info-8.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 





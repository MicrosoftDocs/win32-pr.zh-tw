---
description: '>enumprinters 函式會列舉可用的印表機、列印伺服器、網域或列印提供者。'
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: '>enumprinters 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fb88cef081010f1319fb194904933ba2366d6593f0d2517c696bb6d6490ace20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353838"
---
# <a name="enumprinters-function"></a>>enumprinters 函式

**>Enumprinters** 函式會列舉可用的印表機、列印伺服器、網域或列印提供者。

## <a name="syntax"></a>語法


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

函數應該列舉的列印物件類型。 這個值可以是下列一或多個值。



| 值                                                                                                                                                                                               | 意義                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**印表機 \_ 列舉 \_ 區域**</dt> </dl>                       | 如果 \_ \_ 未同時傳遞印表機列舉名稱旗標，此函式會忽略 *NAME* 參數，並列舉本機安裝的印表機。 如果 \_ \_ 也傳遞印表機列舉名稱，此函式會列舉本機印表機的 *名稱*。 <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**印表機 \_ 列舉 \_ 名稱**</dt> </dl>                          | 函數會列舉依 *名稱* 識別的印表機。 這可以是伺服器、網域或列印提供者。 如果 *Name* 為 **Null**，則函式會列舉可用的列印提供者。<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**印表機 \_ 列舉 \_ 共用**</dt> </dl>                    | 此函數會列舉具有共用屬性的印表機。 無法在隔離中使用;使用或作業來結合另一個印表機 \_ 列舉型別。<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**印表機 \_ 列舉 \_ 連接**</dt> </dl>     | 此函式會列舉使用者對其進行先前連接的印表機清單。<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**印表機 \_ 列舉 \_ 網路**</dt> </dl>                 | 此函數會列舉電腦網域中的網路印表機。 只有當 *層級* 為1時，此值才有效。<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**印表機 \_ 列舉 \_ 遠端**</dt> </dl>                    | 此函數會列舉電腦網域中的網路印表機和列印伺服器。 只有當 *層級* 為1時，此值才有效。<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**印表機 \_ 列舉 \_ 類別 \_ 3d**</dt> </dl>    | 此函數只會列舉3D 印表機。<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**印表機 \_ 列舉 \_ 類別目錄 \_**</dt> </dl> | 此函數會列舉所有列印裝置，包括3D 印表機。<br/>                                                                                                                                                                           |



 

如果 *層級* 為4，您只能使用印表機 \_ 列舉 \_ 連接和印表機 \_ 列舉 \_ 本機常數。

> [!Note]  
> 預設不會列舉3D 列印裝置。 您必須同時包含 **印表機 \_ 列舉 \_ 類別 \_ 3d** 和 **印表機 \_ 列舉 \_ 區域** ，才能列舉3d 印表機。 若要包含3D 印表機以及所有其他本機印表機，請使用 [ **印表機 \_ 列舉 \_ 類別 \_** ] 和 [ **印表機 \_ 列舉 \_ 本機**]。

 

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

如果 *層級* 為1， *旗標* 就會包含印表機 \_ 列舉 \_ 名稱，而 *名稱* 為非 **null**，則 *name* 是以 null 結束的字串指標，可指定要列舉的物件名稱。 這個字串可以是伺服器、網域或列印提供者的名稱。

如果 *層級* 為1， *旗標* 就會包含印表機 \_ 列舉 \_ 名稱，而 *名稱* 是 **Null**，則函式會列舉可用的列印提供者。

如果 *層級* 為1， *旗標* 就會包含印表機 \_ ENUM \_ REMOTE，而 *Name* 是 **Null**，則函式會列舉使用者網域中的印表機。

如果 *層級* 為2或5，則 *名稱* 是以 null 結束的字串指標，可指定要列舉其印表機的伺服器名稱。 如果此字串為 **Null**，則此函式會列舉本機電腦上安裝的印表機。

如果 *層級* 為4，則 *名稱* 應該是 **Null**。 函數一律會在本機電腦上進行查詢。

當 *名稱* 為 **Null** 時，將 *旗標* 設定為印表機 \_ 列舉 \_ 本機 \| 印表機 \_ 列舉 \_ 連接會列舉安裝在本機電腦上的印表機。 這些印表機包括實際連接到本機電腦的印表機，以及具有網路連線的遠端印表機。

當 *Name* 不是 **Null** 時，將 *旗標* 設定為印表機 \_ 列舉 \_ 本機 \| 印表機 \_ 列舉 \_ 名稱會列舉安裝在伺服器 *名稱* 上的本機印表機。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PPrinterEnum* 所指向的資料結構類型。 有效的值為1、2、4和5，其對應于 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md)、 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 、 [**印表機 \_ 資訊 \_ 4**](printer-info-4.md)和 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md) 資料結構。

此值可以是1、2、4或5。

</dd> <dt>

*pPrinterEnum* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md)、 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)、 [**印表機 \_ 資訊 \_ 4**](printer-info-4.md)或 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md) 結構的陣列。 每個結構都包含描述可用列印物件的資料。

如果 *層級* 為1，則陣列包含 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md) 結構。 如果 *層級* 為2，則陣列會包含 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 結構。 如果 *層級* 為4，則陣列包含 [**印表機 \_ 資訊 \_ 4**](printer-info-4.md) 結構。 如果 *層級* 為5，則陣列包含 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md) 結構。

緩衝區必須夠大，才能接收資料結構的陣列，以及結構成員指向的任何字串或其他資料。 如果緩衝區太小， *pcbNeeded* 參數會傳回所需的緩衝區大小。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PPrinterEnum* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

值的指標，如果函式成功則為，如果 *cbBuf* 太小，則會收到所需的位元組數目，以接收復制的位元組數目。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

值的指標，此值會接收在 *pPrinterEnum* 點的陣列中，此函式所傳回的 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md)、[**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 、[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)或 [**印表機 \_ 資訊 \_ 5**](printer-info-5.md)結構的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

如果 **>enumprinters** 傳回印表機列舉容器所指定的 [**印表機 \_ 資訊 \_ 1**](printer-info-1.md) 結構 \_ \_ ，則表示有印表機物件的階層。 應用程式可以再次呼叫 **>enumprinters** 來列舉階層，並將 *名稱* 設定為 **印表機 \_ 資訊 \_ 1** 結構的 **pName** 成員的值。

**>Enumprinters** 函數不會取得安全性資訊。 如果 *pPrinterEnum* 所指向的陣列中傳回 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構，其 *pSecurityDescriptor* 成員將會設定為 **Null**。

若要取得預設印表機的相關資訊，請呼叫 [**GetDefaultPrinter**](getdefaultprinter.md)。

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)結構提供簡單且極快速的方式來抓取本機電腦上安裝的印表機名稱，以及使用者已建立的遠端連線。 使用 **印表機 \_ 資訊 \_ 4** 資料結構呼叫 **>enumprinters** 時，該函式會查詢登錄中的指定資訊，然後立即傳回。 這與其他層級的 **印表機 \_ 資訊 \_ \* *_ 資料結構一起呼叫時，與 >enumprinters 的行為不同。尤其是當*** 使用層級 2 ([**印表機 \_ 資訊 \_ 2**](printer-info-2.md)) 資料結構來呼叫 _ >enumprinters 時，它會在每個遠端連線上執行 [**OpenPrinter**](openprinter.md)呼叫。 如果遠端連線已關閉，或遠端伺服器已不存在，或遠端印表機已不存在，則函式必須等待 RPC 超時，進而使 **OpenPrinter** 呼叫失敗。 這可能需要一段時間。 傳遞 **印表機 \_ 資訊 \_ 4** 結構，可讓應用程式取出最少的必要資訊; 如果需要更詳細的資訊，則可以進行後續的 **>enumprinters** 層級2呼叫。

**Windows Vista：** 當 *層級* 的值為4時，會從本機快取中取出 **>enumprinters** 傳回的印表機資料。

下表顯示當 *Level* 參數設定為1時，各種 *旗標* 值的 **>enumprinters** 輸出。

在資料表的 [ *名稱* 參數] 欄中，您應該以適當的名稱取代列印提供者、網域和電腦。 例如，針對「列印提供者」，您可以使用網路列印提供者的名稱或本機列印提供者的名稱。 若要取出列印提供者名稱，請呼叫 *名稱* 設為 **Null** 的 **>enumprinters** 。



| *旗標* 參數                                  | *Name* 參數                            | 結果                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| 印表機 \_ 列舉 \_ 本機 (而非印表機 \_ 列舉 \_ 名稱)  | *Name* 參數會被忽略。<br/> | 所有本機印表機。<br/>                                                                    |
| 印表機 \_ 列舉 \_ 名稱                                | 「列印提供者」<br/>                 | 所有功能變數名稱<br/>                                                                       |
| 印表機 \_ 列舉 \_ 名稱                                | 「列印提供者！局域<br/>          | 電腦網域中的所有印表機和列印伺服器<br/>                                |
| 印表機 \_ 列舉 \_ 名稱                                | 「列印提供者！ \\ \\設備<br/>    | 電腦上共用的所有印表機 \\ \\<br/>                                                     |
| 印表機 \_ 列舉 \_ 名稱                                | 空字串 ""<br/>              | 所有本機印表機。<br/>                                                                    |
| 印表機 \_ 列舉 \_ 名稱                                | **NULL**<br/>                         | 電腦網域中的所有列印提供者<br/>                                           |
| 印表機 \_ 列舉 \_ 連接                         | *Name* 參數會被忽略。<br/> | 所有連線的遠端印表機<br/>                                                          |
| 印表機 \_ 列舉 \_ 網路                             | *Name* 參數會被忽略。<br/> | 電腦網域中的所有印表機<br/>                                                  |
| 印表機 \_ 列舉 \_ 遠端                              | 空字串 ""<br/>              | 電腦網域中的所有印表機和列印伺服器<br/>                                |
| 印表機 \_ 列舉 \_ 遠端                              | 「列印提供者」<br/>                 | 與印表機 \_ 列舉 \_ 名稱相同<br/>                                                            |
| 印表機 \_ 列舉 \_ 遠端                              | 「列印提供者！局域<br/>          | 電腦網域中的所有印表機和列印伺服器，不論指定的 *網域* 為何。<br/> |
| 印表機 \_ 列舉 \_ 類別 \_ 3d                        | *Name* 參數會被忽略。<br/> | 只會列舉3D 印表機。<br/>                                                       |
| 印表機 \_ 列舉 \_ 類別目錄 \_                       | *Name* 參數會被忽略。<br/> | 系統會列舉3D 印表機以及所有其他印表機。<br/>                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumPrintersW** (Unicode) 和 **EnumPrintersA** (ANSI) <br/>                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Interactivesession.addprinter**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 1**](printer-info-1.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 


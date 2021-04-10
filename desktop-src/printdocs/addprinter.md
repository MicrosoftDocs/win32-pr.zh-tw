---
description: Interactivesession.addprinter 函式會將印表機新增至指定伺服器支援的印表機清單。
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: 'Interactivesession.addprinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192610"
---
# <a name="addprinter-function"></a>Interactivesession.addprinter 函式

**Interactivesession.addprinter** 函式會將印表機新增至指定伺服器支援的印表機清單。

## <a name="syntax"></a>語法


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定應該安裝印表機之伺服器的名稱。 如果這個字串為 **Null**，則印表機會安裝在本機。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PPrinter* 所指向的結構版本。 此值必須是2。

</dd> <dt>

*pPrinter* \[在\]
</dt> <dd>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的指標，其中包含印表機的相關資訊。 在呼叫 **interactivesession.addprinter** 之前，您必須為此結構的 **pPrinterName**、 **pPortName**、 **pDriverName** 和 **pPrintProcessor** 成員指定非 **Null** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是控制碼 (不會) 至新的印表機物件的執行緒安全。 當您完成控制碼時，請將它傳遞至 [**ClosePrinter**](closeprinter.md) 函式來關閉它。

如果函式失敗，則傳回值為 **Null**。

## <a name="remarks"></a>備註

請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。

傳回的控制碼不是安全線程。 如果呼叫端需要在多個執行緒上同時使用它，則必須使用 [同步](/windows/desktop/Sync/synchronization-functions)處理函式提供對印表機控制碼的自訂同步存取。 為了避免撰寫自訂程式碼，應用程式可以視需要開啟每個執行緒上的印表機控制碼。

以下是在呼叫 **interactivesession.addprinter** 函式之前可以設定的 [**印表機 \_ INFO \_ 2**](printer-info-2.md)結構的成員：

-   **屬性**
-   **pPrintProcessor**
-   **DefaultPriority**
-   **優先順序**
-   **pComment**
-   **pSecurityDescriptor**
-   **pDatatype**
-   **pSepFile**
-   **pDevMode**
-   **pShareName**
-   **pLocation**
-   **StartTime**
-   **pParameters**
-   **UntilTime**

[**印表機 \_ INFO \_ 2**](printer-info-2.md)結構的 **Status**、 **CJobs** 和 **AveragePPM** 成員是保留供 [**GetPrinter**](getprinter.md)函式使用。 它們必須在呼叫 **interactivesession.addprinter** 之前設定。

如果 **pSecurityDescriptor** 為 **Null**，系統會將預設安全描述項指派給印表機。 預設安全描述項具有下列許可權。



| 值                          | 描述                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 系統管理員與進階使用者 | 完整控制列印佇列。 這表示這些群組的成員可以列印、管理佇列 (可以刪除佇列、變更佇列的任何設定，包括安全描述項) ，以及管理所有使用者的列印工作 (刪除、暫停、繼續、重新開機作業) 。請注意，Windows XP Professional 之前不存在 Power 使用者。<br/> |
| 建立者/擁有者                  | 可以管理自己的作業。 這表示提交工作的使用者可以管理 (刪除、暫停、繼續、重新開機) 自己的作業。                                                                                                                                                                                                                                  |
| 所有人                       | Execute 和 standard read control。 這表示 everyone 群組的成員可以列印和讀取列印佇列的屬性。                                                                                                                                                                                                                     |



 

應用程式使用 **interactivesession.addprinter** 函式建立印表機物件之後，必須使用 [**PrinterProperties**](printerproperties.md) 函式來指定與印表機物件相關聯之印表機驅動程式的正確設定。

如果已經存在具有相同名稱的印表機物件， **interactivesession.addprinter** 函式會傳回錯誤，除非該物件標示為待刪除。 在此情況下，不會刪除現有的印表機，而且會使用 **interactivesession.addprinter** 建立參數來變更現有印表機設定 (如同應用程式已使用 [**SetPrinter**](setprinter.md) 函式) 。

您可以使用 [**EnumPrintProcessors**](enumprintprocessors.md) 函式來列舉安裝在伺服器上的列印處理器組。 您可以使用 [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) 函式來列舉列印處理器所支援的一組資料類型。 使用 [**EnumPorts**](enumports.md) 函式來列舉可用的埠集合。 使用 [**EnumPrinterDrivers**](enumprinterdrivers.md) 函式來列舉已安裝的印表機驅動程式。

**Interactivesession.addprinter** 函式的呼叫端必須具有伺服器 \_ 存取權 \_ ，才能管理要在其上建立印表機的伺服器。 此函式所傳回的控制碼會有 [印表機 \_ 所有 \_ 存取權限]，可用來執行印表機的系統管理操作。

如果傳遞了 **DrvPrinterEvent** 函式的印表機 \_ 事件 \_ 旗標 \_ 沒有 \_ ui 旗標，則驅動程式不應在 **DrvPrinterEvent** 期間使用 ui 呼叫。 若要執行 UI 相關的工作，安裝程式應該使用印表機的 .inf 檔案中的 **VendorSetup** 專案，或針對隨插即用的裝置，安裝程式可以使用裝置特定的共同安裝程式。 如需有關 **VendorSetup** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) 。

網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是當您執行 **interactivesession.addprinter** 時，會啟用檔案和列印共用的例外狀況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddPrinterW** (Unicode) 和 **AddPrinterA** (ANSI) <br/>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**PrinterProperties**](printerproperties.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 


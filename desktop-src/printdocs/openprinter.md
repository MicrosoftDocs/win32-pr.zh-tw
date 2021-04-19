---
description: OpenPrinter 函式會抓取指定之印表機或列印伺服器或列印子系統中其他類型之控制碼的控制碼。
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: 'OpenPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969386"
---
# <a name="openprinter-function"></a>OpenPrinter 函式

**OpenPrinter** 函式會抓取指定之印表機或列印伺服器或列印子系統中其他類型之控制碼的控制碼。

## <a name="syntax"></a>語法


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPrinterName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定印表機或列印伺服器的名稱、印表機物件、XcvMonitor 或 XcvPort。

若為印表機物件，請使用： PrinterName、Job xxxx。 若為 XcvMonitor，請使用： ServerName，XcvMonitor MonitorName。 若為 XcvPort，請使用： ServerName，XcvPort PortName。

如果是 **Null**，則表示本機印表機伺服器。

</dd> <dt>

*phPrinter* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收控制碼 (不會) 開啟的印表機或列印伺服器物件的安全線程。

*PhPrinter* 參數可以傳回 Xcv 控制碼，以搭配 XcvData 函式使用。 如需 XcvData 的詳細資訊，請參閱 DDK。

</dd> <dt>

*pDefault* \[在\]
</dt> <dd>

[**印表機 \_ 預設**](printer-defaults.md)結構的指標。 這個值可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。

> [!Note]  
> 針對遠端印表機的 **OpenPrinter** 呼叫所取得的控制碼，會透過「列印多工緩衝處理器」服務的本機快取來存取印表機。 此快取不是即時精確。 若要取得準確的資料，請將 OpenPrinter 呼叫取代為 [**OpenPrinter2**](openprinter2.md) ，並將 pOptions 設定為印表機 \_ 選項 \_ NO \_ CACHE。 請注意，只有 OpenPrinter2W 可正常運作。 函數會傳回使用其他列印 API 呼叫的印表機控制碼，並略過本機快取。 這個方法會在等候與遠端印表機的網路通訊時封鎖，所以它可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

> [!Note]  
> 針對遠端印表機呼叫 **OpenPrinter** 所取得的控制碼，將會透過列印多工緩衝處理器服務中的本機快取來存取印表機。 這種快取的設計並不是即時精確。 如果您需要取得精確的資料，請將 **OpenPrinter** 呼叫取代為 [**OpenPrinter2**](openprinter2.md) ，並將 *pOptions* 設定為 [**印表機 \_ 選項 \_ NO \_ CACHE**](printer-options.md)。 請注意，只有 **OpenPrinter2W** 可正常運作。 如此一來，函式就會傳回印表機控制碼，讓其他的列印 API 呼叫略過本機快取。 請注意，這種方法會在等候遠端印表機的往返網路通訊時封鎖，所以它可能不會立即傳回。 此函式傳回的速度取決於執行時間因素，例如網路狀態、列印伺服器設定，以及印表機驅動程式的執行因素。撰寫應用程式時，難以預測的因素。 因此，從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

*PhPrinter* 所指向的控制碼不是安全線程。 如果呼叫端需要在多個執行緒上同時使用它，則必須使用 [同步](/windows/desktop/Sync/synchronization-functions)處理函式提供對印表機控制碼的自訂同步存取。 為了避免撰寫自訂程式碼，應用程式可以視需要開啟每個執行緒上的印表機控制碼。

*PDefault* 參數可讓您指定用來列印 [**StartDocPrinter**](startdocprinter.md)函數所提交檔的資料類型和裝置模式值。 不過，您可以在檔啟動後使用 [**SetJob**](setjob.md) 函式來覆寫這些值。

當在 [**StartDocPrinter**](startdocprinter.md)呼叫的 *pDocInfo* 參數中傳遞的 [**DOC \_ INFO \_ 1**](doc-info-1.md)結構的 *pDatatype* 成員值為 "RAW" 時，不會使用 *PDefault* 參數的 [**印表機 \_ 預設**](printer-defaults.md)值結構中所定義的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)設定。 當高階檔 (例如 Adobe PDF 或 Microsoft Word 檔案) 或其他印表機資料 (這類 PCL、PS 或 HPGL) 直接傳送至 *pDatatype* 設定為「原始」的印表機時，檔必須完整地以硬體理解的語言描述 **DEVMODE** 樣式的列印工作設定。

您可以呼叫 **OpenPrinter** 函數來開啟列印伺服器的控制碼，或判斷用戶端對列印伺服器的存取權限。 若要這樣做，請在 *pPrinterName* 參數中指定列印伺服器的名稱，將 [**印表機 \_ 預設**](printer-defaults.md)結構的 **PDatatype** 和 **PDevMode** 成員設為 **Null**，並設定 **DesiredAccess** 成員以指定伺服器存取遮罩值，例如 [伺服器 \_ 所有存取] \_ 。 當您完成控制碼時，請將它傳遞至 [**ClosePrinter**](closeprinter.md) 函式來關閉它。

使用 [**印表機 \_ 預設**](printer-defaults.md)結構的 **DesiredAccess** 成員，指定印表機所需的存取權限。 存取權限可以是下列其中一項。  (如果 *pDefault* 為 **Null**，則存取權限會是印表機 \_ 存取 \_ 使用。 ) 



| 所需的存取值                        | 意義                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 印表機 \_ 存取 \_ 管理                 | 執行管理工作，例如 [**SetPrinter**](setprinter.md)所提供的工作。                                                                                                 |
| 印表機 \_ 存取 \_ 使用                        | 執行基本列印工作。                                                                                                                                                        |
| 印表機 \_ 所有 \_ 存取                        | 若要執行所有管理工作和基本列印工作，除了同步處理 (請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。                                     |
| 印表機 \_ 存取 \_ 管理 \_ 受限            | 執行管理工作，例如 [**SetPrinter**](setprinter.md) 和 [**SetPrinterData**](setprinterdata.md)所提供的工作。 從 Windows 8.1 開始，可以使用這個值。 |
| 一般安全性值，例如寫入 \_ DAC | 允許特定的控制存取權限。 請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。                                                                                      |



 

如果使用者沒有許可權可使用所需的存取權開啟指定的印表機或列印伺服器，則 **OpenPrinter** 呼叫會失敗，並傳回值為零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回值 \_ 拒絕存取的值 \_ 。

## <a name="examples"></a>範例

如需使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **OpenPrinterW** (Unicode) 和 **OpenPrinterA** (ANSI) <br/>                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**印表機 \_ 預設值**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 


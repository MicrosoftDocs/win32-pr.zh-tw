---
description: 在設定部分印表機選項時，抓取列印子系統中指定之印表機、列印伺服器或其他類型之控制碼的控制碼。
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: 'OpenPrinter2 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849752"
---
# <a name="openprinter2-function"></a>OpenPrinter2 函式

在設定部分印表機選項時，抓取列印子系統中指定之印表機、列印伺服器或其他類型之控制碼的控制碼。

## <a name="syntax"></a>語法


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPrinterName* \[在\]
</dt> <dd>

常數以 null 終止的字串指標，指定印表機或列印伺服器的名稱、印表機物件、XcvMonitor 或 XcvPort。

若為印表機物件，請使用： PrinterName、Job xxxx。 若為 XcvMonitor，請使用： ServerName，XcvMonitor MonitorName。 若為 XcvPort，請使用： ServerName，XcvPort PortName。

**Windows Vista：** 如果是 **Null**，則表示本機列印伺服器。

</dd> <dt>

*phPrinter* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收開啟的印表機或列印伺服器物件的控制碼。

</dd> <dt>

*pDefault* \[在\]
</dt> <dd>

[**印表機 \_ 預設**](printer-defaults.md)結構的指標。 這個值可以是 **Null**。

</dd> <dt>

*pOptions* \[在\]
</dt> <dd>

[**印表機 \_ 選項**](printer-options.md)結構的指標。 這個值可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。 如需擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

請勿在 [**DllMain**](/windows/desktop/Dlls/dllmain)中呼叫這個方法。

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

此函式的 ANSI 版本不會實作為函式，並傳回 \_ 不支援的錯誤 \_ 。

*PDefault* 參數可讓您指定用來列印 [**StartDocPrinter**](startdocprinter.md)函數所提交檔的資料類型和裝置模式值。 不過，您可以在檔啟動後使用 [**SetJob**](setjob.md) 函式來覆寫這些值。

您可以呼叫 **OpenPrinter2** 函數來開啟列印伺服器的控制碼，或判斷列印伺服器的用戶端存取許可權。 若要這樣做，請在 *pPrinterName* 參數中指定列印伺服器的名稱，將 [**印表機 \_ 預設**](printer-defaults.md)結構的 **PDatatype** 和 **PDevMode** 成員設為 **Null**，並設定 **DesiredAccess** 成員以指定伺服器存取遮罩值，例如 [伺服器 \_ 所有存取] \_ 。 當您完成控制碼時，請將它傳遞至 [**ClosePrinter**](closeprinter.md) 函式來關閉它。

使用 [**印表機 \_ 預設**](printer-defaults.md)結構的 **DesiredAccess** 成員來指定所需的存取權限。 存取權限可以是下列其中一項。



| 所需的存取值                        | 意義                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 印表機 \_ 存取 \_ 管理                 | 執行管理工作，例如 [**SetPrinter**](setprinter.md)所提供的工作。                                                                                                 |
| 印表機 \_ 存取 \_ 使用                        | 執行基本列印工作。                                                                                                                                                        |
| 印表機 \_ 所有 \_ 存取                        | 執行所有管理工作和基本列印工作（同步處理除外）。 請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。                                         |
| 印表機 \_ 存取 \_ 管理 \_ 受限            | 執行管理工作，例如 [**SetPrinter**](setprinter.md) 和 [**SetPrinterData**](setprinterdata.md)所提供的工作。 從 Windows 8.1 開始，可以使用這個值。 |
| 一般安全性值，例如寫入 \_ DAC | 允許特定的控制存取權限。 請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。                                                                                      |



 

如果使用者沒有許可權可使用所需的存取權開啟指定的印表機或列印伺服器，則 **OpenPrinter2** 呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回拒絕存取的值 \_ \_ 。

當 *pPrinterName* 是本機印表機時， **OpenPrinter2** 會忽略 [**印表機 \_ 選項**](printer-options.md)結構指向使用 *pOptions* 的所有 **dwFlags** 值，但印表機 \_ 選項 \_ 用戶端 \_ 變更除外。 如果傳遞後者，則 **OpenPrinter2** 會傳回 \_ 拒絕存取錯誤 \_ 。 因此，開啟本機印表機時， **OpenPrinter2** 不會比 [**OpenPrinter**](openprinter.md)更具優勢。

**Windows Vista：****OpenPrinter2** 傳回的印表機資料是從本機快取中取出，除非 *POptions* 所參考 [**印表機 \_ 選項**](printer-options.md)結構的 **dwFlags** 欄位中未設定 [**印表機] \_ \_ \_ 選項**。

## <a name="examples"></a>範例

在此範例中 ，當印表機 \_ 存取 \_ 管理 \_ 限制傳遞到 [**印表機 \_ 預設**](printer-defaults.md)結構，且使用者沒有適當的許可權時，OpenPrinter2 就會失敗。


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



如需示範如何使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **OpenPrinter2W** (Unicode) 和 **OpenPrinter2A** (ANSI) <br/>                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**印表機 \_ 預設值**](printer-defaults.md)
</dt> <dt>

[**印表機 \_ 選項**](printer-options.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 


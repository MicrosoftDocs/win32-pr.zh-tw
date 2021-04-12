---
description: FindFirstPrinterChangeNotification 函式會建立變更通知物件，並將控制碼傳回物件。 然後，您可以在呼叫其中一個等候函式時，使用這個控制碼來監視印表機或列印伺服器的變更。
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: 'FindFirstPrinterChangeNotification 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindFirstPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2da6a2ae73aa5b987ea3b8f8789f81ed0b4cdf06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192721"
---
# <a name="findfirstprinterchangenotification-function"></a>FindFirstPrinterChangeNotification 函式

**FindFirstPrinterChangeNotification** 函式會建立變更通知物件，並將控制碼傳回物件。 然後，您可以在呼叫其中一個等候函式時，使用這個控制碼來監視印表機或列印伺服器的變更。

**FindFirstPrinterChangeNotification** 呼叫會指定要監視的變更類型。 您可以指定一組條件來監視變更、一組要監視的印表機資訊欄位，或兩者。

當指定的印表機或列印伺服器發生其中一個指定的變更時，變更通知控制碼上的等候作業就會成功。 然後，您可以呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式來取得變更的相關資訊，以及重設變更通知物件，以便在下一次等候操作中使用。

## <a name="syntax"></a>語法


```C++
HANDLE FindFirstPrinterChangeNotification(
  _In_     HANDLE hPrinter,
           DWORD  fdwFilter,
           DWORD  fdwOptions,
  _In_opt_ LPVOID pPrinterNotifyOptions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

您要監視的印表機或列印伺服器的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*fdwFilter* 
</dt> <dd>

會導致變更通知物件進入信號狀態的條件。 當符合一或多個指定的條件時，就會發生變更通知。 如果 *pPrinterNotifyOptions* 為非 **Null**，則 *fdwFilter* 參數可以為零。

這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <dt>**印表機 \_ 變更 \_ 表單**</dt> </dl>                                   | 通知表單的任何變更。 您可以設定這個一般旗標或下列一或多個特定旗標：<br/> <dl> <dd>印表機 \_ 變更 \_ 新增 \_ 表單</dd> <dd>印表機 \_ 變更 \_ 集 \_ 表單</dd> <dd>印表機 \_ 變更 \_ 刪除 \_ 表單</dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <dt>**印表機 \_ 變更 \_ 作業**</dt> </dl>                                      | 通知作業的任何變更。 您可以設定這個一般旗標或下列一或多個特定旗標：<br/> <dl> <dd>印表機 \_ 變更 \_ 新增 \_ 作業</dd> <dd>印表機 \_ 變更 \_ 集 \_ 作業</dd> <dd>印表機 \_ 變更 \_ 刪除 \_ 作業</dd> <dd>印表機 \_ 變更 \_ 寫入 \_ 作業</dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <dt>**印表機 \_ 變更 \_ 埠**</dt> </dl>                                   | 通知埠的任何變更。 您可以設定這個一般旗標或下列一或多個特定旗標：<br/> <dl> <dd>印表機 \_ 變更 \_ 新增 \_ 埠</dd> <dd>印表機 \_ 變更 \_ 設定 \_ 埠 </dd> <dd>印表機 \_ 變更 \_ 刪除 \_ 埠</dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <dt>**印表機 \_ 變更 \_ 列印 \_ 處理器**</dt> </dl> | 對列印處理器進行任何變更的通知。 您可以設定這個一般旗標或下列一或多個特定旗標： <br/> <dl> <dd>印表機 \_ 變更 \_ 新增 \_ 列印 \_ 處理器 </dd> <dd>印表機 \_ 變更 \_ 刪除 \_ 列印 \_ 處理器</dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <dt>**印表機 \_ 變更 \_ 印表機**</dt> </dl>                          | 通知印表機的任何變更。 您可以設定這個一般旗標或下列一或多個特定旗標：<br/> <dl> <dd>印表機 \_ 變更 \_ 新增 \_ 印表機</dd> <dd>印表機 \_ 變更 \_ 集 \_ 印表機</dd> <dd>印表機 \_ 變更 \_ 刪除 \_ 印表機</dd> <dd>印表機 \_ 變更 \_ \_ 連接 \_ 印表機失敗</dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <dt>**印表機 \_ 變更 \_ 印表機 \_ 驅動程式**</dt> </dl>    | 通知印表機驅動程式的任何變更。 您可以設定這個一般旗標或下列一或多個特定旗標：<br/> <dl> <dd>印表機 \_ 變更 \_ 新增 \_ 印表機 \_ 驅動程式</dd> <dd>印表機 \_ 變更 \_ 集 \_ 印表機 \_ 驅動程式</dd> <dd>印表機 \_ 變更 \_ 刪除 \_ 印表機 \_ 驅動程式</dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <dt>**印表機 \_ \_ 全部變更**</dt> </dl>                                      | 如果發生上述任何變更，請通知。<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**印表機 \_ 變更 \_ 伺服器**</dt> </dl>                             | Windows 7：通知伺服器的任何變更。<br/> 此旗標不包含在藉由設定 **印表機 \_ \_ 全部變更** 值所監視的變更中。<br/>                                                                                                                                                                                                      |



 

如需上表中更明確旗標的說明，請參閱 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函數。

</dd> <dt>

*fdwOptions* 
</dt> <dd>

此旗標會決定可用於通知的印表機分類。



| 值                                                                                                                                                                                                                                                               | 意義                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <dt>**印表機 \_通知 \_ 類別 \_ 所有**</dt> <dt>0x001000</dt> </dl> | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 會傳回2D 和3d 印表機的通知。<br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <dt>**印表機 \_通知 \_ 類別 \_ 3d**</dt> <dt>0x002000</dt> </dl>    | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 只會傳回3d 印表機的通知。<br/>        |



 

當此旗標設定為零 (0) 時， **FindFirstPrinterChangeNotification** 將只適用于2d 印表機。 這是預設值。

</dd> <dt>

*pPrinterNotifyOptions* \[在中，選擇性\]
</dt> <dd>

[**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)結構的指標。 此結構的 **pTypes** 成員是一或多個 [**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md) 結構的陣列，每個都指定要監視的印表機資訊欄位。 當一或多個指定的欄位變更時，就會發生變更通知。 發生變更時， [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式可以取得新的印表機資訊。 如果 *fdwFilter* 為非零值，則此參數可以是 **Null** 。

如需可監視的欄位清單，請參閱 [**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是與指定的印表機或列印伺服器相關聯之變更通知物件的控制碼。

如果函式失敗，則傳回值是不正確 \_ 控制碼 \_ 值。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

若要監視印表機或列印伺服器，請呼叫 **FindFirstPrinterChangeNotification** 函式，然後在呼叫其中一個 [等候](/windows/desktop/Sync/wait-functions)函式時，使用傳回的變更通知物件控制碼。 變更通知物件進入已發出信號的狀態時，會滿足變更通知物件的等候作業。 當受監視的印表機或列印伺服器發生 *fdwFilter* 或 *pPrinterNotifyOptions* 所指定的一或多項變更時，系統會通知物件。

當您呼叫 **FindFirstPrinterChangeNotification** 時， *fdwFilter* 必須為非零值，否則 *pPrinterNotifyOptions* 必須是非 **Null**。 如果同時指定這兩者，則會對兩者進行通知。

當滿足印表機變更通知物件的等候操作時，請呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式來判斷通知的原因。 針對 *fdwFilter* 所指定的條件， **FindNextPrinterChangeNotification** 會報告已變更的條件或條件。 針對 *pPrinterNotifyOptions* 所指定的印表機資訊欄位， **FindNextPrinterChangeNotification** 會報告已變更的欄位，以及這些欄位的新資訊。 **FindNextPrinterChangeNotification** 也會將變更通知物件重設為未收到信號狀態，因此您可以在另一個等候作業中使用它來繼續監視印表機或列印伺服器。

有一個例外狀況，如果變更通知物件不是處於已發出信號的狀態，請勿呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函數。 如果 wait 函式傳回值等候 \_ 超時，則變更物件不會處於已發出信號的狀態。 只有在等候函式成功時才呼叫 **FindNextPrinterChangeNotification** 函式，而不會超時。當使用 \_ \_ \_ *PPRINTERNOTIFYOPTIONS* 參數中所設定的印表機通知選項重新整理位來呼叫 FindNextPrinterChangeNotification 時，就會發生例外狀況。

當您不再需要變更通知物件時，請呼叫 [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) 函式將其關閉。

**FindFirstPrinterChangeNotification** 的呼叫端必須確保傳入 **FindFirstPrinterChangeNotification** 的印表機控制碼會維持有效，直到呼叫 [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)為止。 如果印表機控制碼在印表機變更通知控制碼之前關閉，將無法傳遞進一步的通知。

**FindFirstPrinterChangeNotification** 不會將3d 印表機的變更通知傳送到伺服器控制碼。

> [!Note]  
> 在 Windows XP Service Pack 2 (SP2) 和更新版本中，網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是可以啟用檔案和列印共用的例外狀況。 如果使用者將印表機連線到另一部電腦，但未啟用例外狀況，則使用者將不會收到來自伺服器的印表機變更通知。 電腦系統管理員必須啟用例外狀況。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md)
</dt> </dl>

 


---
description: FindNextPrinterChangeNotification 函式會針對與印表機或列印伺服器相關聯的變更通知物件，抓取最新變更通知的相關資訊。
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: 'FindNextPrinterChangeNotification 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 37b05603a75f7bc8e68ead2d0dffdec2e99e7618e5461360760f2d9c89ae52da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112478"
---
# <a name="findnextprinterchangenotification-function"></a>FindNextPrinterChangeNotification 函式

**FindNextPrinterChangeNotification** 函式會針對與印表機或列印伺服器相關聯的變更通知物件，抓取最新變更通知的相關資訊。 當滿足變更通知物件的等候作業時，請呼叫此函式。

此函數也會將變更通知物件重設為未收到信號的狀態。 然後，您可以在另一個等候作業中使用此物件，以繼續監視印表機或列印伺服器。 作業系統會在下一次對印表機或列印伺服器進行一組指定的變更時，將物件設定為已發出信號的狀態。 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函式會建立變更通知物件，並指定要監視的變更集。

## <a name="syntax"></a>語法


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hChange* \[在\]
</dt> <dd>

與印表機或列印伺服器相關聯之變更通知物件的控制碼。 您可以藉由呼叫 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 函數來取得這類控制碼。 當偵測到物件的變更通知篩選器中所指定的其中一項變更時，作業系統會將此變更通知物件設定為已發出信號的狀態。

</dd> <dt>

*pdwChange* \[out、optional\]
</dt> <dd>

變數的指標，其位設定為表示造成最新通知的變更。 可能設定的位旗標，會對應至 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)呼叫的 *fdwFilter* 參數中指定的位旗標。 系統會設定下列一或多個位旗標。



| 值                                                                                                                                                                                                                                             | 意義                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**印表機 \_ 變更 \_ 新增 \_ 表單**</dt> </dl>                                                     | 已將表單新增至伺服器。<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**印表機 \_ 變更 \_ 新增 \_ 作業**</dt> </dl>                                                        | 列印工作已傳送至印表機。<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**印表機 \_ 變更 \_ 新增 \_ 埠**</dt> </dl>                                                     | 埠或監視器已新增至伺服器。<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**印表機 \_ 變更 \_ 新增 \_ 列印 \_ 處理器**</dt> </dl>                   | 列印處理器已新增至伺服器。<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**印表機 \_ 變更 \_ 新增 \_ 印表機**</dt> </dl>                                            | 印表機已新增至伺服器。<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**印表機 \_ 變更 \_ 新增 \_ 印表機 \_ 驅動程式**</dt> </dl>                      | 印表機驅動程式已新增至伺服器。<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**印表機 \_ 變更 \_ 設定 \_ 埠**</dt> </dl>                                   | 已在伺服器上設定埠。<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**印表機 \_ 變更 \_ 刪除 \_ 表單**</dt> </dl>                                            | 已從伺服器刪除表單。<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**印表機 \_ 變更 \_ 刪除 \_ 作業**</dt> </dl>                                               | 已刪除作業。<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**印表機 \_ 變更 \_ 刪除 \_ 埠**</dt> </dl>                                            | 埠或監視器已從伺服器刪除。<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**印表機 \_ 變更 \_ 刪除 \_ 列印 \_ 處理器**</dt> </dl>          | 已從伺服器刪除列印處理器。<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**印表機 \_ 變更 \_ 刪除 \_ 印表機**</dt> </dl>                                   | 已刪除印表機。<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**印表機 \_ 變更 \_ 刪除 \_ 印表機 \_ 驅動程式**</dt> </dl>             | 已從伺服器刪除印表機驅動程式。<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**印表機 \_ 變更 \_ \_ 連接 \_ 印表機失敗**</dt> </dl> | 印表機連接已失敗。<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**印表機 \_ 變更 \_ 集 \_ 表單**</dt> </dl>                                                     | 已在伺服器上設定表單。<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**印表機 \_ 變更 \_ 集 \_ 作業**</dt> </dl>                                                        | 已設定作業。<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**印表機 \_ 變更 \_ 集 \_ 印表機**</dt> </dl>                                            | 已設定印表機。<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**印表機 \_ 變更 \_ 集 \_ 印表機 \_ 驅動程式**</dt> </dl>                      | 已設定印表機驅動程式。<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**印表機 \_ 變更 \_ 寫入 \_ 作業**</dt> </dl>                                                  | 已寫入工作資料。<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**印表機 \_ 變更 \_ 超時**</dt> </dl>                                                         | 作業超時。<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**印表機 \_ 變更 \_ 伺服器**</dt> </dl>                                                            | Windows 7：伺服器發生變更。<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[在中，選擇性\]
</dt> <dd>

[**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)結構的指標。 將此結構的 **旗標** 成員設定為 [ **印表機 \_ 通知 \_ 選項 \_** 重新整理]，讓函式傳回所有受監視印表機資訊欄位的目前資料。 函數會忽略結構的所有其他成員。 此參數可以是 **Null**。

</dd> <dt>

*ppPrinterNotifyInfo* \[out、optional\]
</dt> <dd>

指標變數的指標，此變數會接收系統組態的唯讀緩衝區指標。 當您完成時，請呼叫 [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) 函式來釋放緩衝區。 如果不需要任何資訊，則此參數可以是 **Null** 。

緩衝區包含 [**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md) 結構，其中包含 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md) 結構的陣列。 陣列的每個元素都包含 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)呼叫的 *pPrinterNotifyOptions* 參數中所指定的其中一個欄位的相關資訊。 一般而言，此函數只會針對變更為的欄位提供資料，以導致最近的通知。 但是，如果 *pPrinterNotifyOptions* 參數所指向的結構指定了 **印表機 \_ 通知 \_ 選項 \_** 重新整理，則此函式會為所有受監視的欄位提供資料。

如果 [**印表機通知資訊結構的 \_ \_**](printer-notify-info.md) **旗標** 成員中設定了 [**印表機 \_ 通知資訊已 \_ \_ 捨棄** 位]，就會發生溢位或錯誤，而且通知可能已遺失。 在此情況下，在您進行第二個 **FindNextPrinterChangeNotification** 呼叫以指定 **印表機 \_ 通知 \_ 選項 \_** 重新整理之前，將不會傳送任何其他通知。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

滿足 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)所建立之通知物件的等候作業之後，請呼叫 **FindNextPrinterChangeNotification** 函數。 呼叫 **FindNextPrinterChangeNotification** 可讓您取得滿足等候作業之變更的相關資訊，並重設通知物件，以便在下一次發生變更時收到通知。

有一個例外狀況，如果變更通知物件不是處於已發出信號的狀態，請勿呼叫 **FindNextPrinterChangeNotification** 函數。 如果等候函式傳回值 **等候 \_ 超時**，則變更物件不會處於已發出信號的狀態。 只有在等候函式成功時才呼叫 **FindNextPrinterChangeNotification** 函式，而不會超時。當使用 *pPrinterNotifyOptions* 參數中所設定的 **印表機 \_ 通知 \_ 選項 \_** 重新整理位來呼叫 **FindNextPrinterChangeNotification** 時，就會發生例外狀況。 請注意，即使設定此旗標，仍可能在 *ppPrinterNotifyInfo* 參數中設定 [已 **\_ \_ \_ 捨棄印表機通知資訊**] 旗標。

若要繼續監視印表機或列印伺服器的變更，請重複呼叫其中一個 [wait](/windows/desktop/Sync/wait-functions) 函式的迴圈，然後呼叫 **FindNextPrinterChangeNotification** 函式來檢查變更並重設通知物件。

**FindNextPrinterChangeNotification** 可能會將相同印表機資訊欄位的多個變更合併成單一通知。 發生這種情況時，函式通常會將欄位的所有變更折迭為 *ppPrinterNotifyInfo* 中的 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)結構陣列中的單一專案; 單一專案只報告最新的資訊。 不過，對於某些作業和印表機資訊欄位，此函數可以針對相同的欄位傳回多個陣列專案。 在此情況下，欄位的最後一個陣列專案會報告目前的資料，而較舊的專案則包含中繼階段的資料。

當您不再需要變更通知物件時，請呼叫 [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) 函式將其關閉。

> [!Note]  
> 在 Windows XP Service Pack 2 (SP2) 和更新版本中，網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是可以啟用檔案和列印共用的例外狀況。 如果使用者將印表機連線到另一部電腦，但未啟用例外狀況，則使用者將不會收到來自伺服器的印表機變更通知。 電腦系統管理員必須啟用例外狀況。

 

## <a name="examples"></a>範例

下列程式碼範例說明如何使用這些功能來監視印表機狀態。


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)
</dt> </dl>

 


---
description: SetJob 函式會在指定的印表機上暫停、繼續、取消或重新開機列印工作。 您也可以使用 SetJob 函數來設定列印工作參數，例如列印工作優先順序和檔案名稱。
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: 'SetJob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9259429a7696e832bbbe6d0dd4bbb6fb46e7bce2bf7157122c10ca47656af346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060018"
---
# <a name="setjob-function"></a>SetJob 函式

**SetJob** 函式會在指定的印表機上暫停、繼續、取消或重新開機列印工作。 您也可以使用 **SetJob** 函數來設定列印工作參數，例如列印工作優先順序和檔案名稱。

您可以使用 **SetJob** 函式，將命令提供給列印工作，或設定列印工作參數，或在相同的呼叫中執行這兩個動作。 *Command* 參數的值不會影響函式使用 *Level* 和 *pJob* 參數的方式。 此外，您也可以搭配使用 **SetJob** 與 [**工作 \_ 資訊 \_ 3**](job-info-3.md) ，將一組列印工作連結在一起。 如需詳細資訊，請參閱「備註」。

## <a name="syntax"></a>語法


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

感興趣的印表機物件控制碼。 使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。

</dd> <dt>

*JobId* \[在\]
</dt> <dd>

指定列印工作的識別碼。 您可以藉由呼叫 [**system.printing.printqueue.addjob**](addjob.md) 函式或 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函數來取得列印工作識別碼。

如果 *Level* 參數設定為3，則 *JobId* 參數必須符合 *pJob* 所指向之 [**作業 \_ 資訊 \_ 3**](job-info-3.md)結構的 **jobid** 成員

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PJob* 參數所指向的作業資訊結構類型。

**所有版本的 Windows**：您可以將 *Level* 參數設定為0、1或2。 當您將 *層級* 設定為0時， *PJob* 應該是 **Null**。 當您未設定任何列印工作參數時，請使用這些值。

您也可以將 *Level* 參數設為3。

從 **Windows Vista** 開始：您也可以將 *Level* 參數設定為4。

</dd> <dt>

*pJob* \[在\]
</dt> <dd>

設定列印工作參數之結構的指標。

**所有版本的 Windows**： *pJob* 可指向 [**作業 \_ 資訊 \_ 1**](job-info-1.md)或 [**作業 \_ 資訊 \_ 2**](job-info-2.md)結構。

*pJob* 也可以指向 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構。 您必須擁有作業 **\_ 資訊 \_ 3** 結構的 **JobId** 和 **NextJobId** 成員所指定之作業的 **作業存取權 \_ \_ 管理** 存取權限。

從 **Windows Vista** 開始： *pJob* 也可以指向 [**工作 \_ 資訊 \_ 4**](job-info-4.md)結構。

如果 *Level* 參數為0，則 *PJob* 應該是 **Null**。

</dd> <dt>

*命令* \[在\]
</dt> <dd>

要執行的列印工作作業。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                            | 意義                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**作業 \_ 控制 \_ 取消**</dt> </dl>                                    | 請勿使用。 若要刪除列印工作，請使用 **工作 \_ 控制 \_ 刪除**。<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**作業 \_ 控制 \_ 暫停**</dt> </dl>                                       | 暫停列印工作。<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**作業 \_ 控制項 \_ 重新開機**</dt> </dl>                                 | 重新開機列印工作。 只有在列印時才能重新開機作業。<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**作業 \_ 控制 \_ 繼續**</dt> </dl>                                    | 繼續暫停的列印工作。<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**作業 \_ 控制 \_ 刪除**</dt> </dl>                                    | 刪除列印工作。<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**\_ \_ 傳送 \_ 至印表機的作業控制 \_**</dt> </dl>       | 由埠監視器用來結束列印工作。<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**工作 \_ 控制 \_ 最後一 \_ 頁已 \_ 退出**</dt> </dl> | 供語言監視器用來結束列印工作。<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**工作 \_ 控制 \_ 保留**</dt> </dl>                                    | **Windows Vista 和更新版本**：在列印後將工作保留在佇列中。<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**作業 \_ 控制 \_ 發行**</dt> </dl>                                 | **Windows Vista 和更新版本**：發行列印工作。<br/>                     |



 

您可以使用 **SetJob** 函數的相同呼叫來設定列印工作參數，以及提供命令給列印工作。 因此，如果您要設定列印工作參數， *命令* 就不需要是0，雖然它可以是。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

您可以使用 **SetJob** 函式來設定各種列印工作參數，方法是提供 [**工作 \_ 資訊 \_ 1**](job-info-1.md)、 [**作業 \_ 資訊 \_ 2**](job-info-2.md)、 [**作業 \_ 資訊 \_ 3**](job-info-3.md)的指標，或包含所需資料的 [**工作 \_ 資訊 \_ 4**](job-info-4.md) 結構。

若要移除或刪除特定印表機的所有列印工作，請呼叫 [**SetPrinter**](setprinter.md) 函式，並將其 *命令* 參數設定為 **印表機 \_ 控制項 \_ 清除**。

呼叫 **SetJob**： **JobId**、 **pPrinterName**、 **pMachineName**、 **pUserName**、 **pDrivername**、 **Size**、已 **提交**、 **Time** 和 **TotalPages** 時，會忽略 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、[**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**作業 \_ 資訊 \_ 4**](job-info-4.md)結構的下列成員。

您必須擁有印表機的 **印表機 \_ 存取權 \_ 管理** 存取權限，才能在列印佇列中變更列印工作的位置。

如果您不想要在列印佇列中設定列印工作的位置，則應該將 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、[**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**工作 \_ 資訊 \_ 4**](job-info-4.md)結構的 **位置** 成員設定為 **\_ \_ 未指定的工作位置**。

使用 **SetJob** 函式搭配 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構，將一組列印工作連結 (也稱為鏈) 。 當單一檔是由數個您想要個別轉譯的部分所組成時，這項功能就很有用。 若要依序列印 A、B、C 和 D 等作業，請使用 [**工作 \_ 資訊 \_ 4**](job-info-4.md)呼叫 **SetJob** ，將 A 連結至 b、b 至 C 和 c 到 D。

如果您連結列印工作，請注意下列事項：

-   作業可以新增至鏈的開頭或結尾。
-   鏈中的所有工作都必須具有相同的資料類型。
-   在幕後處理開始之前，必須完整連結鏈，否則，多工緩衝處理器可能會列印和刪除多工緩衝處理作業，然後才能將它們全部連結。 有兩種方式可以讓鏈保持不上列印：

    -   暫停鏈中的第一個工作，直到鏈完全連結為止。 第一個工作的暫停狀態會控制鏈中所有工作的狀態。
    -   讓第一個工作不完整，也就是不針對第一個作業呼叫 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 或 [**ScheduleJob**](schedulejob.md) 。 但是，如果已啟用 (預設) 的「在幕後列印時列印」，這個方法會在建立鏈時封鎖埠，這也會防止列印非相關的作業。

-   應用程式必須處理在鏈完成列印之前，使用者在鏈中刪除工作的情況。 當 JobID 不存在時， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)會傳回 **不正確 \_ 參數**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **SetJobW** (Unicode) 和 **SetJobA** (ANSI) <br/>                                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**System.printing.printqueue.addjob**](addjob.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 1**](job-info-1.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 2**](job-info-2.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 3**](job-info-3.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 4**](job-info-4.md)
</dt> </dl>

 


---
description: 「列印多工緩衝處理器」 API 包含應用程式用來管理 Windows 列印多工緩衝處理器的功能和資料結構，以及它所控制的印表機和列印工作。
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: 列印多工緩衝處理器 API 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df751b11206ebf26d2d0e8fd88f61ede8447dad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194849"
---
# <a name="print-spooler-api-functions"></a>列印多工緩衝處理器 API 函式

「列印多工緩衝處理器」 API 包含應用程式用來管理 Windows 列印多工緩衝處理器的功能和資料結構，以及它所控制的印表機和列印工作。

列印多工緩衝處理器 API 的功能分成下列群組：

-   [列印工作函式](#print-job-functions)
-   [印表機消費者介面功能](#printer-user-interface-functions)
-   [印表機功能](#printer-functions)
-   [印表機變更通知功能](#printer-change-notification-functions)
-   [印表機表單函式](#printer-form-functions)
-   [列印多工緩衝處理器函式](#print-spooler-api-functions)

## <a name="print-job-functions"></a>列印工作函式

這些函式會將列印工作傳送至印表機，並追蹤和控制列印多工緩衝處理器中的列印工作。



| 函式                                                                      | 描述                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**System.printing.printqueue.addjob**](addjob.md)<br/>                                           | [**System.printing.printqueue.addjob**](/windows/desktop/printdocs/addjob)函式會將列印工作加入至可由列印多工緩衝處理器排程的列印工作清單。 函數會抓取您可用來儲存作業的檔案名。 <br/>                                      |
| [**ClosePrinter**](closeprinter.md)<br/>                               | [**ClosePrinter**](/windows/desktop/printdocs/closeprinter)函式會關閉指定的印表機物件。 <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | [**DocumentEvent**](/windows/desktop/printdocs/documentevent)函數是與列印檔案相關聯之事件的事件處理常式。 <br/>                                                                                                                     |
| [**DocumentProperties**](documentproperties.md)<br/>                   | [**DocumentProperties**](/windows/desktop/printdocs/documentproperties)函式會抓取或修改印表機初始化資訊，或顯示指定印表機的印表機設定屬性工作表。 <br/>                                        |
| [**EndDocPrinter**](enddocprinter.md)<br/>                             | [**EndDocPrinter**](/windows/desktop/printdocs/enddocprinter)函式會結束指定之印表機的列印工作。 <br/>                                                                                                                                             |
| [**EndPagePrinter**](endpageprinter.md)<br/>                           | [**EndPagePrinter**](/windows/desktop/printdocs/endpageprinter)函式會通知列印多工緩衝處理器，應用程式是列印工作中頁面的結尾。 <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | [**EnumJobs**](/windows/desktop/printdocs/enumjobs)函式會抓取指定印表機的一組指定列印工作的相關資訊。 <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | [**GetJob**](/windows/desktop/printdocs/getjob)函式會抓取指定列印工作的相關資訊。 <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | [**OpenPrinter**](/windows/desktop/printdocs/openprinter)函式會抓取指定之印表機或列印伺服器或列印子系統中其他類型之控制碼的控制碼。 <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | 在設定部分印表機選項時，抓取列印子系統中指定之印表機、列印伺服器或其他類型之控制碼的控制碼。<br/>                                                                                      |
| [**ReportJobProcessingProgress**](reportjobprocessingprogress.md)<br/> | 向「列印多工緩衝處理器」服務回報 XPS 列印工作是否在幕後處理或轉譯階段，以及處理的哪個部分正在進行中。<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | [**ScheduleJob**](/windows/desktop/printdocs/schedulejob)函式要求列印多工緩衝處理器排程指定的列印工作來進行列印。 <br/>                                                                                                                |
| [**SetJob**](setjob.md)<br/>                                           | [**SetJob**](/windows/desktop/printdocs/setjob)函式會在指定的印表機上暫停、繼續、取消或重新開機列印工作。 您也可以使用 **SetJob** 函數來設定列印工作參數，例如列印工作優先順序和檔案名稱。 <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | [**StartDocPrinter**](/windows/desktop/printdocs/startdocprinter)函式會通知列印多工緩衝處理器，檔會進行多工緩衝處理以進行列印。 <br/>                                                                                                           |
| [**StartPagePrinter**](startpageprinter.md)<br/>                       | [**StartPagePrinter**](/windows/desktop/printdocs/startpageprinter)函式會通知多工緩衝處理器，頁面即將列印在指定的印表機上。 <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>印表機消費者介面功能

這些函式會顯示使用者介面，讓使用者可以選取或設定印表機。



| 函式                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedDocumentProperties**](advanceddocumentproperties.md)<br/> | [**AdvancedDocumentProperties**](/windows/desktop/printdocs/advanceddocumentproperties)函式會顯示指定印表機的 [印表機設定] 對話方塊，讓使用者可以設定該印表機。 <br/>                                                                                                                                                      |
| [**ConfigurePort**](configureport.md)<br/>                           | [**ConfigurePort**](/windows/desktop/printdocs/configureport)函式會顯示指定伺服器上端口的 [埠-設定] 對話方塊。 <br/>                                                                                                                                                                                                                     |
| [**ConnectToPrinterDlg**](connecttoprinterdlg.md)<br/>               | [**ConnectToPrinterDlg**](/windows/desktop/printdocs/connecttoprinterdlg)函式會顯示一個對話方塊，讓使用者流覽並聯機到網路上的印表機。 如果使用者選取印表機，此函式會嘗試建立與它的連接;如果伺服器上未安裝適當的驅動程式，則會提供使用者在本機建立印表機的選項。 <br/> |
| [**PrinterProperties**](printerproperties.md)<br/>                   | [**PrinterProperties**](/windows/desktop/printdocs/printerproperties)函式會顯示指定印表機的印表機屬性屬性工作表。 <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>印表機功能

這些函式會新增及設定列印多工緩衝處理器所使用的印表機。



| 函式                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPrinter**](abortprinter.md)<br/>                       | 如果印表機設定為可進行幕後處理， [**AbortPrinter**](/windows/desktop/printdocs/abortprinter) 函式會刪除印表機的多工緩衝處理檔案。 <br/>                                                                                                                                                                                                                                                                  |
| [**Interactivesession.addprinter**](addprinter.md)<br/>                           | [**Interactivesession.addprinter**](/windows/desktop/printdocs/addprinter)函式會將印表機新增至指定伺服器支援的印表機清單。 <br/>                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection**](addprinterconnection.md)<br/>       | **AddPrinterConnection** 函式會將連接加入至指定的印表機，以供目前的使用者使用。 <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | 將連接新增至目前使用者的指定印表機，並指定連接詳細資料。<br/>                                                                                                                                                                                                                                                                                             |
| [**DeletePrinter**](deleteprinter.md)<br/>                     | [**DeletePrinter**](/windows/desktop/printdocs/deleteprinter)函式會刪除指定的印表機物件。 <br/>                                                                                                                                                                                                                                                                                                    |
| [**DeletePrinterConnection**](deleteprinterconnection.md)<br/> | [**DeletePrinterConnection**](/windows/desktop/printdocs/deleteprinterconnection)函式會刪除 [**AddPrinterConnection**](addprinterconnection.md)或 [**ConnectToPrinterDlg**](connecttoprinterdlg.md)的呼叫所建立之印表機的連接。 <br/>                                                                                                                                      |
| [**DeletePrinterData**](deleteprinterdata.md)<br/>             | [**DeletePrinterData**](/windows/desktop/printdocs/deleteprinterdata)函式會刪除印表機的指定設定資料。 印表機的設定資料是由一組命名的和具類型的值所組成。 **DeletePrinterData** 函式會刪除其中一個值，並以其值名稱來指定。 <br/>                                                                                                     |
| [**DeletePrinterDataEx**](deleteprinterdataex.md)<br/>         | [**DeletePrinterDataEx**](/windows/desktop/printdocs/deleteprinterdataex)函式會從印表機的設定資料中刪除指定的值。 印表機的設定資料是由一組儲存在登錄機碼階層中的命名和類型值所組成。 函數會刪除指定之索引鍵下的指定值。 <br/>                                                                        |
| [**DeletePrinterKey**](deleteprinterkey.md)<br/>               | [**DeletePrinterKey**](/windows/desktop/printdocs/deleteprinterkey)函式會刪除指定之印表機的指定機碼及其所有子機碼。 <br/>                                                                                                                                                                                                                                                               |
| [**EnumPrinterData**](enumprinterdata.md)<br/>                 | [**EnumPrinterData**](/windows/desktop/printdocs/enumprinterdata)函式會列舉指定印表機的設定資料。 <br/>                                                                                                                                                                                                                                                                               |
| [**EnumPrinterDataEx**](enumprinterdataex.md)<br/>             | [**EnumPrinterDataEx**](/windows/desktop/printdocs/enumprinterdataex)函式會列舉指定之印表機和索引鍵的所有值名稱和資料。 <br/>                                                                                                                                                                                                                                                             |
| [**EnumPrinterKey**](enumprinterkey.md)<br/>                   | [**EnumPrinterKey**](/windows/desktop/printdocs/enumprinterkey)函式會列舉指定印表機之指定機碼的子機碼。 <br/>                                                                                                                                                                                                                                                                     |
| [**>enumprinters**](enumprinters.md)<br/>                       | [**>enumprinters**](/windows/desktop/printdocs/enumprinters)函式會列舉可用的印表機、列印伺服器、網域或列印提供者。 <br/>                                                                                                                                                                                                                                                                 |
| [**FlushPrinter**](flushprinter.md)<br/>                       | [**FlushPrinter**](/windows/desktop/printdocs/flushprinter)函式會將緩衝區傳送至印表機，以便從暫時性狀態中清除。 <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | [**GetDefaultPrinter**](/windows/desktop/printdocs/getdefaultprinter)函式會針對本機電腦上的目前使用者，抓取預設印表機的印表機名稱。 <br/>                                                                                                                                                                                                                                    |
| [**GetPrinter**](getprinter.md)<br/>                           | [**GetPrinter**](/windows/desktop/printdocs/getprinter)函式會捕獲指定印表機的相關資訊。 <br/>                                                                                                                                                                                                                                                                                               |
| [**GetPrinterData**](getprinterdata.md)<br/>                   | [**GetPrinterData**](/windows/desktop/printdocs/getprinterdata)函式會抓取指定印表機或列印伺服器的設定資料。 <br/>                                                                                                                                                                                                                                                                |
| [**GetPrinterDataEx**](getprinterdataex.md)<br/>               | [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex)函式會抓取指定印表機或列印伺服器的設定資料。 **GetPrinterDataEx** 可以取出 [**SetPrinterData**](setprinterdata.md) 函數所儲存的值。 此外， **GetPrinterDataEx** 可以透過 [**SetPrinterDataEx**](setprinterdataex.md) 函數來取出儲存在指定索引鍵下的值。 <br/> |
| [**IsValidDevmode**](isvaliddevmode.md)<br/>                   | [**IsValidDevmode**](isvaliddevmode.md)函數會驗證 DEVMODE 結構的內容是否有效。 <br/>                                                                                                                                                                                                                                                                           |
| [**ReadPrinter**](readprinter.md)<br/>                         | [**ReadPrinter**](/windows/desktop/printdocs/readprinter)函數會從指定的印表機抓取資料。 <br/>                                                                                                                                                                                                                                                                                                   |
| [**ResetPrinter**](resetprinter.md)<br/>                       | [**ResetPrinter**](/windows/desktop/printdocs/resetprinter)函式會指定要用於列印 [**StartDocPrinter**](startdocprinter.md)函式所提交檔的資料類型和裝置模式值。 在檔列印開始之後，您可以使用 [**SetJob**](setjob.md) 函數來覆寫這些值。 <br/>                                                                  |
| [**SetDefaultPrinter**](setdefaultprinter.md)<br/>             | [**SetDefaultPrinter**](/windows/desktop/printdocs/setdefaultprinter)函式會設定本機電腦上目前使用者之預設印表機的印表機名稱。 <br/>                                                                                                                                                                                                                                         |
| [**SetPort**](setport.md)<br/>                                 | [**SetPort**](/windows/desktop/printdocs/setport)函式會設定與印表機埠相關聯的狀態。 <br/>                                                                                                                                                                                                                                                                                                      |
| [**SetPrinter**](setprinter.md)<br/>                           | [**SetPrinter**](/windows/desktop/printdocs/setprinter)函式會設定指定印表機的資料，或藉由暫停列印、繼續列印或清除所有列印工作來設定指定印表機的狀態。 <br/>                                                                                                                                                                                           |
| [**SetPrinterData**](setprinterdata.md)<br/>                   | [**SetPrinterData**](/windows/desktop/printdocs/setprinterdata)函數會設定印表機或列印伺服器的設定資料。 <br/>                                                                                                                                                                                                                                                                             |
| [**SetPrinterDataEx**](setprinterdataex.md)<br/>               | [**SetPrinterDataEx**](/windows/desktop/printdocs/setprinterdataex)函數會設定印表機或列印伺服器的設定資料。 此函數會將設定資料儲存在印表機的登錄機碼下。 <br/>                                                                                                                                                                                            |
| [**WritePrinter**](writeprinter.md)<br/>                       | [**WritePrinter**](writeprinter.md)函數會通知列印多工緩衝處理器，資料應該寫入指定的印表機。 <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>印表機變更通知功能

這些功能可讓應用程式在印表機狀態變更時收到通知。



| 函式                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)<br/> | [**FindClosePrinterChangeNotification**](/windows/desktop/printdocs/findcloseprinterchangenotification)函式會關閉藉由呼叫 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函數所建立的變更通知物件。 與變更通知物件相關聯的印表機或列印伺服器，將不會再由該物件監視。 <br/> |
| [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)<br/> | [**FindFirstPrinterChangeNotification**](/windows/desktop/printdocs/findfirstprinterchangenotification)函式會建立變更通知物件，並將控制碼傳回物件。 然後，您可以在呼叫其中一個等候函式時，使用這個控制碼來監視印表機或列印伺服器的變更。 <br/>                                                                              |
| [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)<br/>   | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函式會針對與印表機或列印伺服器相關聯的變更通知物件，抓取最新變更通知的相關資訊。 當滿足變更通知物件的等候作業時，請呼叫此函式。 <br/>                                           |
| [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md)<br/>                           | [**FreePrinterNotifyInfo**](/windows/desktop/printdocs/freeprinternotifyinfo)函式會釋放由 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函數所建立的系統組態緩衝區。 <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>印表機表單函式

這些函數會管理印表機所使用的表單。



| 函式                                    | 描述                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddForm**](addform.md)<br/>       | [**AddForm**](/windows/desktop/printdocs/addform)函式會將表單新增至可針對指定印表機選取的可用表單清單。 <br/> |
| [**DeleteForm**](deleteform.md)<br/> | [**DeleteForm**](/windows/desktop/printdocs/deleteform)函數會從支援的表單清單中移除表單名稱。 <br/>                                |
| [**EnumForms**](enumforms.md)<br/>   | [**EnumForms**](/windows/desktop/printdocs/enumforms)函式會列舉指定印表機所支援的表單。 <br/>                               |
| [**GetForm**](getform.md)<br/>       | [**GetForm**](/windows/desktop/printdocs/getform)函式會捕獲指定表單的相關資訊。 <br/>                                              |
| [**SetForm**](setform.md)<br/>       | [**SetForm**](/windows/desktop/printdocs/setform)函式會設定指定印表機的表單資訊。 <br/>                                       |



 

## <a name="print-spooler-functions"></a>列印多工緩衝處理器函式

這些函式會在低層級與列印多工緩衝處理器互動。



| 函式                                                          | 描述                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseSpoolFileHandle**](closespoolfilehandle.md)<br/>   | [**CloseSpoolFileHandle**](/windows/desktop/printdocs/closespoolfilehandle)函式會關閉與應用程式目前所提交列印工作相關聯之多工緩衝處理檔案的控制碼。 <br/>                    |
| [**CommitSpoolData**](commitspooldata.md)<br/>             | [**CommitSpoolData**](/windows/desktop/printdocs/commitspooldata)函式會通知列印多工緩衝處理器，指定的資料量已寫入指定的多工緩衝處理檔案，而且已準備好可供轉譯。 <br/> |
| [**GetPrintExecutionData**](getprintexecutiondata.md)<br/> | [**GetPrintExecutionData**](getprintexecutiondata.md)會捕獲目前的列印內容。<br/>                                                                                             |
| [**GetSpoolFileHandle**](getspoolfilehandle.md)<br/>       | [**GetSpoolFileHandle**](/windows/desktop/printdocs/getspoolfilehandle)函式會抓取與應用程式目前所提交之作業相關聯的多工緩衝處理檔案的控制碼。 <br/>                        |



 

 


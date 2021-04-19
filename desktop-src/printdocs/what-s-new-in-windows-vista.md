---
description: 列出 (Api) Windows Vista 中引進的列印應用程式設計介面。
ms.assetid: 7a4eb5d7-b37d-4090-aea4-7274daa1e15c
title: Windows Vista 中的列印功能新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8648d57f48623e6db0f6311bb07ae24ac15d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989478"
---
# <a name="whats-new-for-printing-in-windows-vista"></a>Windows Vista 中的列印功能新功能

列出 (Api) Windows Vista 中引進的列印應用程式設計介面。

下列函數和列舉是用來管理列印票證。



| 函式                                                               | 描述                                                                                                                                   | 標頭    | 程式庫     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------|-------------|
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) | 將列印票證轉換成 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構。                                                                            | Prntvpt。h | Prntvpt .lib |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) | 將 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 轉換為列印票證。                                                                                      | Prntvpt。h | Prntvpt .lib |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)                             | 釋放特定列印票證管理功能所建立的緩衝區。                                                                        | Prntvpt。h | Prntvpt .lib |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) | 驗證兩個列印票證，並將其合併成可行的列印票證。                                                                            | Prntvpt。h | Prntvpt .lib |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)               | 取得印表機功能的帳戶。                                                                                                | Prntvpt。h | Prntvpt .lib |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)                               | 開啟列印票證提供者。                                                                                                                | Prntvpt。h | Prntvpt .lib |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)                           | 開啟列印票證提供者，即使它不支援慣用的 [列印架構](./print-schema.md)版本。 | Prntvpt。h | Prntvpt .lib |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)                             | 關閉列印票證提供者。                                                                                                               | Prntvpt。h | Prntvpt .lib |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)     | 取得指定印表機支援的 [列印架構](./print-schema.md) 最新版本。                        | Prntvpt。h | Prntvpt .lib |



 



| 列舉型別                                        | 描述                                                                                                                                                                               | 標頭    |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) | 當列印票證未指定任何可能在 **DEVMODE** 中的設定時，可讓呼叫者指定要使用哪一個 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)作為預設值的來源。 | Prntvpt。h |
| [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope)     | 指定列印票證的範圍。                                                                                                                                                    | Prntvpt。h |



 

以下是用來安裝印表機驅動程式的功能。



| 函式                                                                   | 描述                                                                                                                                                                 | 標頭     | 程式庫      |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CorePrinterDriverInstalled**](coreprinterdriverinstalled.md)           | 報告是否已安裝具有指定之 GUID、日期和版本的核心印表機驅動程式。                                                                                | Winspool.drv。h | Winspool.drv .lib |
| [**DeletePrinterDriverPackage**](deleteprinterdriverpackage.md)           | 從驅動程式存放區刪除印表機驅動程式套件。                                                                                                                     | Winspool.drv。h | Winspool.drv .lib |
| [**GetCorePrinterDrivers**](getcoreprinterdrivers.md)                     | 取得指定之核心印表機驅動程式的 GUID、版本和日期，以及其套件的路徑。                                                                      | Winspool.drv。h | Winspool.drv .lib |
| [**GetPrinterDriverPackagePath**](getprinterdriverpackagepath.md)         | 取得列印伺服器上指定之印表機驅動程式套件的路徑。                                                                                                    | Winspool.drv。h | Winspool.drv .lib |
| [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) | 從列印伺服器的驅動程式存放區中的驅動程式套件安裝印表機驅動程式。                                                                                         | Winspool.drv。h | Winspool.drv .lib |
| [**UploadPrinterDriverPackage**](uploadprinterdriverpackage.md)           | 將印表機驅動程式上傳至列印伺服器的驅動程式存放區，使其可與 [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md)一起安裝。 | Winspool.drv。h | Winspool.drv .lib |



 

下列函式、列舉和結構可用於列印以及管理印表機和印表機連接。



| 函式                                               | 描述                                                                                                                                              | 標頭     | 程式庫      |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**AddPrinterConnection2**](addprinterconnection2.md) | 將連接加入至指定的印表機，以供目前的使用者使用。                                                                                         | Winspool.drv。h | Winspool.drv .lib |
| [**OpenPrinter2**](openprinter2.md)                   | 在設定部分印表機選項時，抓取指定印表機或列印伺服器的控制碼，或列印子系統中其他類型的控制碼。 | Winspool.drv。h | Winspool.drv .lib |



 



| 列舉型別                                            | 描述                                                                                       | 標頭     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------|------------|
| [**印表機 \_ 選項 \_ 旗標**](printer-option-flags.md) | 指定以 [**OpenPrinter2**](openprinter2.md)開啟之印表機的控制碼快取。 | Winspool.drv。h |



 



| 結構                                                         | 描述                                                                            | 標頭     |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------|
| [**核心 \_ 印表機 \_ 驅動程式**](core-printer-driver.md)              | 代表其他印表機驅動程式相依的印表機驅動程式。              | Winspool.drv。h |
| [**驅動程式 \_ 資訊 \_ 8**](driver-info-8.md)                          | 代表印表機驅動程式。                                                           | Winspool.drv。h |
| [**表單 \_ 資訊 \_ 2**](form-info-2.md)                              | 代表可當地語系化之列印表單的相關資訊。                                 | Winspool.drv。h |
| [**作業 \_ 資訊 \_ 4**](job-info-4.md)                                | 表示與作業相關聯的一組完整值，並支援64位多工緩衝處理檔案。 | Winspool.drv。h |
| [**印表機 \_ 連接 \_ 資訊 \_ 1**](printer-connection-info-1.md) | 代表印表機連接的相關資訊。                                | Winspool.drv。h |
| [**印表機 \_ 選項**](printer-options.md)                       | 代表印表機選項。                                                            | Winspool.drv。h |
| [**PRINTPROCESSOR \_ CAPS \_ 2**](printprocessor-caps-2.md)          | 代表印表機功能資訊。                                             | Winspool.drv。h |



 

下列函數、列舉和介面可用來執行新的非同步列印通知系統。



| 函式                                                                             | 描述                                                                                                                                                                                       | 標頭     | 程式庫      |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)               | 在多工緩衝處理器裝載的列印元件之間建立通道，例如列印驅動程式或埠監視器，以及需要從元件接收通知的應用程式。 | Prnasnot。h | Winspool.drv .lib |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)     | 註冊應用程式，以接收來自多工緩衝處理器主控元件的通知，例如印表機驅動程式、列印處理器和埠監視器。                                                    | Prnasnot。h | Winspool.drv .lib |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications) | 啟用已註冊的應用程式，以接收來自多工緩衝處理器的列印元件的通知，以結束其對通知的訂閱。                                         | Prnasnot。h | Winspool.drv .lib |



 



| 列舉型別                                                                    | 描述                                                                                                                                                                                                          | 標頭     |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| [**PrintAsyncNotifyConversationStyle**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle) | 指定應用程式和列印多工緩衝處理器裝載的元件（如印表機驅動程式、列印處理器和埠監視器）之間的通訊是否為雙向或單向。                          | Prnasnot。h |
| [**PrintAsyncNotifyError**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)                         | 指定非同步通知交易中的錯誤。                                                                                                                                                      | Prnasnot。h |
| [**PrintAsyncNotifyUserFilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)               | 指定通知是否只會傳送給與「列印多工緩衝處理器」主控的寄件者相關聯的應用程式，或是否要移至一組更廣泛的接聽應用程式。 | Prnasnot。h |



 



| 介面和方法                                                                                                      | 描述                                                                                                                                                   | 標頭     | 程式庫      |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**IPrintAsyncNotifyCallback::ChannelClosed**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-channelclosed)    | 由通道的一個成員用來通知另一個要關閉通道的成員。                                                    | Prnasnot。h | Winspool.drv .lib |
| [**IPrintAsyncNotifyCallback::OnEventNotify**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify)    | 由列印多工緩衝處理器呼叫，以警示接聽程式，通知可用於指定的通道。                                                      | Prnasnot。h | Winspool.drv .lib |
| [**IPrintAsyncNotifyChannel::CloseChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel)         | 關閉通道。                                                                                                                               | Prnasnot。h | Winspool.drv .lib |
| [**IPrintAsyncNotifyChannel：： SendNotification**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification) | 將來自「列印多工緩衝處理器」元件的通知傳送至一或多個接聽的應用程式，或將應用程式的回應傳送回元件。 | Prnasnot。h | Winspool.drv .lib |
| [**IPrintAsyncNotifyDataObject::AcquireData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata)  | 將接聽應用程式的端點指向通知資料，以及資料的大小和類型。                                                                   | Prnasnot。h | Winspool.drv .lib |
| [**IPrintAsyncNotifyDataObject::ReleaseData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata)  | 釋放封裝在 [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)中的資料所使用的記憶體。                                  | Prnasnot。h | Winspool.drv .lib |



 

下列列舉和結構會用來叫用 Microsoft XPS 檔轉換器 (MXDC) 將 XML 檔規格 (XPS) 檔寫入至裝置或檔案。



| 列舉型別                                | 描述                                                            | 標頭 |
|--------------------------------------------|------------------------------------------------------------------------|--------|
| [**MxdcS0PageEnums**](mxdcs0pageenums.md) | 指定 XPS 頁面上的資源類型，例如字型或影像。 | Mxdc。h |



 



| 結構                                                          | 描述                                                                                                                                    | 標頭 |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| [**MxdcEscapeHeader**](mxdcescapeheader.md)                       | 表示 MXDC 的指示。                                                                                                         | Mxdc。h |
| [**MxdcGetFileNameData**](mxdcgetfilenamedata.md)                 | 代表 MXDC 輸出檔的完整路徑和名稱。                                                                                     | Mxdc。h |
| [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)             | 表示 [**MxdcEscapeHeader**](mxdcescapeheader.md) 和 [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)的組合。 | Mxdc。h |
| [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)   | 代表將與 XPS 檔相關聯的列印票證。                                                                        | Mxdc。h |
| [**MxdcS0PageData**](mxdcs0pagedata.md)                           | 代表要傳遞給 MXDC 輸出檔的 XPS 格式頁面，而不進行任何處理。                                                  | Mxdc。h |
| [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) | 表示 [**MxdcEscapeHeader**](mxdcescapeheader.md) 和 [**MxdcS0PageData**](mxdcs0pagedata.md)的組合。                         | Mxdc。h |
| [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)       | 表示 [**MxdcEscapeHeader**](mxdcescapeheader.md) 和 [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)的組合。           | Mxdc。h |
| [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)             | 代表 MXDC 在 XPS 頁面上包含的資源，例如字型或影像。                                                   | Mxdc。h |



 

 

 

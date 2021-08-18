---
description: GDI 列印 API 函式
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: GDI 列印 API 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcdb6119a56524d3e94c1c1e35f3f1a95bfb86d6e9a23343b07d4250bfc178eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971507"
---
# <a name="gdi-print-api-functions"></a>GDI 列印 API 函式

## <a name="in-this-section"></a>本節內容



| 函式                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | [**AbortDoc**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc)函式會停止目前的列印工作，並清除自從最後一次呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)函式之後所繪製的所有專案。<br/>                                                                                                                                                                                                 |
| [*AbortProc*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | [**AbortProc**](/windows/desktop/api/wingdi/nc-wingdi-abortproc)函式是與 [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)函數搭配使用的應用程式定義回呼函數。 當列印工作在幕後處理期間取消時，會呼叫此檔案。 **ABORTPROC** 型別定義此回呼函數的指標。 **AbortProc** 是應用程式定義函數名稱的預留位置。<br/> |
| [**DeviceCapabilities**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | [**DeviceCapabilities**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa)函式會捕獲印表機驅動程式的功能。<br/>                                                                                                                                                                                                                                                       |
| [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | [**EndDoc**](/windows/desktop/api/wingdi/nf-wingdi-enddoc)函式會結束列印工作。<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | **EndPage** 函式會通知裝置應用程式已完成寫入頁面。 此函式通常用來指示設備磁碟機前進至新的頁面。<br/>                                                                                                                                                                             |
| [**逸出**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | 讓應用程式存取無法透過 GDI 使用的系統定義裝置功能。<br/>                                                                                                                                                                                                                                                         |
| [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | [**ExtEscape**](/windows/desktop/api/wingdi/nf-wingdi-extescape)函式可讓應用程式存取無法透過 GDI 使用的裝置功能。<br/>                                                                                                                                                                                                                                |
| [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md)<br/> | [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md)函式會判斷指定的視窗目前是否重新導向以進行列印。<br/>                                                                                                                                                                                                         |
| [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | [**PrintWindow**](/windows/desktop/api/winuser/nf-winuser-printwindow)函式會將視覺化視窗複製到指定的裝置內容 (DC) ，通常是印表機 DC。<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | [**SetAbortProc**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc)函式會設定應用程式定義的 abort 函式，以允許在幕後處理期間取消列印工作。<br/>                                                                                                                                                                                                               |
| [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | [**StartDoc**](/windows/desktop/api/wingdi/nf-wingdi-startdoca)函式會啟動列印工作。<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | [**StartPage**](/windows/desktop/api/wingdi/nf-wingdi-startpage)函數會準備印表機驅動程式來接受資料。<br/>                                                                                                                                                                                                                                                                             |



 

 


---
description: GDI 列印 API 會提供應用程式與裝置無關的列印介面。
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: GDI 列印 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192718"
---
# <a name="gdi-print-api"></a>GDI 列印 API

GDI 列印 API 會提供應用程式與裝置無關的列印介面。 如果應用程式使用 GDI 來呈現文字和圖形，請使用此介面。

如果您撰寫適用于 Windows Vista 或更新版本 Windows 的應用程式，請考慮使用「 [Xps 檔 api](/previous-versions/windows/desktop/dd316976(v=vs.85)) 」和「 [xps 列印 api](xps-printing.md) 」來使用 XPSDrv 列印驅動程式所支援的較高效能圖形介面。

本節提供下列主題的相關資訊。



| 主題                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 GDI 列印 API](about-the-gdi-print-api.md)<br/>                                 | GDI 列印功能的總覽。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [使用 GDI 列印 API](using-the-printing-functions.md)<br/>                            | 在應用程式中使用 GDI 列印 API 的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [GDI 列印 API 參考](gdi-print-api-reference.md)<br/>                                 | GDI 列印 API 的函式、結構和其他元素的詳細說明。<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS 檔轉換器 (MXDC) ](microsoft-xps-document-converter--mxdc-.md)<br/> | [MICROSOFT XPS 檔轉換器 (MXDC) ](microsoft-xps-document-converter--mxdc-.md)是一種元件，可讓應用程式搭配具有 XPSDrv 列印驅動程式的印表機使用 GDI 列印 API。<br/>                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Writer (MXDW) ](microsoft-xps-document-writer.md)<br/>              | [MICROSOFT XPS Document Writer (MXDW) ](microsoft-xps-document-writer.md)提供具有「儲存為 xps」或「匯出至 xps」功能的應用程式。 未以原生方式建立 XPS 檔內容的應用程式可以使用 MXDW 建立 XPS 檔檔，而不需要使用 [xps 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))。 不過，XPS 檔 API 提供的應用程式能夠使用 XPSDrv 列印驅動程式所支援的較高效能圖形介面。<br/> |



 

下圖顯示 GDI 列印 API 與應用程式可使用的其他列印 Api 的關聯性。

![顯示 gdi 列印 api 與 win32 應用程式可使用的其他列印 api 關聯性的圖表](images/print-apis-gdi.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**System.printing.printqueue.addjob**](addjob.md)
</dt> <dt>

[XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS 列印 API](xps-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API](print-spooler-api.md)
</dt> <dt>

[列印票證 API](print-ticket-api.md)
</dt> </dl>

 


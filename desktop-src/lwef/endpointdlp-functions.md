---
title: 端點資料遺失防止函式
description: 端點資料遺失防止功能所使用的函數。
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: f4a6395dacfdeccd032f7ad54719082c0e69f33692bda32798c09592c95d318e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751630"
---
# <a name="endpoint-data-loss-prevention-functions"></a>端點資料遺失防止函式

端點資料遺失防止功能所使用的函數。



| 函式                                                       | Description                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | 在開機檔案關閉作業之前，為系統提供檔的相關資訊。                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | 在開機檔案關閉作業之前，為系統提供檔的相關資訊。                                  |
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | 當輸入放置目標時，為系統提供檔的相關資訊。                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | 在目前的裝置上，抓取端點資料遺失防止 (DLP) API 的版本。                                  |
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | 針對一組端點資料遺失防止 (DLP) 作業，通知系統所需的強制模式。                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | 判斷應用程式是否必須從系統剪貼簿提取資料，而不是從其內部快取中取得資料。                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | 當卸載目標結束時，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | 在複製到剪貼簿作業完成後，為系統提供檔的相關資訊。  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | 在拖放作業完成後，為系統提供檔的相關資訊。  |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md)                       | 在開啟作業完成後，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | 在開啟作業完成後，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | 在貼上剪貼簿作業完成後，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | 在列印工作完成後，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | 在 [另存新檔] 作業完成後，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | 在列印工作開始後，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | 提供隱藏專案剪貼簿作業完成後的系統狀態資訊。                                  |
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | 在起始複製到剪貼簿作業之前，為系統提供檔的相關資訊。  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | 在起始拖放作業之前，為系統提供檔的相關資訊。  |
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md)                         | 在起始開啟作業之前，為系統提供檔的相關資訊。  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | 在起始開啟作業之前，為系統提供檔的相關資訊。  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | 為系統提供檔的相關資訊，再開始貼上剪貼簿作業。  |
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | 在開始列印工作之前，為系統提供檔的相關資訊。  |
| [DlpNotifyPreSaveDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | 在起始「另存新檔」作業之前，為系統提供檔的相關資訊。                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | 在起始隱藏剪貼簿作業之前通知系統。                                  |